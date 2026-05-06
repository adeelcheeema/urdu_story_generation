## Project Summary

This notebook demonstrates a character-level recurrent neural network (RNN) model for text generation in Urdu. The project involves the following key steps:

1.  **Data Loading and Preprocessing**:
    - Loading Urdu text from a `.txt` file.
    - Normalizing the text using `urduhack` for consistency.
    - Cleaning the text by removing special characters, numbers, URLs, emails, and currency symbols.
    - Creating character-to-integer mappings (vocabulary) and vice-versa.
    - Converting the text into sequences of integer IDs.

    _Example Preprocessed Text Snippet:_

    ```
    شہزاد بہت لاپرواہ اور کھیل کود میں مگن رہنے والا لڑکا تھا -سارا دن فضول کھیلوں میں وقت ضائع کرتا تھا -شہزاد کی ماں اس کے بچپن میں فوت ہو گئی تھی اور اس کا باپ صبح سویرے کھیت میں چلا جاتا اور رات کو دیر سے گھر واپس آتا تھا -
    جس وجہ سے شہزاد کی لاپروائ
    ```

    _Vocabulary Size:_ `52 unique characters`

2.  **Dataset Preparation**:
    - Creating input and target sequences for the RNN model. Each input sequence predicts the next character in the target sequence.
    - Batching and shuffling the dataset for efficient training.

3.  **Model Architecture (RNN with GRU/LSTM)**:
    - Defining a character-level RNN model using `tf.keras.Sequential`.
    - The model typically consists of:
      - An `Embedding` layer to convert character IDs into dense vectors.
      - A `GRU` (Gated Recurrent Unit) or `LSTM` (Long Short-Term Memory) layer to process sequences and capture dependencies.
      - A `Dense` layer to output logits for each character in the vocabulary.

4.  **Model Training**:
    - Compiling the model with an Adam optimizer and `SparseCategoricalCrossentropy` loss.
    - Training the model for a specified number of epochs, saving checkpoints to track progress.

5.  **Text Generation**:
    - Implementing a function to generate new text given a starting string.
    - The model predicts the next character based on the current character and its internal state.
    - Using a `temperature` parameter to control the randomness of the generated text.

    _Example Generated Text:_

    ```
    محبتی سے پہلے ہی لگتا تھا -پھر اچانک میرا نام سنا ہو - پھروں کے منہ سے قیمتی چھوٹے سے پیٹ پرانے کا عذر تب جارہاہے -
    چچا چمن نے خوشگوار حکمت سے ہمیں فائدہ پہنچایا تو کہیں کل کی پیٹھ پر سکون نہیں  -توبنٹھلی گئیں اور پانچواں چینی بھائی کی پریشانی دیکھ کر می خوش اور مہربانیتے  -
    ایک روز ملک اپنی جماعت سے نکالا تو بالے نے پوچھا -
     سا پیچھے ان تینوں کے ساتھ تمہیں تجربے کھوپڑی نے اسے گروہ کافی حد تک گند اللہ ہے اپنے کھیتوں اور برائی کروں گا وہ صرف چو یں میں آفس میں پھنس گیا اور آخر معاف کر دی  -اس دوران کا کار آپ کا دینھ کام کرنے اور معذوئی زندگی کے کتابوں کا تحریک پتہ تھا کہ نزی خریدی چور کو اسکا ذکر پریعام لگتا تھا اور اب جن کی سوچ سمجھ تھی اور اب وہ بچہ چیز کھیلنے کی ضرورت نہیں -
    دونوں تیار ہو گی -
     کس وقت آٹ کو پیر کباڑی کی دنیا میں جانے لگی  -اسے جانوروں کی برائی کرنے لگا -میں نے کس طرح سے بھی خیال نکالا ہوا بولا- امی حضور جب میں اسکول کی خاتون تھی کہ اسے کسی دوست یا رشتے دار کے ہاتھوں پر فٹوخت کے چھلانگ لگائی اور لوگوں نے روین سے بیٹھ گیا- انہیں روز محض یہ کرتے ہوئے سمجھائی کہ ناصر اتنی بڑ
    ```

This notebook provides a complete pipeline from raw Urdu text to a trained text generation model, showcasing the capabilities of RNNs for creative text synthesis.
