# XAI metode za klasifikaciju EKG spektrograma

Primjena metoda objašnjivosti (Grad-CAM, LIME, SHAP, Integrated Gradients) na CNN model za 
klasifikaciju EKG signala.

## Opis projekta
Projekat se bavi primjenom metoda objašnjive vještačke inteligencije (XAI) na konvolucijsku neuronsku mrežu koja klasifikuje EKG signale. Nad EKG signalima urađena je kratkotrajna Fourierova transformacija (STFT), te su dobijeni spektrogrami signala od interesa, koji su korišteni kao ulazni podaci za CNN model. Urađen je fine-tuning pretrenirane ResNet50 mreže za klasifikaciju spektrograma u četiri klase: normalan ritam, atrijalna fibrilacija, ostali ritmovi i šum. Nad tako dobijenim CNN modelom urađena je analiza primjenom XAI metoda Grad-CAM, LIME i Integrated Gradients, sa ciljem ispitivanja koje regije spektrograma model smatra relevantnim za donošenje odluke.


## Korištena baza podataka
The PhysioNet/Computing in Cardiology Challenge 2017
Link za preuzimanje: https://physionet.org/content/challenge-2017/1.0.0/

## Struktura projekta
xai-ekg-projekat/

├── README.md

├── kodovi_final/

│   ├── predobrada_final.ipynb

│   └── xai_poredjenje_final.ipynb

├── primjeri/

│   ├── PRIMJER1_ispravno.png

│   ├── PRIMJER2_ispravno.png

│   ├── PRIMJER1_pogresno.png

│   └── PRIMJER2_pogresno.png

├── izvjestaj/

│   └── UDOS_midterm3_IrmaSaric.pdf

│   └── XAI_prezentacija.pptx

│   └── NOTE.txt

└── .gitignore

## Instalacija

pip install torch torchvision scipy matplotlib numpy pandas grad-cam

## Pokretanje
1. Skinuti bazu sa PhysioNet linka i otpakovati u folder 'training2017/'
2. Pokrenuti'kodovi_final/predobrada_final.ipynb' (generiše spektrograme, generise database, radi fine-tuning i sačuvana model)
3. Pokrenuti 'kodovi_final/xai_poredjenje_final.ipynb' (učitava sačuvani model i generiše XAI vizualizacije)


## Korištene XAI metode za implementaciju
- Grad-CAM
- LIME
- Integrated Gradients

## Autor
Irma Šarić