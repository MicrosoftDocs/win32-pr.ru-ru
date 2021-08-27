---
description: Преобразования типов мультимедиа
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Преобразования типов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5d91844a062d5d4a1aa98af1a2e77c9cabfadb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474350"
---
# <a name="media-type-conversions"></a>Преобразования типов мультимедиа

иногда требуется выполнить преобразование между Media Foundation типами носителей и более старыми структурами типов мультимедиа из DirectShow или пакета SDK Windows Media Format.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>Из структуры формата в тип Media Foundation

Следующие функции инициализируют Media Foundation тип носителя из структуры формата. Эти функции также полезны, если поток данных или заголовок файла содержит структуру формата. Например, заголовок файла для звуковых файлов звукозаписи содержит структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .




| Преобразуемая структура | Компонент | 
|----------------------|----------|
| <a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br /><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (объекты мультимедиа DirectX) <br /><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (пакет SDK для Windows MEDIA Format) <br /><blockquote>[!Note]<br />Эти структуры эквивалентны.</blockquote><br /><br /> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>мфинитмедиатипефромаммедиатипе</strong></a> | 
| <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>битмапинфохеадер</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>мфкреатевидеомедиатипефромбитмапинфохеадерекс</strong></a> | 
| <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>мфвидеоформат</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>мфинитмедиатипефроммфвидеоформат</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>видеоинфохеадер</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>мфинитмедиатипефромвидеоинфохеадер</strong></a> | 
| <a href="/previous-versions/dd757713(v=vs.85)"><strong>Вавеформатекс</strong></a> или <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>вавеформатекстенсибле</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>мфинитмедиатипефромвавеформатекс</strong></a> | 




 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Из типа Media Foundation в структуру формата

Следующие функции создают или инициализируют структуру формата на основе типа носителя Media Foundation.



| Компонент                                                                             | Целевая структура                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Имфмедиатипе::, представляющее**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_ \_Тип носителя**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**мфвидеоформат**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**мфкреатеаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_тип носителя \_ AM**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**мфкреатемфвидеоформатфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**мфвидеоформат**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**Вавеформатекс**](/previous-versions/dd757713(v=vs.85)) или [ **вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**мфинитаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_тип носителя \_ AM**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Сопоставления формата

В следующих таблицах перечислены Media Foundation атрибуты, соответствующие различным структурам формата. Не все эти атрибуты можно перевести напрямую. Для выполнения преобразований следует использовать функции, перечисленные в предыдущем разделе. Эти таблицы предоставляются главным образом для справки.

### <a name="am_media_type"></a>\_тип носителя \_ AM



| Член                   | attribute                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **бтемпоралкомпрессион** | [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md) |
| **бфикседсизесамплес**    | [**\_ \_ примеры фиксированного \_ размера MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           |
| **лсамплесизе**          | [**\_ \_ Размер образца MF \_ MT**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>ВАВЕФОРМАТЕКС, ВАВЕФОРМАТЕКСТЕНСИБЛЕ



| Член                  | attribute                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **вформаттаг**          | [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)<br/> Если **вформаттаг** имеет \_ \_ расширяемый формат Wave, подтип находится в элементе **подформата** .<br/> |
| **нчаннелс**           | [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **нсамплесперсек**      | [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **навгбитесперсек**     | [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **нблоккалигн**         | [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **вбитсперсампле**      | [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **ввалидбитсперсампле** | [**\_ \_ \_ допустимый бит для звука MF MT \_ \_ на \_ выборку**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **всамплесперблокк**    | [**\_ \_ звуковые образцы MF MT \_ \_ на \_ блок**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **двчаннелмаск**       | [**\_ \_ \_ Маска канала MF MT \_ Audio**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **Подформат**           | [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Дополнительные данные              | [**\_ \_ данные пользователя MF \_ MT**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>ВИДЕОИНФОХЕАДЕР, VIDEOINFOHEADER2



| Член                                         | attribute                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **двбитрате**                                  | [**\_ \_ Средняя скорость MF \_ MT**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **двбитерроррате**                             | [**\_ \_ \_ \_ Частота погрешностей средней разрядности MF MT \_**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **авгтимеперфраме**                            | [**MF \_ \_ \_ Частота кадров MT**](mf-mt-frame-rate-attribute.md); для вычисления этого значения используйте [**мфаверажетимеперфраметофрамерате**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) .                                                                             |
| **двинтерлацефлагс**                           | [**\_ \_ режим чересстрочную РАЗВЕРТКи MF \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **двкопипротектфлагс**                         | Нет определенного эквивалента                                                                                                                                                                                                                            |
| **двпиктаспектратиокс**, **двпиктаспектратиой** | [**MF \_ Пропорции в \_ 1 – пиксельное \_ \_ соотношение**](mf-mt-pixel-aspect-ratio-attribute.md); необходимо преобразовать пропорции изображения в пропорции рисунка.                                                                                                      |
| **двконтролфлагс**                             | [**MF \_ \_ \_ \_ Флаги элемента управления "MT Pad**](mf-mt-pad-control-flags-attribute.md)". Если установлен флаг **амконтрол \_ колоринфо present ( \_ присутствие** ), задайте атрибуты расширенного цвета, описанные в разделе [Расширенные сведения о цвете](extended-color-information.md). |
| **бмихеадер. бивидс**, **бмихеадер. бихеигхт**  | [**\_ \_ Размер пакета MF \_ MT**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **Бмихеадер. Бибиткаунт**                       | Неявный в подтипе ([**MF \_ MT, \_ подтип**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **Бмихеадер. Бикомпрессион**                    | Неявный в подтипе.                                                                                                                                                                                                                         |
| **Бмихеадер. Бисизеимаже**                      | [**\_ \_ Размер образца MF \_ MT**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Сведения о палитре                            | [**\_ \_ Палитра MF MT**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Следующие атрибуты могут выводиться из структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , но также требуются некоторые знания о формате. Например, различные форматы YUV имеют разные требования к STRIDE.

-   [**MF \_ , \_ шаг по умолчанию \_**](mf-mt-default-stride-attribute.md)
-   [**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_ \_ \_ Апертура для поиска MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Член                                   | attribute                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **двстарттимекоде**                      | [**\_ \_ \_ \_ код времени начала MF MT \_ MPEG**](mf-mt-mpeg-start-time-code-attribute.md) |
| **бсекуенцехеадер**                      | [**\_ \_ \_ заголовок последовательного сервера MF MT MPEG \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **бикспелсперметер**, **бийпелсперметер** | [**пропорции MF \_ MT \_ пикселей \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Член               | attribute                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **двстарттимекоде**  | [**\_ \_ \_ \_ код времени начала MF MT \_ MPEG**](mf-mt-mpeg-start-time-code-attribute.md) |
| **двсекуенцехеадер** | [**\_ \_ \_ заголовок последовательного сервера MF MT MPEG \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **двпрофиле**        | [**\_Профиль MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md)                 |
| **двлевел**          | [**\_Уровень MF \_ MT \_**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**\_ \_ Флаги MF MT MPEG2 \_**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Примеры

Следующий код заполняет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) из типа видеоклипа. Обратите внимание, что при преобразовании теряются некоторые сведения о форматировании (чередование, частота кадров, Расширенные данные о цветах). Однако это может быть полезно при сохранении растрового изображения из видеокадра, например.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы носителей](media-types.md)
</dt> </dl>

 

 
