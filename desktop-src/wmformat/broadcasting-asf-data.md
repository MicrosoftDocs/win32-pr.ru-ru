---
title: Трансляция данных ASF
description: Трансляция данных ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Пакет SDK для формата мультимедиа, рассылка данных ASF
- Расширенный формат систем (ASF), данные вещания
- ASF (Расширенный системный формат), широковещательная рассылка данных
- Windows Пакет SDK для формата мультимедиа, отправка данных ASF
- Расширенный системный формат (ASF), отправка данных
- ASF (Расширенный системный формат), отправка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434468"
---
# <a name="broadcasting-asf-data"></a>Трансляция данных ASF

В этом разделе описывается отправка данных ASF по сети с помощью протокола HTTP. Для отправки файлов по сети необходимо использовать объект модуля записи, поэтому прежде чем читать этот раздел, необходимо получить общее представление об этом объекте. Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).

Если вы начинаете с несжатых данных, выполните следующие действия.

1.  Создайте объект модуля записи, вызвав функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Эта функция возвращает указатель **ивмвритер** .
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Создайте объект приемника сети, вызвав функцию [**вмкреатевритернетворксинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , которая возвращает указатель **ивмвритернетворксинк** .
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Вызовите [**ивмвритернетворксинк:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) в сетевом приемнике и укажите номер порта, который нужно открыть; Например, 8080. При необходимости вызовите [**ивмвритернетворксинк:: жесостурл**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) , чтобы получить URL-адрес узла. Клиенты будут обращаться к содержимому из этого URL-адреса. Можно также вызвать метод [**ивмвритернетворксинк:: сетмаксимумклиентс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) , чтобы ограничить количество клиентов.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Подключите сетевой приемник к модулю записи, вызвав [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) в модуле записи, указав указатель на интерфейс **ивмвритернетворксинк** сетевого приемника.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Задайте профиль ASF, вызвав метод [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) объекта Writer с указателем [**ивмпрофиле**](iwmprofile.md) . Сведения о создании профиля см. в разделе [Работа с профилями](working-with-profiles.md).
6.  При необходимости укажите метаданные с помощью интерфейса [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) в модуле записи.
7.  Вызовите [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) в модуле записи.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Для каждого образца вызовите метод [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Укажите номер потока, время презентации, длительность выборки и указатель на буфер выборки. Метод **вритесампле** сжимает образцы.
9.  По завершении вызовите метод [**ивмвритер:: ендвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) в модуле записи.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Вызовите [**ивмвритерадванцед:: ремовесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) в модуле записи, чтобы отсоединить объект приемника сети.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Вызовите [**ивмвритернетворксинк:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) в сетевом приемнике, чтобы освободить порт.
    ```C++
    hr = pNetSink->Close();
    ```

    

Другим способом потоковой передачи содержимого ASF по сети является его чтение из существующего ASF-файла. Этот подход демонстрируется в примере Вмвнетврите, приведенном в пакете SDK. В дополнение к приведенным выше шагам выполните следующие действия.

1.  Создайте объект Reader и вызовите метод **Open** с именем файла.
2.  Вызовите [**ивмреадерадванцед:: сетмануалстреамселектион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) в объекте Reader со значением **true**. Это позволяет приложению считывать каждый поток в файле, включая потоки с взаимным исключением.
3.  Запросите средство чтения для интерфейса [**ивмпрофиле**](iwmprofile.md) . Этот указатель используется при вызове [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) в объекте модуля записи (шаг 5 в предыдущей процедуре).
4.  Для каждого потока, определенного в профиле, вызовите [**ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) , чтобы получить номер потока. Передайте этот номер потока в метод [**ивмреадерадванцед:: сетрецеивестреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) средства чтения. Этот метод информирует читателя о необходимости доставки сжатых образцов, а не декодирования их. Образцы будут доставляться в приложение с помощью метода обратного вызова [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) приложения.

    Необходимо получить сведения о кодека для каждого потока, который вы читаете без сжатия, и добавить его в заголовок перед рассылкой. Чтобы получить сведения о кодека, вызовите [**IWMHeaderInfo2:: жеткодеЦинфокаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) и [**IWMHeaderInfo2:: жеткодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) , чтобы перечислить кодеки, связанные с файлом, в модуле чтения. Выберите сведения о кодека, соответствующие конфигурации потока. Затем задайте сведения о кодека в средстве записи, вызвав [**IWMHeaderInfo3:: аддкодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), передав данные, полученные от модуля чтения.

5.  После настройки профиля в модуле записи вызовите [**ивмвритер:: жетинпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) в модуле записи, чтобы получить число входов. Для каждого входа вызовите [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) со значением **null**. Это указывает объекту модуля записи, что приложение будет доставлять сжатые образцы, поэтому модуль записи не должен использовать ни один кодек для сжатия данных. Перед вызовом **бегинвритинг** необходимо вызвать метод **сетинпутпропс** .
6.  При необходимости скопируйте атрибуты метаданных из модуля чтения в модуль записи
7.  Поскольку образцы из модуля чтения уже сжаты, используйте метод [**ивмвритерадванцед:: вритестреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) для записи образцов вместо метода **вритесампле** . Метод **вритестреамсампле** обходит обычные процедуры сжатия объекта модуля записи.
8.  Когда модуль чтения достигнет конца файла, он отправляет \_ приложению уведомление ВМТ EOF.

Кроме того, приложение должно запрашивать часы на объекте модуля чтения, чтобы средство чтения запрашивает данные из файла как можно быстрее. Для этого вызовите метод [**ивмреадерадванцед:: сетусерпровидедклокк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) в средстве чтения со значением **true**. После того как модуль чтения отправит \_ уведомление Started ВМТ, вызовите [**ивмреадерадванцед::D еливертиме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) и укажите интервал времени, который должен доставлять модуль чтения. После того, как модуль чтения прочитает этот интервал времени, он вызывает метод обратного вызова [**ивмреадеркаллбаккадванцед:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) приложения. Приложение должно вызвать **деливертиме** еще раз для чтения следующего интервала времени. Например, для чтения из файла с интервалом в одну секунду:


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Отправка данных ASF по сети**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Работа с приемниками модуля записи**](working-with-writer-sinks.md)
</dt> </dl>

 

 




