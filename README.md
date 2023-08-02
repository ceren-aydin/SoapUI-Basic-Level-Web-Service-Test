# SoapUI-Basic-Level-Web-Service-Test

Bu projede SoapUI ile SOAP Web Servis testi yapılmıştır. Bu test için http://www.dneonline.com/calculator.asmx servisi üzerinden 3 ayrı işlem yapılmıştır. İşlemler sırası ile; request atılması, sonrasında TestSuite oluşturulup birden fazla request atılması, son olarak response'tan alınan verinin başka bir fonksiyona request olarak verilmesi.

SoapUI, Web Servislerini test etmek için kullanılan bir araçtır; bunlar SOAP Web Servisleri olabileceği gibi RESTful Web Servisleri veya HTTP tabanlı servisler de olabilir. Fonksiyonel Test, Performans Testi, Birlikte Çalışabilirlik Testi, Regresyon Testi ve çok daha fazlası yapılabilir.



https://github.com/ceren-aydin/SoapUI-Basic-Level-Web-Service-Test/assets/74559017/f8109743-2f88-4001-ae9f-92ec087701cf



# Proje Adımları

**Request atılması :** Yeni bir SOAP projesi oluşturulur. Add ve Multiply bölümünden request atılır. Bu request'in sonucu olarak response alınır.

**TestSuite oluşturulması :** İşlemlerin senaryo şeklinde art arda gerçekleşmesi için TestSuite oluşturulur. Burada add ve multiply eklenir, TestSuite sayesinde bu işlemler gruplandırılmış olur. TestSuit'in çalıştırılmasıyla beraber, bu iki işlem de gerçekleşir.

**"Property Transfer test adımı" sayesinde response içerisindeki değerin bir sonraki request içerisine eklenmesi :** Add request sonucu alınan response'un Multiply'a verilmesi için property transfer oluşturulur. Envelope değerleri alınır ve Add'in response'u _//*:AddResult_ XPath'i eklenerek alınır, bunun Multiply'ın girdisi olması için _//*:intA_ XPath'i verilir. TestSuite çalıştırıldıktan sonra Multiply'a bakıldığında, Add'in response'unun Multiply'ın girdisi olduğu görülür.
