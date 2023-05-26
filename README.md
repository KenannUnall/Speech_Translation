 # Speech Translation
## Giriş
Speech synthesis ve sesli tercüme, iletişimde büyük bir öneme sahiptir. Bu teknolojiler, farklı dilleri konuşan insanlar arasındaki engelleri kaldırmak için kullanılabilirler. Özellikle küreselleşen dünyada, farklı kültürler arasındaki iletişim giderek önem kazanmaktadır. Speech synthesis ve sesli tercüme, bu iletişimi kolaylaştırarak iş dünyasında, turizm sektöründe ve diğer birçok alanda büyük bir role sahip olabilirler. Ayrıca, öğrenme ve eğitim gibi alanlarda da kullanılabilirler, özellikle yabancı dillerin öğreniminde büyük bir yardımcı olabilirler.

##- Özellik Tabanlı Yaklaşımlar:
Heartbeat seslerinin sınıflandırılmasında yaygın olarak kullanılan bir yöntem, özellik tabanlı yaklaşımlardır. Bu yaklaşımlar, heartbeat seslerini özelliklerine göre sınıflandırmayı amaçlar. Mel Frekanslı Cepstral Katsayıları (MFCC) ve Mel Spektrogramları, heartbeat seslerinin zaman ve frekans özelliklerini görselleştiren grafikler olarak kullanılmaktadır. Bu grafikler, ses dosyalarından elde edilen özelliklerin bir temsili olarak kullanılır ve daha sonra sınıflandırma için kullanılan makine öğrenmesi yöntemlerine beslenir.

## -Derin Öğrenme Modelleri:
Son yıllarda, derin öğrenme modelleri, heartbeat seslerinin sınıflandırılmasında başarılı sonuçlar vermektedir. Özellikle, LSTM (Long Short-Term Memory) modelleri, zaman serileri için uygun bir derin öğrenme modeli olarak kullanılmaktadır. LSTM modelleri, heartbeat seslerinin zamansal özelliklerini yakalamak için etkili bir şekilde çalışır. Bu modeller, önceden eğitilmiş veri setleri üzerinde eğitilerek heartbeat seslerinin sınıflandırılmasında yüksek doğruluk oranları elde edebilir.
## -Veri Setlerinin Önemi:
Heartbeat seslerinin sınıflandırılmasında kullanılan veri setlerinin önemi büyüktür. Özellikle, büyük ve çeşitli veri setleri, modelin performansını artırmak ve daha doğru sonuçlar elde etmek için önemlidir. Bu nedenle, çalışmalarda geniş veri setlerinin kullanımına önem verilmektedir. Veri setleri, sağlıklı bireylerin ve kalp hastalığı olan bireylerin heartbeat seslerini içermelidir.
## -Literatürde öne çıkan çalışmalar
Heartbeat seslerinin sınıflandırılması, kalp hastalıklarının teşhisinde önemli bir rol oynar. Bu nedenle, son yıllarda, heartbeat seslerinin otomatik olarak sınıflandırılması için birçok çalışma yapılmıştır. Birçok çalışma, heartbeat seslerini özelliklerine göre sınıflandırmayı amaçlamaktadır. Özellikle, Mel Frekanslı Cepstral Katsayıları (MFCC) ve Mel Spektrogramları, heartbeat seslerinin sınıflandırılmasında yaygın olarak kullanılan özelliklerdir. Bu özellikler, ses dosyalarının zaman ve frekans özelliklerini görselleştiren grafiklerdir ve daha sonra otomatik olarak sınıflandırma için kullanılırlar.Sınıflandırma için çeşitli makine öğrenmesi yöntemleri kullanılmaktadır. LSTM (Long Short-Term Memory) modelleri, özellikle zaman serileri için uygun bir derin öğrenme modeli olarak kullanılır ve son yıllarda heartbeat seslerinin sınıflandırılmasında da başarılı sonuçlar vermiştir. Çalışmalarda,  heartbeat seslerinin sınıflandırılmasında kullanılan veri setlerinin önemi üzerinde durmaktadır. Özellikle, büyük ve çeşitli veri setleri, modelin performansını arttırmaya yardımcı olur ve daha doğru sonuçlar verir.

> BHeart sound classification using wavelet transform and incremental self-organizing map
> Yazarlar: Zümray Dokur,  Tamer Ölmez
> Heartbeat sound dataset
> discrete wavelet transform (DWT), Wavelet transform feature sellection                         
> Artificial neural networks(ANN), incremental self-organizing map (ISOM) sınıflandırma
> ncremental self-organizing map (ISOM)  0.79 AUC
> Frequency Cepstral Coefficient (MFCC) 0.68 AUC

> Deep attention-based neural networks for explainable heart sound classification
> Yazarlar: Fengquan Dong , Zhenyu Dai , Wolfgang Nejdl, Yoshiharu Yamamoto , Björn W. Schuller 
> Heart Sounds Shenzhen (HSS) database 
>  Log-mel spectrom feature sellection Recurrent Neural Networks (RNNs) sınıflandırma
>  CNN 0.73 AUC
> LSTM-RNN 0.60 AUC
> GRU-RNN 0.70

> Heartbeat sound classification using Mel-frequency cepstral coefficients and deep convolutional neural network
> Yazarlar: Shamik Tiwari,  Varun Sapra, Anurag Jain
> Heartbeat sound dataset
> MFCC feature extraction, Fourier transform (FT) ,  discrete cosine transform (DCT) feature sellection
> Convolutional Neural Network (CNN) sınıflandırma
> CNN 0.91 AUC  

