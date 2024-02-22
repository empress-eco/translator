<div align="center">

<img src="https://grow.empress.eco/uploads/default/original/2X/1/1f1e1044d3864269d2a613577edb9763890422ab.png" alt="Logo" width="80" height="80">

# Translator: Unlock Multilingual Power for Your Apps

Welcome to Translator, the go-to solution for developers seeking to implement versatile multilingual support in their applications!

[Explore the Docs](https://grow.empress.eco/) | [Report Bug](https://github.com/empress-eco/translator/issues) | [Request Feature](https://github.com/empress-eco/translator/issues)

</div>

## About The Project
Translator is a dynamic translation portal specifically designed for developers. With the ability to add new languages, efficiently update translations, and smoothly export translations into your applications, Translator equips you with powerful tools to enhance your app's multilingual capabilities.

### Key Features:
- Hassle-free addition of new languages
- Efficient updating of translations
- Seamless exporting of translations

## Technical Stack and Setup Instructions

### Prerequisites
A basic understanding of the bench command-line tool is required to get started with Translator.

### Installation & Usage

Clone the repository using the following command:
```sh
git clone https://github.com/empress-eco/translator.git
```
1. To add a new language to your application, follow these steps:

```sh
# Add a new language via desk
bench use translate.YOUR-DOMAIN.com
bench translate-untranslated [language_code]

# Export new languages.json and commit it to the repo
bench execute Empress.core.doctype.language.language.export_languages_json
```

2. Update the latest translations from your apps:

```sh
bench import-source-messages
```

3. Update missing translations:

```sh
bench translate-untranslated-all
```

4. Copy translations from one language to another:

```sh
bench copy-language [from] [to]
```

5. Import the translations into your application:

```sh
# On Remote:
bench --site translate.YOUR-DOMAIN.com execute "translator.data.write_csv_for_all_languages"

# On local bench:
bench download-translations
```

## Contribution Guidelines
We welcome contributions from everyone. Here's how you can contribute:

- Fork the Project
- Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
- Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
- Push to the Branch (`git push origin feature/AmazingFeature`)
- Open a Pull Request

## License and Acknowledgements

### License
This project is licensed under the MIT License. Your contributions will also be licensed under the MIT License.

### Acknowledgements
We express our profound gratitude to the Empress Community, whose innovative tools form the backbone of this project. Their dedication and pioneering work have been instrumental in building the foundations and functionalities we rely on. We are deeply appreciative of their support.