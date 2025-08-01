# stable-diffusion-colab-guide
Bu repo, metin açıklamalarından (prompt) yüksek kaliteli görseller üreten devrim niteliğindeki **Stable Diffusion** modelini **Google Colab** üzerinde nasıl çalıştıracağınızı adım adım gösteren bir kılavuz içerir. Güçlü bir bilgisayara ihtiyaç duymadan, sadece tarayıcınızı kullanarak kendi yapay zeka sanat eserlerinizi yaratın!

## 🚀 Ne Öğreneceksiniz?
- Hugging Face üzerinden API anahtarı (token) almayı.
- Google Colab'da ücretsiz T4 GPU'yu nasıl aktive edeceğinizi.
- API anahtarınızı Colab'in "Secrets" özelliği ile güvenli bir şekilde nasıl saklayacağınızı.
- `diffusers` kütüphanesi ile Stable Diffusion v1.5 modelini yüklemeyi.
- Kendi `prompt` ve `negative_prompt`'larınızı yazarak hayalinizdeki görselleri üretmeyi.

## 🛠️ Ön Gereksinimler
1.  **Google Hesabı**: Google Colab'ı kullanmak için gereklidir.
2.  **Hugging Face Hesabı**: Modeli indirmek için ücretsiz bir API anahtarı almak üzere gereklidir.

## 📝 Kurulum ve Kullanım

Sadece 3 basit adımla görselinizi üretebilirsiniz.

### Adım 1: Hugging Face Token'ınızı Alın
Modeli indirebilmek için Hugging Face'den ücretsiz bir anahtar almanız gerekiyor.
1.  [Hugging Face web sitesine](https://huggingface.co/join) gidin ve bir hesap oluşturun.
2.  Profilinize gidin: **Profile > Settings > Access Tokens**.
3.  **"New token"** butonuna tıklayın ve bir isim verin. **`Read`** rolü yeterlidir.
4.  Oluşturulan ve `hf_...` ile başlayan token'ı kopyalayın.

### Adım 2: Google Colab'ı Yapılandırın
1.  Yukarıdaki **"Open In Colab"** butonuna tıklayarak not defterini açın.
2.  **EN ÖNEMLİ ADIM:** Menüden **Çalışma Zamanı > Çalışma zamanı türünü değiştir**'e gidin.
3.  Açılan pencerede "Donanım hızlandırıcı" olarak **T4 GPU**'yu seçin ve kaydedin.
4.  Sol menüdeki **anahtar (🔑) simgesine** tıklayarak "Gizli Anahtarlar" (Secrets) bölümünü açın.
5.  **"Yeni gizli anahtar ekle"** deyin ve şu bilgileri girin:
    - **Name:** `HF_TOKEN`
    - **Value:** Az önce kopyaladığınız Hugging Face token'ınızı buraya yapıştırın.
6.  Anahtarı kaydedin. Bu sayede token'ınız kod içinde görünmez ve güvende kalır.

### Adım 3: Hücreleri Sırasıyla Çalıştırın
Not defterindeki kod hücrelerini yukarıdan aşağıya doğru, her birinin solundaki **oynat (▶️) simgesine** basarak çalıştırın.

- **Hücre 1: Kurulum:** Gerekli kütüphaneleri (`diffusers`, `torch` vb.) kurar.
- **Hücre 2: Modeli Yükleme:** Stable Diffusion v1.5 modelini indirir ve GPU'ya taşır. (Bu işlem birkaç dakika sürebilir).
- **Hücre 3: Görseli Üretme:** `prompt` ve `negative_prompt` alanlarını doldurarak hayalinizdeki görseli yaratın!

## ✨ Örnek Çıktı

![Büyücü şapkalı sevimli British Shorthair kedisi](https://github.com/Mervecaliskann/stable-diffusion-colab-guide/blob/main/indir%20(4).png?raw=true)
**Prompt:** `photo of a beautiful British shorthair cat wearing a tiny wizard hat, magical library in the background`

## 🎨 Sıra Sizde!
Artık fırça sizin elinizde! 3. hücredeki `prompt` ve `negative_prompt` metinlerini değiştirerek kendi yaratıcılığınızı keşfedin. Hayal gücünüzün sınırlarını zorlayın!


# Stable Diffusion on Google Colab: Generate Your First AI Image

This repository contains a step-by-step guide on how to run **Stable Diffusion**, a revolutionary text-to-image model, on **Google Colab**. Create your own AI-powered art without needing a powerful computer—all you need is your browser!

## 🚀 What You'll Learn
- How to get an API token from Hugging Face.
- How to activate the free T4 GPU in Google Colab.
- How to securely store your API key using Colab's "Secrets" feature.
- How to load the Stable Diffusion v1.5 model using the `diffusers` library.
- How to generate images from your imagination by writing custom `prompt` and `negative_prompt` texts.

## 🛠️ Prerequisites
1.  **Google Account**: Required to use Google Colab.
2.  **Hugging Face Account**: Required to get a free API token to download the model.

## 📝 Setup and Usage

You can generate your image in just 3 simple steps.

### Step 1: Get Your Hugging Face Token
You need a free token from Hugging Face to download the model.
1.  Go to the [Hugging Face website](https://huggingface.co/join) and create an account.
2.  Navigate to your profile: **Profile > Settings > Access Tokens**.
3.  Click the **"New token"** button and give it a name. The **`Read`** role is sufficient.
4.  Copy the generated token (it starts with `hf_...`).

### Step 2: Configure Google Colab
1.  Open the notebook by clicking the **"Open In Colab"** badge above.
2.  **CRUCIAL STEP:** In the menu, go to **Runtime > Change runtime type**.
3.  In the pop-up window, select **T4 GPU** as the "Hardware accelerator" and save.
4.  In the left sidebar, click the **key icon (🔑)** to open the "Secrets" tab.
5.  Click **"Add a new secret"** and enter the following:
    - **Name:** `HF_TOKEN`
    - **Value:** Paste your Hugging Face token here.
6.  Save the secret. This keeps your token secure and out of your code.

### Step 3: Run the Cells in Order
Run the code cells in the notebook from top to bottom by clicking the **play (▶️) icon** to the left of each cell.

- **Cell 1: Setup:** Installs the necessary libraries (`diffusers`, `torch`, etc.).
- **Cell 2: Load the Model:** Downloads the Stable Diffusion v1.5 model and moves it to the GPU. (This may take a few minutes).
- **Cell 3: Generate the Image:** Create your dream image by filling in the `prompt` and `negative_prompt` fields!

## ✨ Example Output

An example image generated using the following prompt

![British shorthair cat](https://github.com/Mervecaliskann/stable-diffusion-colab-guide/blob/main/indir%20(4).png?raw=true)

**Prompt:** `photo of a beautiful British shorthair cat wearing a tiny wizard hat, magical library in the background`


## 🎨 Now It's Your Turn!
The brush is in your hands! Explore your creativity by changing the `prompt` and `negative_prompt` texts in the third cell. Push the limits of your imagination!
