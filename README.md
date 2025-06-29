🌐 Language Translation Tool 📝

A simple Python GUI application that translates text into different languages using **Google Translate API** and provides **speech output** with **pyttsx3**. Built using **Tkinter**, this tool offers an intuitive interface for quick translation and accessibility.

## 🖥️ Features

* 🌍 Translate text to any language supported by Google Translate.
* 📋 Copy the translated text to clipboard.
* 🗣️ Listen to the translated text using text-to-speech.
* ❌ Clear the input and output fields.
* 🎨 Colorful and user-friendly GUI.

---

## 📂 Project Structure

```bash
language_translator/
│
├── translator_gui.py          # Main Python GUI script
├── TRANSLATORICON.ico         # Icon used in the application window (optional)
└── README.md                  # Project description and usage (this file)
```

---

## 🔧 Requirements

Install the following Python packages before running the app:

```bash
pip install googletrans==4.0.0rc1
pip install pyttsx3
```

---

## 🚀 How It Works

### 1. **UI Layout**:

* A pink-colored background window using `tkinter.Tk()`.
* Labels like “Language Translator”, “Enter Text”, and “Translation” to guide the user.
* An `Entry` widget to input text.
* A `Text` widget to display the translation output.
* A `Combobox` to choose destination language from a list of supported languages.
* Buttons for **Translate**, **Speak**, **Copy**, and **Clear**.

### 2. **Translation**:

Uses the `googletrans` module:

```python
translator = Translator()
translated = translator.translate(text=Input_text.get(), dest=dest_lang.get())
```

### 3. **Text-to-Speech**:

Implemented using `pyttsx3`, a text-to-speech conversion library:

```python
engine.say(text)
engine.runAndWait()
```

### 4. **Copy to Clipboard**:

Copies the translated output to your clipboard using:

```python
root.clipboard_append(Output_text.get(1.0, END).strip())
```

---

## 📸 Screenshot

> You can insert an image of your GUI like this:

```markdown
![Screenshot](screenshot.png)
```

---

## ⚠️ Notes

* The `googletrans` library is not an official Google product and may occasionally break due to API changes.
* Ensure your internet connection is active when using translation functionality.
* The `.ico` file must be correctly linked; adjust the path if needed.

---

## 💡 Future Enhancements

* Add **input language auto-detection**.
* Allow saving translation history.
* Support for speech input using `speech_recognition`.

---

## 🧑‍💻 Author

**Vasan**
Feel free to fork, contribute, or report issues.


