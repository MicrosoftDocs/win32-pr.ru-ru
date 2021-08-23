---
description: Фильтр звукового кодировщика Microsoft MPEG-2 кодирует звуковые слои MPEG-1 I и II, включая поддержку расширений MPEG-2 с низким частотой дискретизации (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Кодировщик Microsoft MPEG-2 Audio Encoder (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584124"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Кодировщик Microsoft MPEG-2 Audio Encoder

Фильтр звукового кодировщика Microsoft MPEG-2 кодирует звуковые слои MPEG-1 I и II, включая поддержку расширений MPEG-2 с низким частотой дискретизации (LSF).

Для кодирования и мультиплексирования потоков аудио/видео используйте фильтр [**кодировщика Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) , который инкапсулирует функции обоих фильтров и фильтра [**видеокодировщика Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .

> [!Note]  
> Этот фильтр не поддерживается на платформах на базе IA-64.

 



Сведения о фильтре

Интерфейсы фильтра

[**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **иенкодерапи**<br/> [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**ивидеоенкодер**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Типы носителей входных закрепления

**MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**

Интерфейсы входных закрепления

[**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Типы носителей для выходного ПИН-кода

**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG2 \_ Audio**<br/> **MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG2 \_ Audio**<br/> **MEDIATYPE \_ Stream**, **\_ \_ Программа медиасубтипе MPEG2**<br/> **MEDIATYPE \_ Поток**, **\_ \_ транспорт медиасубтипе MPEG2**<br/>

Интерфейсы выходного ПИН-кода

[**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Фильтровать CLSID

**Идентификатор CLSID \_ CMPEG2EncoderAudioDS** (объявлено в вмкодекдсп. h)

Исполняемый объект

msmpeg2enc.dll

[Заслуживают](merit.md)

**\_ \_ не \_ использовать**

[Категория фильтра](filter-categories.md)

**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**



 

## <a name="remarks"></a>Remarks

Кодировщик MPEG-2 может формировать следующие типы выходных данных:

-   Простейший поток звука
-   Звук в потоке программы MPEG-2
-   Звук в транспортном потоке MPEG-2

Он поддерживает расширения MPEG-1 с уровнями I и II и MPEG-2 с низкой частотой дискретизации (LSF).

В примерах входных данных должно быть 16 бит на выборку с частотой выборки звука 48, 44,1, 32, 22,05 или 16 кГц. Кодировщику не удается выполнить повторную выборку аудиопотока; закодированный звук имеет ту же частоту выборки, что и входные данные.

Входные образцы должны быть Mono или стерео. В закодированном аудио содержится число каналов в качестве входных данных.

### <a name="limitations"></a>Ограничения

Кодировщик не поддерживает следующие действия:

-   Аудио битстреамс MPEG Layer III.
-   Многоканальное расширение MPEG-2 битстреамс.
-   MPEG-4 AAC битстреамс.
-   Битстреамс (NBC) MPEG-2 без обратной совместимости.
-   Создание пакетных пакетов простейшего потока (PES).
-   Цифровая кодировка Dolby.

### <a name="codec-properties"></a>Свойства кодека

Фильтр поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

-   [**аваудиочаннелкаунт**](avaudiochannelcount-property.md)
-   [**аваудиосамплерате**](avaudiosamplerate-property.md)
-   [**авенкаудиоинтервалтоенкоде**](avencaudiointervaltoencode-property.md)
-   [**авенккоммонформатконстраинт**](avenccommonformatconstraint-property.md)
-   [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md)
-   [**авенкмпакодингмоде**](avencmpacodingmode-property.md)
-   [**авенкмпакопиригхт**](avencmpacopyright-property.md)
-   [**авенкмпаемфасистипе**](avencmpaemphasistype-property.md)
-   [**авенкмпаенаблередунданципротектион**](avencmpaenableredundancyprotection-property.md)
-   [**авенкмпалайер**](avencmpalayer-property.md)
-   [**авенкмпаоригиналбитстреам**](avencmpaoriginalbitstream-property.md)
-   [**авенкмпаприватеусербит**](avencmpaprivateuserbit-property.md)

> [!Note]  
> В более ранней версии документации неправильно указаны некоторые дополнительные свойства, которые не поддерживаются.

 

Для обеспечения обратной совместимости фильтр поддерживает следующее свойство через интерфейс **иенкодерапи** :



| Свойство                 | Описание                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **\_скорость енкапипарам** | Эквивалентно [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md). |



 

Рекомендуется задавать свойства в следующем порядке:

1.  [**авенккоммонформатконстраинт**](avenccommonformatconstraint-property.md)
2.  [**авенкмпалайер**](avencmpalayer-property.md)
3.  [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md)
4.  [**авенкмпакодингмоде**](avencmpacodingmode-property.md)

Задайте остальные свойства в любом порядке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows главная Premium vista, Windows vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, Windows 7 Максимальная \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[**Типы носителей для демультиплексирования MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
