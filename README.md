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
1. GİRDİ OLARAK ALINAN SESİN METİNLEŞTİRİLMESİ 
</h2>
<p>Bu aşamada işlem adımları aşağıdaki gibidir;</p>
<hr>

<ol>
 <li><strong>Veri setininim araştırılması ve elde edilmesi</strong>
  <p>     Veri seti olarak LJSpeech veri seti kullanılmıştır. LJSpeech veri seti 13.100 adet İngilizce cümle içerir. Konuşmacının cinsiyeti kadındır ve kayıtların kalitesi yüksektir. Model eğitimimiz için veri setinden rastgele seçilmiş 11790 adet veri, test için ise geri kalan 1310 veri kullanılmıştır.</p>
  
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
