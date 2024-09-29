---
jupyter:
  colab:
  kernelspec:
    display_name: Python 3
    name: python3
  language_info:
    name: python
  nbformat: 4
  nbformat_minor: 0
---

::: {.cell .markdown id="uPTbzaf8Aly2"}
# **Tugas Pertemuan 2 - Visualisasi Data dan Informasi**

*Key Principles*

------------------------------------------------------------------------

**Nama : Ima Alifah Izati Zalfa**
**NIM : 121450140**
**Kelas : RA**
:::

::: {.cell .markdown id="R1_wj1jLBDv3"}
Berdasarkan pada prinsip-prinsip (4 prinsip) dalam pengembangan
visualisasi data, maka: cari bentuk/contoh visualisais yang termasuk
dalam Bad dan Good category visualisasi (masing-masing 2 contoh) dan
berikan alasan berdasarkan 4 prinsip mengapa masuk dalam Bad dan Good
visualisasi
:::

::: {.cell .markdown id="wTLFmREz_Ooa"}
## **Contoh Visualisasi yang Buruk (Bad Visualizations)**
:::

::: {.cell .markdown id="DQsOGluE_S4p"}
### **1. Pie Chart dengan Terlalu Banyak Kategori** {#1-pie-chart-dengan-terlalu-banyak-kategori}
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\",\"height\":428}" id="B-4juyMD-7qk" outputId="69224827-25a7-4cf4-e53d-4a5a6d4b39af"}
``` python
import matplotlib.pyplot as plt

# Contoh data pie chart buruk
labels = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']
sizes = [15, 15, 10, 10, 10, 10, 10, 10]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title('Terlalu Banyak Kategori')
plt.show()
```

::: {.output .display_data}
![](vertopal_85cd25dd2b894a128767297e4c658f8e/653143ad9324bc558ae53a3d6e02ce0e02228318.png)
:::
:::

::: {.cell .markdown id="CqYC4hIT_Jbz"}
-   Kejelasan (Clarity): Pie chart ini sulit dibaca karena terlalu
    banyak segmen kecil. Membuat pengguna sulit memahami perbedaan antar
    segmen.
-   Akurasi (Accuracy): Membandingkan ukuran segmen secara visual
    menjadi tidak akurat, terutama ketika perbedaannya kecil.
-   Efisiensi (Efficiency): Membutuhkan usaha ekstra untuk memahami apa
    yang sebenarnya ingin disampaikan.
-   Estetika (Aesthetic): Terlihat berantakan dan tidak enak dipandang
    karena warna yang terlalu banyak dan segmen yang padat.
:::

::: {.cell .markdown id="SWaaIwsb_sLy"}
### **2. 3D Bar Chart** {#2-3d-bar-chart}
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\",\"height\":438}" id="Ab5QXQJB-9jq" outputId="cf83f4cd-a1ed-4041-adcb-a509fe73f512"}
``` python
import numpy as np
from mpl_toolkits.mplot3d import Axes3D

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
xpos = [1, 2, 3, 4]
ypos = [1, 2, 3, 4]
zpos = [0, 0, 0, 0]
dx = dy = dz = [1, 2, 3, 4]
ax.bar3d(xpos, ypos, zpos, dx, dy, dz)
plt.title('3D Bar Chart yang Tidak Efisien')
plt.show()
```

::: {.output .display_data}
![](vertopal_85cd25dd2b894a128767297e4c658f8e/0d0d7203322038a55d15712ee467b32afc3cb235.png)
:::
:::

::: {.cell .markdown id="J1Ehlilz_mkr"}
-   Kejelasan (Clarity): Visualisasi 3D membuat sulit membaca
    perbandingan antar bar dengan jelas karena perspektif mengaburkan
    ukuran sebenarnya.
-   Akurasi (Accuracy): Perspektif 3D seringkali mengaburkan
    perbandingan yang akurat antar data.
-   Efisiensi (Efficiency): Pengguna perlu waktu lebih lama untuk
    memahami data yang tersaji karena distorsi 3D.
-   Estetika (Aesthetic): Meskipun terlihat menarik pada pandangan
    pertama, 3D sering kali berlebihan dan membuat visualisasi tidak
    efisien.
:::

::: {.cell .markdown id="koUfUpsj_w4h"}
## **Contoh Visualisasi yang Baik (Good Visualizations)**
:::

::: {.cell .markdown id="JWG85BMK_3km"}
### **1. Bar Chart Sederhana** {#1-bar-chart-sederhana}
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\",\"height\":452}" id="oZZs0hBU_D2N" outputId="aa9183d7-b64b-4654-8a32-e49ab1d1fb6a"}
``` python
# Contoh data bar chart yang baik
categories = ['A', 'B', 'C', 'D']
values = [10, 20, 15, 25]

plt.bar(categories, values, color='skyblue')
plt.title('Bar Chart Sederhana yang Efisien')
plt.ylabel('Jumlah')
plt.show()
```

::: {.output .display_data}
![](vertopal_85cd25dd2b894a128767297e4c658f8e/1aed90f293d20fcbd65a1ef8ce1f875f49c8bc3b.png)
:::
:::

::: {.cell .markdown id="xntOM6pL_-kb"}
-   Kejelasan (Clarity): Bar chart sederhana ini mudah dipahami dan
    menyajikan perbandingan yang jelas antar kategori.
-   Akurasi (Accuracy): Pengguna bisa dengan mudah membandingkan ukuran
    bar untuk melihat perbedaan antar kategori.
-   Efisiensi (Efficiency): Tidak perlu usaha ekstra untuk memahami
    pesan yang ingin disampaikan, visualisasi langsung memberikan
    insight.
-   Estetika (Aesthetic): Desainnya sederhana, bersih, dan efektif
:::

::: {.cell .markdown id="JyVZ0SQTAGvl"}
### **2. Line Chart dengan Data Waktu** {#2-line-chart-dengan-data-waktu}
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\",\"height\":472}" id="KTRBTD01_9iV" outputId="9077c8f2-9e21-499d-f09a-c2b58a454775"}
``` python
import numpy as np

# Contoh data line chart yang baik
waktu = np.arange(1, 11)
nilai = np.array([2, 4, 6, 8, 10, 12, 14, 16, 18, 20])

plt.plot(waktu, nilai, marker='o', color='green')
plt.title('Line Chart yang Jelas dan Akurat')
plt.xlabel('Waktu')
plt.ylabel('Nilai')
plt.show()
```

::: {.output .display_data}
![](vertopal_85cd25dd2b894a128767297e4c658f8e/d057e31b29aac2ee7f1a78f6a6d9227dad13ea74.png)
:::
:::

::: {.cell .markdown id="yJuxVK75AP2i"}
-   Kejelasan (Clarity): Line chart ini cocok untuk menunjukkan tren
    dari waktu ke waktu, sehingga mudah dipahami.
-   Akurasi (Accuracy): Visualisasi menyajikan data secara akurat dengan
    memberikan gambaran jelas tentang perubahan seiring waktu.
-   Efisiensi (Efficiency): Menyampaikan tren dengan cepat dan tepat,
    sehingga pengguna bisa langsung memahami perubahan.
-   Estetika (Aesthetic): Tampilan bersih dan minimalis yang tidak
    mengalihkan perhatian dari data utama.
:::
