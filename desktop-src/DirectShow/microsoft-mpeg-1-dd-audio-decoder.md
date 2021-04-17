---
description: 'Этот фильтр декодирует следующие форматы звука:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Microsoft MPEG-1/DD/AAC Audio декодер (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682249"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Декодер звука Microsoft MPEG-1/DD/AAC

Этот фильтр декодирует следующие форматы звука:

-   Звуковые слои MPEG-1 I и II.
-   Обратная совместимость MPEG-2 аудио, слои I и II (ISO/IEC 13818-3), моно и стерео.
-   Расширенный профиль (LC) с низким уровнем сложности (AAC).
-   High-Efficiency AAC (HE-AAC) версии 1 и версии 2.
-   Сквозные системы цифрового кинотеатра (DTS) для цифрового выхода.
-   ЛПКМ, Mono и стерео, с или без PES.
-   Dolby Digital.
-   Dolby Digital Plus, включая преобразование из Dolby Digital Plus в Dolby Digital для цифрового выхода.

> [!Note]  
> Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.

 

> [!Note]  
> Этот фильтр не поддерживается на платформах на базе IA-64.

 

Для декодирования форматов Dolby Digital Plus, AAC и AAC требуется Windows 7. Декодирование Dolby Digital или Dolby Digital Plus не поддерживается в Windows 7 Домашняя базовая или Windows 7 Начальная.

В реестре понятное имя этого фильтра — "Microsoft ДТВ-DVD Audio декодер".



Сведения о фильтре

Интерфейсы фильтра

[**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Типы носителей входных закрепления

В Windows Vista и более поздних версиях фильтр поддерживает следующие входные типы:<br/>

-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1Audio**
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1Payload**
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG2 \_ Audio**
-   **MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).
-   **MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ DTS** (см. Примечание 2).
-   **MEDIATYPE \_ \_зашифрованный \_ DVD-диск**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**
-   **MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ MPEG2 \_ Audio**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ DTS** (см. Примечание 2).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ MPEG2 \_ Audio**
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG1Audio**
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG2 \_ Audio**

Начиная с Windows 7, фильтр также поддерживает следующие типы входных данных:<br/>

-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ Ддплус** (см. Примечание 1).
-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ DTS2** (см. Примечание 2).
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**
-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ DVM** (см. Примечание 1).
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG \_ уровнями гарантии**
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ RAW \_ AAC1**
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ Ддплус** (см. Примечание 1).
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG \_ уровнями гарантии**

Тип входных данных может динамически изменяться во время потоковой передачи.<br/> Дополнительные сведения об этих типах носителей см. в разделе [**аудио подтипы**](audio-subtypes.md).<br/>

> [!Note]  
> 1. Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.

<br/>

> [!Note]  
> 2. Входные системы цифрового кинотеатра (DTS) поддерживают только выходные данные S/PDIF (DTS через S/PDIF). Декодирование звука не поддерживается.

<br/>

Интерфейсы входных закрепления

