# Cloud Classification App: A AIoT application to classify cloud type

Author name: Satria Mitra Utama<br> 
Github repo: https://github.com/satria-mitra/CASA0018-Cloud-Classification <br> 
Video presentation: youtube <br> 

## Introduction
Clouds play a crucial role in our daily lives, affecting everything from the weather to the climate. Cloud types have an impact of Earth's energy balance (Hartmann, L, D., Ockert-Bell, M. and Michelsen, L, M., 1992) and global radiation.  (Chen, T., Rossow, B, W. and Zhang, Y., 2000). Thus, understanding cloud is an important task in environmental monitoring and meteorology to improve weather prediction and assessing climate models. Thus, understanding cloud is an important task in environmental monitoring and meteorology to improve weather prediction and assessing climate models. This project will explore the use of Deep Learning models to automatically classify and identify different types of clouds based on ground-based cloud images. 

Luke Howard in 1802 proposed cloud classification into three types, Cirrus, Cumulus & Stratus. And then World Meteorological Organizations (WMO) extended Luke Howard's idea to group cloud types into three levels, namely low level (CL), middle level (CM), and high level (CH). Each of these groups is further divided into 10 cloud types based on the International Cloud Atlas Weather Meteorological Organizations. (World Meteorological Organizations, 1975). This project will only focus on the three types of cloud based on height level with additional of Contrail.

<p align="center" width="100%">
    <img width="60%" src="./assets/pictures/bom.jpeg"> 
</p>


## Research Question
Can cloud be classified on real-time event based on the images input by leveraging a deep learning model on an edge device (like mobilephone) ?

## Application Overview
This project will try to classify cloud into 3 types of cloud plus additional of contrail, the condensation trail that is left behind by a passing jet plane. The goal of this project is to develop a deep learning model that can accurately classify different types of clouds based on ground-based cloud images. The image input is a picture taken on the smartphone by using a Flutter based application with Tensorflow library installed. Tensorflow model will run on the Flutter app, and detect and classify image on the go. Deep learning model is built, trained and converted to the Tensorflow lite model in the Google Colab environment. 




## Data
Initially, CCSN dataset (Cirrus cumulus stratus nimbus (CCSN) database, 2021) which classify cloud into 10 types + 1 contrail is being collected. For simplicity and as a prove concet of Deep Learning, this dataset is modified, merging some cloud types into 3 types of cloud based on their height level with contrail picture is added. A little inspection was done to check and remove for dirty picture, where there is too much additional 'information' on the cloud picture such as building or landscape. This cleaning step is crucial as the project would like to deploy a deep learning model in the real condition.

Regarding the total pictures for the 4 categories, there is a data imbalance between cloud images and contrail images. There are 900 images of each cloud type and fewer than 300 contrail images when this dataset was first downloaded. For this reason, I looked for additional datasets from the image repository, such as flickr.com. By using code from [pyimgdata](https://github.com/jeffheaton/pyimgdata) (Heaton, 2020) which was developed by [Jeff Heaton](https://www.heatonresearch.com/), I can bulk download images from Flickr by using spesific keyword and save the images to my Google Colab environment. The final datasets contain 600 pictures of each type of cloud and contrail, so it was 2400 images in total. The data was further split into 60% (360*4 images) for the training dataset, 20% (120*4 images) for validation and 20% (120*4 images) for testing.



## Model
Experimen dilakukan untuk mendapatkan akurasi terbaik dari sesi pengetesan. 3 model berdasarkan Keras framework dikembangkan untuk mengetahui hasil terbaik untuk mengklasifikasikan awan. The first one is Keras sequential model, the second one is Transfer Learning, and the last one is Fine-tuning the pre-trained model. Dari hasil percobaan yang dijabarkan pada table dibawah terlihat bahwa mempunyai performa terbaik dari segi akurasi 

## Experiments
Eksperimen difokuskan pada model xxx yang terbukti memiliki hasil akurasi terbaik pada sesi pengetesan sebelumnya. xxx parameters yang terlihat pada table xx diuji coba untuk mengetahui lebih jauh performa model xxx. Experimen berfokus kepada optimasi jumlah epoh, batch size dan jenis optimizer
- Optimizer : Percobaan pertama adalah mencoba 3 jneis optimizer dengan learning rate dan batch size fixed as 0.001 dan 32. Aku mengevaluasi optimizer berdasarkan skor akurasi pada validasi tes. Table xx menunjukan skor akurasi yang berbeda untuk setiap macam optimizers. Terlihat bahwa xxxx optimiser menunjukan hasil akurasi terbaik
- Learning rate
- Batch Size

Setelah experiment selesai dilakukan, parameters yang dipilih adalah

## Testing on real-world
Aku melakukan percobaan dengan mendeploy model Tensor Flow pada mobile phone berbasis aplikasi Flutter. Ada beberapa alasan kenapa mobile phone dipilih ketimbang microcontroller. Pertama, aplikasi mobile yang terintegrasi dengan Deep Learning model dapat dikembangkan untuk dapat mengambil gambar atau menggunakan foto dari internet untuk membedakan tipe awan secara cepat. Pengguna dapat langsung mengeluarkan mobile phonenya dan mengarahkan ke langit untuk dapat mengetahui jenis awan yang tidak dikenalinya secara langsung. Kedua, mengingat kompleksitas dari image classification model, mobile phone mempunyai keunggulan dalam hal penyimpanan model yang kompleks, rapid in inference dan kemampuan foto resolusi tinggi. Eksperimen dunia nyata menunjukan bahwa aplikasi dapat bekerjda pada siang hari . Current

## Results and Observations
1. Data
2. d
3. 
## Bibliography
1. Cirrus cumulus stratus nimbus (CCSN) database (no date). Available at: https://doi.org/10.7910/DVN/CADDPD.
2. Chen, T., Rossow, B, W. and Zhang, Y. (2000) "Radiative effects of cloud-type variations," , 13(1),p. 264-286. Available at: https://doi.org/10.1175/1520-0442(2000)013<0264:reoctv>2.0.co;2.
3. Heaton, J. (2020) Pyimgdata, GitHub. Available at: https://github.com/jeffheaton/pyimgdata (Accessed: 23 April 2024). 
4. Hartmann, L, D., Ockert-Bell, M. and Michelsen, L, M. (1992) "The Effect of Cloud Type on Earth's Energy Balance: Global Analysis," American Meteorological Society, 5(11),p. 1281-1304. Available at: https://doi.org/10.1175/1520-0442(1992)005<1281:teocto>2.0.co;2.
5. World Meteorological Organization, 1975. Manual on the Observation of Clouds and Other Meteors. Secretariat of the World Meteorological Organization.
6. 


----

## Declaration of Authorship

I, SATRIA MITRA UTAMA, confirm that the work presented in this assessment is my own. Where information has been derived from other sources, I confirm that this has been indicated in the work.



*Satria Mitra Utama*

25 April 2024
