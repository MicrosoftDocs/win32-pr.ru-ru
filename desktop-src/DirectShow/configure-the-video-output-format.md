---
description: Настройка формата вывода видео
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Настройка формата вывода видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556989"
---
# <a name="configure-the-video-output-format"></a>Настройка формата вывода видео

> [!Note]  
> Функциональные возможности, описанные в этом разделе, являются устаревшими. Чтобы настроить выходной формат устройства записи, приложение должно использовать структуру [**\_ \_ типа данных AM Media**](/windows/win32/api/strmif/ns-strmif-am_media_type) , возвращенную функцией [**иамстреамконфиг::-Format**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) в параметре *ПЛТ* .

 

Устройство записи может поддерживать диапазон выходных форматов. Например, устройство может поддерживать 16-разрядный RGB, 32-разрядный RGB и ЮИВ. В каждом из этих форматов устройство может поддерживать диапазон размеров кадров.

В устройстве WDM интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) используется для сообщения о том, какие форматы поддерживает устройство, и для задания формата. (Для устаревших устройств VFW используйте диалоговое окно VFW в формате видео, как описано в разделе [Отображение диалоговых окон VFW Capture](display-vfw-capture-dialog-boxes.md).) Интерфейс **иамстреамконфиг** предоставляется на ПИН-коде записи фильтра записи, предварительный просмотр ПИН-кода или и то, и другое. Чтобы получить указатель интерфейса, используйте метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) :


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



Устройство имеет список поддерживаемых типов мультимедиа. Для каждого типа носителя устройство также предоставляет набор возможностей. К ним относятся диапазон размеров кадров, доступных для этого формата, то, насколько хорошо устройство может растянуть или сжать изображение, а также диапазон частот кадров.

Чтобы получить количество типов мультимедиа, вызовите метод [**иамстреамконфиг:: жетнумберофкапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) . Метод возвращает два значения:

-   Число типов мультимедиа.
-   Размер структуры, содержащей сведения о возможностях.

Значение размера необходимо, так как интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) используется как для аудио, так и для видео (и может быть расширен для других типов мультимедиа). Для видео возможности описываются с помощью структуры " [**\_ \_ \_ заглушки конфигурации видеопотока**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) ", а в Audio используется структура [**\_ \_ \_ CAPS в конфигурации**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) аудиопотока.

Чтобы перечислить типы мультимедиа, вызовите метод [**иамстреамконфиг:: жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) с индексом, начинающимся с нуля. Метод **жетстреамкапс** Возвращает тип мультимедиа и соответствующую структуру возможностей:


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Обратите внимание на то, как распределяются структуры для метода [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Метод выделяет структуру типа мультимедиа, в то время как вызывающий объект выделяет структуру возможностей. Приведение структуры возможностей к указателю массива байтов. После завершения работы с типом мультимедиа удалите структуру [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , а также блок формата типа мультимедиа.

Можно настроить устройство для использования формата, возвращаемого методом [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Просто вызовите [**иамстреамконфиг:: сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) с типом мультимедиа:


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Если ПИН-код не подключен, будет предпринята попытка использовать этот формат при подключении. Если ПИН-код уже подключен, он пытается подключиться с помощью нового формата. В любом случае возможно, что нисходящий фильтр отклонит формат.

Кроме того, можно изменить тип носителя перед его передачей методу [**сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) . Именно в этом случае используется структура [**\_ \_ \_ CAPS в конфигурации потока видео**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . В нем описываются все допустимые способы изменения типа носителя. Чтобы использовать эти сведения, необходимо ознакомиться с подробными сведениями о конкретном типе носителя.

Например, предположим, что [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) возвращает 24-битный формат RGB с размером кадра 320 x 240 пикселей. Эти сведения можно получить, изучив основной тип, подтип и блок формата типа мультимедиа:


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



Структура [**\_ \_ \_ Caps config в конфигурации потока видео**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) предоставляет минимальную и максимальную ширину и высоту, которые можно использовать для этого типа мультимедиа. Он также дает «шаг», который определяет приращение, на которое можно изменить ширину или высоту. Например, устройство может вернуть следующее:

-   Минаутпутсизе: 160 x 120
-   Максаутпутсизе: 320 x 240
-   Аутпутгрануларитикс: 8 пикселей (горизонтальный размер шага)
-   Аутпутгрануларитии: 8 пикселей (вертикальный размер шага)

Учитывая эти числа, можно установить ширину для любого значения в диапазоне (160, 168, 176,... 304, 312, 320) и высота по всем значениям в диапазоне (120, 128, 136,... 104, 112, 120). Этот процесс представлен на схеме ниже.

![Размеры видеоформатов](images/strmcap3.png)

Чтобы задать новый размер кадра, непосредственно измените структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , возвращаемую в [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



Затем передайте тип мультимедиа методу [**сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , как описано выше.

Элементы **минфрамеинтервал** и **максфрамеинтервал** с [**\_ \_ \_ ограничениями конфигурации видеопотока**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) — это минимальная и максимальная длина каждого кадра видео, которую можно преобразовать в частоту кадров следующим образом:

`frames per second = 10,000,000 / frame duration`

Чтобы запросить определенную частоту кадров, измените значение **авгтимеперфраме** в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) в типе мультимедиа. Устройство может не поддерживать все возможные значения между минимальным и максимальным значениями, поэтому драйвер будет использовать ближайшее значение, которое это возможно. Чтобы узнать, какое значение использует драйвер, вызовите [**иамстреамконфиг::**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) сетформат после вызова [](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).

Некоторые драйверы могут сообщать **макслонглонг** (0x7FFFFFFFFFFFFFFF) о значении **максфрамеинтервал**, что фактически означает отсутствие максимальной длительности. Однако может потребоваться принудительно применить минимальную частоту кадров в приложении, например 1 кадр/с.

## <a name="related-topics"></a>См. также

<dl> <dt>

[О типах носителей](about-media-types.md)
</dt> <dt>

[Настройка устройства видеозаписи](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



