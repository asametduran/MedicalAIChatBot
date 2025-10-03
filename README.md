# 🩺🤖 MedicalAIChatBot

Merhaba! 👋  
MedicalAIChatBot, tıbbi dokümanlardan bilgi çekebilen ve kullanıcı sorularına yapay zeka ile yanıt verebilen bir chatbot uygulamasıdır.  
Bu projede **Flask**, **LangChain**, **Pinecone**, **Google Gemini API**, **AWS** ve **Docker** gibi modern teknolojiler kullanılmıştır! 🚀

---

## 🚦 Özellikler

✨ PDF dosyalarından tıbbi metinleri otomatik olarak işler  
✨ HuggingFace ile metin embedding işlemleri  
✨ Pinecone üzerinde vektör tabanlı arama  
✨ Google Gemini API ile akıllı soru-cevap  
✨ Flask ile web arayüzü  
✨ AWS EC2 ve ECR ile otomatik CI/CD pipeline  
✨ Docker ile kolay kurulum ve dağıtım

---

## 🛠️ Kurulum

### 1️⃣ Gerekli Paketler

```bash
pip install -r requirements.txt
```

### 2️⃣ Ortam Değişkenleri

Proje kök dizininde `.env` dosyası oluşturun ve aşağıdaki anahtarları ekleyin:

```
PINECONE_API_KEY=your_pinecone_api_key
GOOGLE_API_KEY=your_google_api_key
```

### 3️⃣ Docker ile Çalıştırma

```bash
docker build -t medical-ai-chatbot .
docker run -p 8080:8080 --env-file .env medical-ai-chatbot
```

### 4️⃣ Lokal Çalıştırma

```bash
python app.py
```

---

## 💻 Kullanım

- Web arayüzüne gidin: [http://localhost:8080](http://localhost:8080) 🌐
- Sorunuzu yazın, tıbbi dokümanlardan AI destekli yanıt alın! 🧑‍⚕️🤖

---

## 📁 Dosya Yapısı

```
├── app.py                # Flask backend ve chatbot API
├── src/
│   ├── helper.py         # Veri işleme ve yardımcı fonksiyonlar
│   └── prompt.py         # Sistem promptları
├── store_index.py        # PDF yükleme ve Pinecone index oluşturma scripti
├── research/
│   └── trials.ipynb      # Proje denemeleri ve ilk testler
├── templates/
│   └── chat.html         # Web arayüzü
├── static/
│   └── style.css         # Arayüz stilleri
├── .env                  # API anahtarları
├── Dockerfile            # Docker imajı için yapılandırma
└── .github/workflows/
    └── cicd.yaml         # CI/CD pipeline
```

---

## 🚀 CI/CD ve Dağıtım

- Her kod güncellemesinde **GitHub Actions** ile otomatik olarak Docker imajı oluşturulur ve AWS ECR’a push edilir.
- AWS EC2 üzerinde otomatik olarak güncellenir ve yayına alınır.

---

## 🤝 Katkı ve Lisans

Katkıda bulunmak için pull request gönderebilirsin!  
Bu proje MIT lisansı ile lisanslanmıştır.

---

**Hazırlayan:** Samet DURAN  
**İletişim:** asametdurann@gmail.com

---

> 💡 **Haydi, tıbbi bilginin gücünü yapay zeka ile birleştir!**
