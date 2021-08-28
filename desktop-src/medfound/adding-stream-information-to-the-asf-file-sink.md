---
description: Сведения о добавлении потоковых данных в приемник файлов ASF, который приложение может использовать для архивации данных ASF Media в файл.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Добавление потоковой информации в приемник файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0273f6080293803db7fa7451460e8f8d7700c5e405b9ed09d8d35e384abc8ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975043"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Добавление потоковой информации в приемник файлов ASF

Приемник ASF-файлов — это реализация [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл. Сведения об объектной модели приемников ASF Media и общем использовании см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).

После создания экземпляра приемника файла его необходимо настроить перед созданием топологии. Приемнику файла необходимо узнать о потоках в выходном файле, сведениях о режиме кодирования и метаданных. В этом разделе описывается процесс добавления потока в приемник файла.

-   [добавление Потоки в приемник файлов ASF](#adding-streams-in-the-asf-file-sink)
-   [Перечисление приемников потоков](#enumerating-stream-sinks)
-   [Связанные темы](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>добавление Потоки в приемник файлов ASF

Приемник файла должен иметь представление о потоках вывода и их свойствах, чтобы они могли соответствующим образом формировать выходные образцы и добавлять их в выходной файл ASF. Эти параметры записываются в окончательный объект заголовка ASF.

Чтобы задать сведения о потоке, необходимо иметь ссылку на объект ASF Контентинфо приемника файлов. Дополнительные сведения см. [в разделе Создание приемника файлов ASF](creating-the-asf-file-sink.md).

Следующая процедура описывает общие шаги настройки потока с помощью объекта профиля ASF.

**Настройка потоковой информации в приемнике файлов ASF**

1.  Создайте объект профиля ASF, вызвав [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Для каждого потока в выходном файле создайте тип мультимедиа для целевого потока, добавляемого в приемник файла. тип мультимедиа должен быть совместим с типами выходных данных, которые поддерживаются кодировщиками Windows media.

    дополнительные сведения о добавлении в профиль звуковых потоков см. в разделе создание аудио Потоки для кодирования ASF.

    сведения о добавлении потоков видео в профиль см. в разделе создание видео Потоки для кодирования ASF.

3.  Создайте потоки на основе типов носителей, созданных на шаге 2, вызвав [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Назначьте номер потока для вновь созданного потока, вызвав указатель интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) , полученный на шаге 3.
5.  При необходимости настройте поток со следующими сведениями:
    -   Параметры сегмента с утечкой путем установки атрибутов: [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) или [**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Расширение полезных данных — взаимное исключение путем вызова методов [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .
6.  При необходимости задайте размер пакета данных для профиля, установив атрибуты [**MF \_ асфпрофиле \_ минпаккетсизе**](mf-asfprofile-minpacketsize-attribute.md) и [**MF \_ асфпрофиле \_ макспаккетсизе**](mf-asfprofile-maxpacketsize-attribute.md) . Профиль ASF предоставляет интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , к которому приложение может получить ссылку путем вызова **Имфасфпрофиле:: QueryInterface**.
7.  Задайте сведения о кодировке для потока в приемнике файла. Описывается в разделе [Установка свойств в приемнике файла](setting-properties-in-the-file-sink.md).
8.  Добавьте поток в профиль, вызвав [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Свяжите профиль с объектом Контентинфо, вызвав [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Чтобы изменить существующий поток, приложение может получить ссылку на интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) потока и перенастроить его в соответствии с требованиями. Чтобы добавить или удалить потоки, приложение должно вызвать [**имфасфпрофиле:: ремовестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Чтобы применить эти изменения, изменить потоковые изменения или удалить, необходимо снова задать профиль в объекте Контентинфо. При этом существующий профиль, уже связанный с объектом Контентинфо, перезаписывается.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Перечисление приемников потоков

Для каждого потока в профиле, о котором известно объект Контентинфо, приемник файлов ASF создает и добавляет приемник потока, который содержит все свойства закодированного потока. Приемник файлов ASF предназначен для хранения фиксированных потоков. Это означает, что нельзя добавлять или удалять потоки путем вызова [**имфмедиасинк:: аддстреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) или [**Имфмедиасинк:: ремовестреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Эти вызовы в приемнике файлов завершаются с \_ \_ \_ фиксированным кодом ошибки MF E стреамсинкс. Добавление или удаление потоков в профиле не приводит к автоматическому добавлению или удалению приемников потоков в приемнике файлов. Необходимо удалить существующий экземпляр файла и повторно создать его со сведениями о новом потоке, если потоки в профиле были изменены.

Следующая процедура обобщает общие шаги для перечисления приемников потоков в приемнике файлов ASF.

**Перечисление приемников потоков**

1.  Вызовите [**имфмедиасинк:: жетстреамсинккаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) , чтобы получить общее число приемников потоков в приемнике файлов ASF.
2.  Пройдите через приемники потоков, Энг получить ссылку на интерфейс [**жетстреамсинкбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) приемника потока.

    -или-

    Вызовите метод [**имфмедиасинк:: жетстреамсинкбид**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) , чтобы получить приемник потока, указав номер потока. Каждый приемник потока определяется номером потока, установленным при создании потока в профиле.

При создании частичной топологии для кодирования файла мультимедиа необходимо добавить приемник файла в топологию в качестве узла выходной топологии. Это можно сделать, указав каждый приемник Steam в приемнике файлов или установив объект активации приемника файла и идентификаторы приемника потока. Дополнительные сведения и пример кода см. в разделе [Создание выходных узлов](creating-output-nodes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Приемники мультимедиа ASF](asf-media-sinks.md)
</dt> <dt>

[Поддержка ASF в Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