## -Kullanılan Veri Seti :
Bu projde kullanılan veri seti Kaggle platformu üzerinde bulunan açık kaynaklı bir veri seti olan "Heartbeat Sounds" veri setidir. Bu veri seti, normal ve anormal kalp atışlarını içeren stetoskop ses kayıtlarından oluşmaktadır. Veri seti, normal kalp atışları ve anormal kalp atışları olarak iki sınıfa ayrılmıştır.

Normal kalp atışları sınıfı, sağlıklı bireylerin kalp atışı ses kayıtlarını içermektedir. Bu kayıtlar, tipik olarak düzenli ve ritmik kalp atışlarını temsil eder. Normal kalp atışları sınıfı, kalp sağlığının normal işleyişini yansıtmak üzere örnekler içermektedir.

Anormal kalp atışları sınıfı ise çeşitli anormallikleri temsil etmek üzere oluşturulmuştur. Bu sınıf, farklı hastalıklardan muzdarip bireylerin kalp atışı ses kayıtlarını içerir. Örneğin, üflemeler, galoplar ve tıklamalar gibi farklı tiplerde kalp atışları bu sınıfın içerisindedir. Anormal kalp atışları, genellikle düzensizlikler veya kalp rahatsızlıklarının belirtilerini yansıtan özelliklere sahiptir.

Toplamda, veri seti 500 kayıttan oluşmaktadır. Bu kayıtlar, önde gelen tıbbi kuruluşlar tarafından kabul edilen standartlar doğrultusunda toplanmıştır. Veri seti, farklı hastalıklardan muzdarip olan hastalardan elde edilen stetoskop ses kayıtlarını içerir. 
Bu veri seti, kalp atışlarının anormalliklerini sınıflandırmak için kullanılan aracın eğitiminde ve değerlendirilmesinde kullanılmıştır. Veri setinin çeşitliliği ve kalitesi, aracın doğruluk oranını ve performansını etkileyen önemli faktörlerdir. Bu nedenle, veri setinin titizlikle toplanması ve temsil edilen sınıfların dengeli bir şekilde dağıtılması sağlanmıştır.<br> **Veri setinin linki yanda verilmiştir:**
<a href = "https://www.kaggle.com/datasets/kinguistics/heartbeat-sounds">Heartbeat Sounds Dataset</a>

## -Yöntem:

Bu projede, MFCC (Mel-Frequency Cepstral Coefficients) ve LSTM (Long Short-Term Memory) modeli kullanılarak kalp atışlarının sınıflandırılması gerçekleştirilir.

### CMFCC Özellik Çıkarımı:
Stetoskop ses kayıtlarından özelliklerin çıkarılması için Librosa kütüphanesi kullanılır. Librosa, ses işleme için kullanılan bir Python kütüphanesidir ve MFCC hesaplamalarını yapmak için uygun fonksiyonlara sahiptir.
İlk adımda, stetoskop ses kayıtları önceden işlenir. Kayıtlar, zaman serileri olarak temsil edilir ve üzerinde MFCC hesaplamaları yapılabilir hale getirilir. Bu adım, ses kayıtlarının frekans spektrumlarını temsil eden mel spektrogramlarını elde etmek için gerçekleştirilir. <br>
<div align="center">
	<img src= "https://pub.mdpi-res.com/sensors/sensors-22-01521/article_deploy/html/images/sensors-22-01521-g003-550.jpg?1645001655">
</div>

### -LSTM Modeli:
LSTM (Long Short-Term Memory), zaman serileri analizi için kullanılan bir derin öğrenme modelidir. LSTM, birçok katmandan oluşan bir sinir ağı yapısına sahiptir ve her bir katman, bir önceki katmandan aldığı çıktıları bir sonraki katmana aktarır.
Mel spektrogramları, LSTM modeline giriş olarak verilir. Model, bu spektrogramları kullanarak stetoskop ses kayıtlarını normal veya anormal kalp atışlarına göre sınıflandırmayı öğrenir.
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/LSTM_Cell.svg/1920px-LSTM_Cell.svg.png">
###- Eğitim ve Değerlendirme:
Veri seti, eğitim ve test kümelerine ayrılır. Eğitim kümesi, modelin öğrenmesi için kullanılırken, test kümesi, eğitilen modelin performansını değerlendirmek için kullanılır.
Eğitim sürecinde, LSTM modeli, eğitim kümesindeki örnekleri kullanarak ağırlıklarını ve parametrelerini ayarlar. Bu adım, modelin veriler arasındaki örüntüleri anlamasını sağlar.

Değerlendirme sürecinde, eğitilen model, test kümesindeki örnekleri sınıflandırır ve tahminlerini gerçek etiketlerle karşılaştırır. Bu adım, modelin doğruluğunu, hassasiyetini ve diğer performans metriklerini değerlendirmek için kullanılır.

Sonuç olarak, MFCC özellikleri ve LSTM modeli kullanılarak kalp atışlarının sınıflandırılması gerçekleştirilir. Bu yöntem, stetoskop ses kayıtlarındaki anormallikleri tespit etmek ve kalp hastalıklarının teşhisine yardımcı olmak için kullanılan bir araç sağlar.