[**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**икспропертисет**](ikspropertyset.md)<br/> [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Типы носителей для выходного ПИН-кода

В Windows Vista и более поздних версиях фильтр поддерживает следующие типы выходных данных:<br/>

-   **MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ AC3 \_ SPDIF** (то же, что **ксдатаформат \_ подтип \_ IEC61937 \_ Dolby \_ Digital**)
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**

Начиная с Windows 7, фильтр также поддерживает следующие типы выходных данных:<br/>

-   **MEDIATYPE \_ Audio**, **ксдатаформат \_ подтип \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Аудио**, **медиасубтипе \_ IEEE \_ float**

Интерфейсы выходного ПИН-кода

[**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Фильтровать CLSID

**Идентификатор CLSID \_ CMPEG2AudDecoderDS** (объявлено в вмкодекдсп. h)

Исполняемый объект

msmpeg2adec.dll

[Заслуживают](merit.md)

**Неуспешный \_ Обычная** — 1

[Категория фильтра](filter-categories.md)

**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**



 

> [!Note]  
> Более ранняя версия документации объявила, что этот фильтр может декодировать "MPEG-2 Audio". Фильтр декодирует только обратно совместимые аудио MPEG-2.

 

## <a name="remarks"></a>Комментарии

Потоки Mono всегда декодированы в стерео.

Для потоков с конфигурацией каналов из двух или более динамиков декодер выполняет одно из следующих действий:

-   До шести каналов с использованием стандартной конфигурации динамика 5,1.
-   Довнмиксес на стерео.

Чтобы выбрать один из этих вариантов, используйте интерфейс [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , чтобы задать свойство [**авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) перед соединением ПИН-кодов. Кроме того, когда приложение создает граф фильтра, оно может задать нужный тип носителя для выходного контакта.

### <a name="aac-decoding"></a>Декодирование AAC

Для AAC декодер имеет определенные ограничения формата для сжатых входных данных AAC. Эти ограничения формата аналогичны Media Foundation [**декодера AAC**](../medfound/aac-decoder.md)и описаны в разделе "[**ограничения формата**](../medfound/aac-decoder.md)".

Декодер DirectShow также принимает различные типы входных данных, чем декодер Media Foundation. Декодер DirectShow поддерживает следующие типы входных данных AAC:

-   **Медиасубтипе \_ Необработанные \_ AAC1**: RAW AAC, обычно находятся в формате AVI или матроска (. MKV) файлы.
-   **Медиасубтипе \_ MPEG \_ ADTS \_ AAC**: AAC в потоке передачи звуковых данных (ADTS) для потоковой передачи.
-   **Медиасубтипе \_ MPEG \_ уровнями гарантии**: транспортный поток с уровнем синхронизации (уровнями гарантии) и уровнем мультиплексирования (латм).

Декодер Media Foundation поддерживает следующие типы входных данных AAC:

-   Мфаудиоформат \_ AAC (то же, что **медиасубтипе \_ MPEG \_ хеаак**) для воспроизведения файла MP4.
-   **Медиасубтипе \_ Необработанный \_ AAC1**.

### <a name="property-sets"></a>Наборы свойств

Входной ПИН-код декодера поддерживает следующие наборы свойств через [**икспропертисет**](ikspropertyset.md):

-   [**Набор свойств защиты копирования DVD-дисков**](dvd-copy-protection-property-set.md)
-   [**Набор свойств "частота-изменение**](rate-change-property-set.md)".

> [!Note]  
> Начиная с Windows 7, декодер поддерживает режим хитрости через набор свойств Rate-Change. Он поддерживает скорости воспроизведения в диапазоне \[ 0,501 – 2,0 \] , где 1,0 — это нормальная скорость воспроизведения, а 2,0 — вдвое нормально.

 

### <a name="codec-properties"></a>Свойства кодека

Входной ПИН-код декодера поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Свойство                                                          | Требуется                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**аваудиочаннелконфиг**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**аваудиочаннелкаунт**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**аваудиосамплерате**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**авддсурраундмоде**](avddsurroundmode-property.md)             | Только для Windows Vista; не поддерживается в Windows 7 и более поздних версиях. |
| [**авдекаудиодуалмоно**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**авдеккоммонинпутформат**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**авдеккоммонмеанбитрате**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Фильтр поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Свойство                                                                          | Требуется      |
|-----------------------------------------------------------------------------------|---------------|
| [**авдекаакдовнмиксмоде**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**авдекаудиодуалмонорепромоде**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**Авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) (см. Примечание 3). | Windows Vista |
| [**авдекдддинамикранжескалехигх**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**авдекдддинамикранжескалелов**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**авдекддоператионалмоде**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**авдекммксскласс**](avdecmmcss-property.md)                                    | Windows Vista |
| [**авдсплауднессекуализатион**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**авдспспеакерфилл**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. Свойство [**авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) должно быть установлено до подключения выходного ПИН-кода декодера. В противном случае изменение не будет действовать.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Домашняя расширенная, Windows Vista Ultimate, \[ только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Звуковые подтипы**](audio-subtypes.md)
</dt> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[**Типы носителей DVD**](dvd-media-types.md)
</dt> </dl>

 

 
