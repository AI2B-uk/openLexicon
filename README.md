# openLexicon
Unlock the world of accents with openLexicon – your open-source repository for pronunciation lexicons tailored for speech synthesis engines like AWS Polly. Our mission is to bring authentic regional pronunciations to your applications, making speech synthesis more natural and relatable.

## 🌍 International Pronunciation Lexicons
Explore a diverse range of lexicons meticulously crafted to represent various languages, countries, and regional accents. Whether you're aiming for the crisp tones of Received Pronunciation or the warm drawl of Southern American English, openLexicon has you covered.

## 📂 Directory Structure
Our lexicons are organised using a clear and intuitive international directory structure:
  ```bash
  openLexicon/
  ├── en/
  │   ├── GB/
  │   │   ├── northern/
  │   │   ├── rp/
  │   │   └── scottish/
  │   └── US/
  │       ├── southern/
  │       └── new_york/
  ├── es/
  │   ├── ES/
  │   │   └── castilian/
  │   └── MX/
  │       └── mexican/
  ├── fr/
  │   ├── FR/
  │   │   └── parisian/
  │   └── CA/
  │       └── quebec/
  ```
- *Language Codes*: ISO 639-1 (e.g., en for English).
- *Country Codes*: ISO 3166-1 alpha-2 (e.g., GB for the United Kingdom).
- *Regional Accents/Dialects*: Specific accent or dialect (e.g., northern, rp).

## 🚀 Getting Started
1. Clone the Repository
  ```bash
  git clone https://github.com/AI2B-uk/openLexicon.git
  ```
2. Navigate to a Lexicon
  ```bash
  cd openLexicon/en/GB/northern/
  ```
3. Integrate with AWS Polly
- Upload the lexicon.xml file to your AWS Polly account.
- Reference the lexicon in your speech synthesis requests.

## 🛠️ Usage Example
  ```python
  import boto3
  
  polly = boto3.client('polly')
  response = polly.synthesize_speech(
      Text='Your text here.',
      OutputFormat='mp3',
      VoiceId='Amy',  # Choose an appropriate voice
      LexiconNames=['northern_uk_lexicon']
  )
  
  with open('speech.mp3', 'wb') as file: 
      file.write(response['AudioStream'].read())
  ```
## 🤝 Contributing
We welcome contributions from the community! Here's how you can get involved:

1. Fork the Repository
Click on the Fork button in the top-right corner.

2. Create a New Branch
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make Your Changes
- Add new lexicons following the directory structure.
- Update existing lexicons with improvements.
4. Submit a Pull Request
- Open a pull request with a clear description of your changes.

## 📄 License
This project is licensed under the MIT License. See the LICENSE file for details.

## 💡 Why openLexicon?
*Authenticity*: Bring genuine regional accents to your applications.
*Versatility*: Supports multiple languages and dialects.
*Community-Driven*: Built and maintained by language enthusiasts worldwide.

## 📧 Contact Us
Have questions or suggestions? We'd love to hear from you!
- *Email*: hello@ai2b.co.uk

## ⭐ Support the Project
If you find openLexicon useful, please star the repository and share it with others!
