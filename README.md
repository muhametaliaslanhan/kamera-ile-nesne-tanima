## Kamera ile Gerçek Zamanlı Nesne Tanıma (YOLOv3 + OpenCV)

Bu Python projesi, **YOLOv3 algoritması** ve **OpenCV** kütüphanesi kullanarak bilgisayar kamerası üzerinden gerçek zamanlı olarak nesneleri tanımayı sağlar.

**YOLO (You Only Look Once)**, nesne algılama konusunda en popüler ve hızlı çalışan algoritmalardan biridir. Bu proje sayesinde webcam üzerinden görüntü alarak canlı nesne tespiti yapabilirsiniz.

---
## Gereksinimler

```bash
pip install -r requirements.txt
```

## YOLO Modellerini İndirme

Aşağıdaki dosyaları `yolo-coco/` klasörüne koymalısınız:

- [yolov3.weights](https://pjreddie.com/media/files/yolov3.weights)
- [yolov3.cfg](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg)
- [coco.names](https://github.com/pjreddie/darknet/blob/master/data/coco.names)

    Not: yolov3.weights dosyası ~248 MB büyüklüğündedir ve GitHub sınırlarını aşar. Bu nedenle .gitignore dosyası ile hariç tutulmuştur.

## Nasıl Çalıştırılır?
Gerekli kütüphaneleri yükleyin:

```bash 
pip install -r requirements.txt
```

Gerekli YOLO dosyalarını yolo-coco/ klasörüne yerleştirin.

Python dosyasını çalıştırın:

Webcam açılır ve tanımlanan nesneler ekranda kutular ve etiketlerle gösterilir.
Çıkmak için ESC tuşuna basın.

```bash
python kamera_ile_nesne_tanima.py
```

```bash
kamera-ile-nesne-tanima/
├── kamera_ile_nesne_tanima.py     # Ana Python kodu
├── yolo-coco/                     # YOLO model dosyalarının bulunduğu klasör
│   ├── yolov3.cfg
│   ├── yolov3.weights             # NOT: GitHub'a yüklenmez (çok büyük!)
│   └── coco.names
├── requirements.txt              # Gerekli kütüphaneler
├── .gitignore                    # yolov3.weights dosyasını hariç tutar
└── README.md                     # Bu belge
```

## Ekstra Bilgiler
1-Proje temel olarak cv2.dnn modülü ile YOLO modelini yükler ve her karede nesne tespiti yapar.

2-Kullanılan model COCO dataset ile eğitilmiş olduğu için; insan, bisiklet, araba, köpek, masa, sandalye gibi 80 nesne sınıfını tanıyabilir.

3-Algılanan her nesne için bir etiket ve güven skoru (confidence) gösterilir.

## İletişim
Bu proje hakkında sorularınız veya önerileriniz varsa, GitHub üzerinden issue açabilir ya da bana mesaj atabilirsiniz
