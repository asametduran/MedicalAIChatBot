# MedicalAIChatBot
# MedicalAIChatBot

MedicalAIChatBot, tıbbi dokümanlardan bilgi çekebilen ve kullanıcı sorularına yapay zeka destekli yanıtlar verebilen bir chatbot uygulamasıdır. Proje, Flask web framework, LangChain, Pinecone vektör veritabanı ve Google Gemini API ile geliştirilmiştir. AWS ve Docker ile bulut ortamında otomatik olarak dağıtılabilir.

## Özellikler

- PDF dosyalarından tıbbi metinleri otomatik olarak yükler ve işler.
- HuggingFace ile metin embedding işlemleri gerçekleştirir.
- Pinecone üzerinde vektör tabanlı arama ve veri saklama.
- Google Gemini API ile gelişmiş yapay zeka tabanlı soru-cevap.
- Flask ile web arayüzü ve API servisi.
- AWS EC2 ve ECR üzerinde otomatik CI/CD pipeline (GitHub Actions ile).
- Docker ile kolay kurulum ve dağıtım.

## Kurulum

### 1. Gerekli Paketler

```bash
pip install -r requirements.txt
```

### 2. Ortam Değişkenleri

Proje kök dizininde `.env` dosyası oluşturun ve aşağıdaki anahtarları ekleyin:

```
PINECONE_API_KEY=your_pinecone_api_key
GOOGLE_API_KEY=your_google_api_key
```

### 3. Docker ile Çalıştırma

```bash
docker build -t medical-ai-chatbot .
docker run -p 8080:8080 --env-file .env medical-ai-chatbot
```

### 4. Lokal Çalıştırma

```bash
python app.py
```

## Kullanım

- Web arayüzüne gidin: [http://localhost:8080](http://localhost:8080)
- Sorunuzu yazın ve tıbbi dokümanlardan AI destekli yanıt alın.

## Dosya Yapısı

- `app.py` : Flask backend ve chatbot API
- `src/helper.py` : Veri işleme ve yardımcı fonksiyonlar
- `src/prompt.py` : Sistem promptları
- `store_index.py` : PDF yükleme ve Pinecone index oluşturma scripti
- `research/trials.ipynb` : Proje denemeleri ve ilk testler
- `templates/chat.html` : Web arayüzü
- `static/style.css` : Arayüz stilleri
- `.env` : API anahtarları
- `Dockerfile` : Docker imajı için yapılandırma
- `.github/workflows/cicd.yaml` : CI/CD pipeline

## CI/CD ve Dağıtım

- Her kod güncellemesinde GitHub Actions ile otomatik olarak Docker imajı oluşturulur ve AWS ECR’a push edilir.
- AWS EC2 üzerinde otomatik olarak güncellenir ve yayına alınır.

## Katkı ve Lisans

Katkıda bulunmak için pull request gönderebilirsiniz.  
Bu proje MIT lisansı ile lisanslanmıştır.

---

**Hazırlayan:** Samet DURAN  
**İletişim:** asametdurann@gmail.com
