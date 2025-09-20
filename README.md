#  MyShell Python (Kivy) - prototype
Conteúdo gerado: 2025-09-18T22:55:40.235156 UTC
Arquivos principais gerados:
⦁	main.py          : aplicativo Kivy que apresenta a avaliação e verifica respostas
⦁	config.json      : arquivo com salt e hash PBKDF2 da sequência de respostas (mantido seguro)
⦁	requirements.txt : dependências (Kivy)
Como testar no desktop (Windows/Linux/macOS):
1.	Instale Python 3.9+ e um ambiente virtual:
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate    # Windows (PowerShell: venv\Scripts\Activate.ps1)
2.	Instale dependências:
pip install -r requirements.txt
3.	Coloque config.json e main.py na mesma pasta (já estão aqui)
4.	Execute:
python main.py
Build / packaging:
⦁	Windows/Mac/Linux: use PyInstaller to gerar executável
⦁	Android: use Buildozer (Kivy) or Briefcase (BeeWare alternative) - Buildozer is recommended
⦁	iOS: use kivy-ios / Xcode (more complex; requires macOS and provisioning)
Notes on mobile:
⦁	Kivy apps can run on Android and iOS, but packaging and signing differ per platform.
⦁	For Android, use Buildozer (Linux or WSL). For iOS, use kivy-ios and Xcode on macOS.
Security notes:
⦁	config.json contains the password salt+hash; proteja o arquivo. Se for distribuir, considere usar keystore ou mecanismo seguro.
⦁	Este protótipo exige respostas exatas (normalização simples). Para aceitar sinônimos ou pontuação parcial, implemente verificação po
