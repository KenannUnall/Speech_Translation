 # Speech Translation
<p>Projemiz konusu İngilizce dilindeki konuşmayı Türkçe’ ye çevirerek seslendirme işlemidir. Projemizin kullanım amacı gerçek zamanlı tercüme gerektiren durumlarda kullanılmasıdır. Gezi turları, ticaret vb. durumlarda büyük kolaylık sağlamaktadır. </p>
Projemiz temel mantık aşamaları sırası ile;
<hr>
<ol>
    <li>Girdi olarak alınan sesin metinleştirilmesi </li>
    <li>Metnin farklı dile çevrilmesi</li>
    <li>Çevrilen metnin seslendirilmesidir.</li>
</ol>

<h2>
 
<br>
1. GİRDİ OLARAK ALINAN SESİN METİNLEŞTİRİLMESİ 
</h2>
<p>Bu aşamada işlem adımları aşağıdaki gibidir;</p>
<hr>

<ol>
 <li><strong>Veri setininim araştırılması ve elde edilmesi</strong>
  <p>     Veri seti olarak LJSpeech veri seti kullanılmıştır. LJSpeech veri seti 13.100 adet İngilizce cümle içerir. Konuşmacının cinsiyeti kadındır ve kayıtların kalitesi yüksektir. Model eğitimimiz için veri setinden rastgele seçilmiş 11790 adet veri, test için ise geri kalan 1310 veri kullanılmıştır.</p>
  <img width="200" height="300" src="https://production-media.paperswithcode.com/datasets/LJSpeech-0000001001-0d016d5b.jpg"></img>
 </li>
 <li><strong>Veri ön işleme adımları</strong>
 <p>  Bu aşamada girdi olarak alınan ses dosyalarının çözümlendirilmesi, özellik çıkarımı vb. işlemler gerçekleştirilmiştir.</p>
  
 </li>
 <li><strong>Model oluşturulması ve eğitilmesi</strong>
 <p>     Modelin eğitilme işlemi uzun zaman alan bir aşamadır. Önemi çok fazladır. İşlem süresinin artıp azalması modelde kullanılan katman sayısına, epoch sayısına kullanılan aktivasyon fonksiyonlarına, gerekli olarak aldığı parametre vb. durumlara bağlıdır. </p>
  </li>
 <li><strong>Model test işlemi, sonuç değerlendirilmesi ve model optimizasyonu</strong>
 <p>    Bu aşama model eğitildikten sonra test verileri üzerinde nasıl sonuç verdiğine bağlı olarak modelde optimizasyon işlemleri gerçekleştirilip tekrardan eğitim süreci başlatılabilir.</p>
  </li>

</ol>
<p>Projemiz bir yapay zekâ projesi olduğundan dolayı sesin metinleştirilmesi kısmında derin öğrenme başlığı altında bulunan RNN mimarisi kullanılmıştır. </p>
<h4>RNN (Recurrent Neural Network):</h4>
<p>
RNN, tekrarlayan (döngülü) bir yapısı olan yapay sinir ağı türüdür. Bu yapay sinir ağı, bir önceki çıktının, bir sonraki adımda girdi olarak kullanılması sayesinde, zaman serileri veya sıralı veriler gibi yapısal verilerin işlenmesi için tasarlanmıştır. RNN'ler, geleneksel yapay sinir ağı modellerinin aksine, aynı ağın birden çok örneği arasında bağlantıları olan bir yapıya sahiptir. Bu bağlantılar, ağın önceki durumlarından zaman içinde bilgi akışını sağlamak için kullanılır. RNN'lerin anahtar özelliği, hafızalarının olmasıdır. Bu hafıza, ağın önceki durumlarını hatırlayarak, bir sonraki adımda gelen girdiye bağlı olarak yeni bir çıktı üretmesine olanak tanır. Bu özellik, RNN'leri zaman serileri, doğal dil işleme, konuşma tanıma gibi sıralı veriler için ideal hale getirir. RNN'ler, sıralı verileri işlemek için tasarlanmıştır ve birçok uygulama alanında kullanılır. Örneğin, zaman serileri analizi, konuşma tanıma, doğal dil işleme, hisse senedi fiyat tahmini, müzik oluşturma gibi alanlarda RNN'ler sıklıkla kullanılır.

</p>

<hr>

<p>
Projemizin temel olarak çalıştığı ses dosyaları, RNN mimarisine direkt girdi olarak verilememesinden dolayı ses dosyası ilk olarak sayısallaştırılmasına (çözümlenme işlemi) daha sonrasında ise RNN mimarisini kullanan derin öğrenme modelimize girdi olarak verilecek ses dosyası özelliklerinin çıkarılması gerekmektedir. Ses dosyalarından özellik çıkarımı işlemi STFT (Short-Time Fourier Transform) yöntemi ile yapılmıştır. STFT, uzun bir ses sinyalini küçük parçalara bölerek, her bir parçanın frekans-zaman uzayındaki özelliklerini hesaplar. Bu özellikler, spektrogram olarak adlandırılırlar ve ses dosyalarından özellik çıkarımında sıklıkla kullanılırlar. Bu aşamada birçok özellik çıkarımı yöntemi bulunmaktadır. Bunlardan bazıları;
</p>


<ol>
 <li><strong>Mel Frekans Cepstral Katsayıları (MFCC)</strong>
  <p>MFCC, insan kulağının işitme özellikleriyle uyumlu bir şekilde, ses sinyallerinin özelliklerini tanımlayan bir yöntemdir. MFCC, ses sinyallerinin frekans-zaman uzayındaki özelliklerini çıkararak, bir dizi katsayıya dönüştürür. Bu katsayılar, ses dosyalarının tanınması, sınıflandırılması ve benzer dosyaların bulunması için kullanılabilir.</p>
  
 </li>
 <li><strong>Perceptual Linear Predictive (PLP)</strong>
 <p>  PLP, ses sinyallerinin özelliklerini çıkarırken, insan işitme sistemine uygun bir şekilde özellikleri seçer. Bu yöntem, insan kulağının işitme özelliklerine uyumlu olarak, ses sinyallerinin özelliklerini tanımlayan bir yöntemdir. PLP, konuşma tanıma ve ses sınıflandırması gibi uygulamalarda sıklıkla kullanılır.</p>
  
 </li>
 <li><strong>Mel-Spektrogram</strong>
 <p> Mel-spektrogram, ses sinyallerinin frekans-zaman uzayında temsil edilmesi için kullanılan bir yöntemdir. Bu yöntem, ses sinyallerinin spektrogramlarını,insan kulağının işitme özelliklerine daha uygun bir şekle dönüştürür. Mel-spektrogram, STFT yöntemi ile elde edilen spektrogramun frekans ölçeğini insan kulağının işitme özelliklerine daha uygun bir şekilde dönüştürür. Bu sayede, insan kulağı için daha anlaşılır bir spektrogram elde edilir. </p>
  </li>
</ol>

<h2>
 <br>
2. METNİN FARKLI DİLE ÇEVRİLMESİ
</h2>
<p>Metnin farklı dile dönüştürülme işleminde ise “googletrans” kütüphanesinin altında bulunan “Translator” sınıfı kullanılmıştır. Bu kısımda derin öğrenmeden çıkan tahmin değeri, translator sınıfından oluşturduğumuz nesnenin translate fonksiyonuna girdi olarak verilerek çeviri işlemi gerçekleştirilmiştir. </p>




