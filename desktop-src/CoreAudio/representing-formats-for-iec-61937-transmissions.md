---
description: Благодаря увеличению количества устройств хранения мультимедиа, требующих сжатия звуковых форматов, приложения должны вычислить, описать и использовать множество новых закодированных звуковых данных для передачи содержимого с компьютеров на устройства, например, с помощью формата HDMI или Дисплайпорт.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Представление форматов для передач IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655925"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Представление форматов для передач IEC 61937

Благодаря увеличению количества устройств хранения мультимедиа, требующих сжатия звуковых форматов, приложения должны вычислить, описать и использовать множество новых закодированных звуковых данных для передачи содержимого с компьютеров на устройства, например, с помощью формата HDMI или Дисплайпорт.

Для представления закодированного звукового потока, передаваемого через совместимый с IEC 61937 интерфейс, приложение должно предоставить:

-   Характеристики закодированного звукового потока для передачи.

-   Характеристики декодированного звукового потока на целевом устройстве.

В Windows Vista и более ранних операционных системах Windows приложение может определить уровень качества звукового формата от количества каналов, размера выборки и скорости передачи данных в потоке аудиопотока, использующем этот формат. Для формата PCM эта информация доступна из элементов **нчаннелс**, **нсамплесперсек** и **навгбитесперсек** структуры **вавеформатекс** , которая определяет формат. Для формата, отличного от PCM, эти три элемента были коммандиред для хранения информации о сжатых данных в потоке аудио. Таким словами, структура **вавеформатекс** не имеет сведений о действительном количестве каналов, объеме выборки и скорости передачи данных из аудиопотока, не использующих PCM, после распаковки и воспроизведения потока. На основе информации в этой структуре пользователь или приложение могут испытывать трудности при откладывание уровня качества потока, не являющегося потоком PCM.

**Вавеформатекс** был расширен до структуры **вавеформатекстенсибле** , чтобы предоставить дополнительные характеристики потока. Однако эта структура также недостаточна для описания потока для передачи данных IEC 61937, так как она предполагалась для представления одного набора характеристик и используется для несжатых, многоканальные данные PCM.

В Windows 7 операционная система решает эту проблему, предоставляя поддержку новой структуры, **вавеформатекстенсибле \_ IEC61937** , которая расширяет структуру **вавеформатекстенсибле** для хранения двух наборов характеристик аудиопотока: закодированный аудио формат перед передачей и характеристиками звукового потока после декодирования. Новая структура явно указывает фактическое количество каналов, размер выборки и скорость передачи данных в формате, не являющемся форматом PCM. С помощью этих сведений приложение может определить уровень качества потока, не являющегося потоком PCM, после его распаковки и воспроизведения.

Структура **\_ IEC61937 вавеформатекстенсибле** объявляется в заголовке ксмедиа. h, ВКЛЮЧЕННОМ в пакет SDK для Windows 7. Элемент **форматекст** — это структура **вавеформатекстенсибле** , в которой хранятся характеристики передаваемого потока. Элемент **Format** структуры **вавеформатекстенсибле** является структурой **вавеформатекс** . Содержимое этого **вавеформатекс** и **вавеформатекстенсибле** указывает приложению, может ли структура интерпретироваться как структура **\_ IEC61937 вавеформатекстенсибле** . Для структуры **\_ IEC61937 вавеформатекстенсибле** :

-   Элемент **вформаттаг** объекта **вавеформатекс** должен содержать формат волны \_ \_ EXTENSIBLE ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   Элемент **Подформата** структуры **вавеформатекстенсибле** указывает идентификатор GUID закодированного формата для передачи. Например, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` указывает формат Dolby Digital Plus. Поддерживаемые идентификаторы GUID см. в разделе идентификаторы GUID подформатов.

-   Размер, указанный членом **КБСИЗЕ** вавеформатекс, составляет 34 байт. (`FormatExt.Format.cbSize = 34`). Общий размер **вавеформатекстенсибле \_ IEC61937** составляет 52 байт.

Члены **двенкодедсамплесперсек**, **Двенкодедчаннелкаунт** и **дваверажебитесперсек** **вавеформатекстенсибле \_ IEC61937** описывают частоту выборки, число каналов и скорость передачи данных в байтах потока аудиопотока после его декодирования.

## <a name="subformat-guids"></a>Идентификаторы GUID подформата

В Windows 7 заголовок Ксмедиа. h содержит определения для идентификаторов GUID подформата для сжатых звуковых форматов, определенных CEA-861-D. Идентификаторы GUID указываются в элементе подформата **вавеформатекстенсибле**, указанном в элементе **форматекст** структуры **вавеформатекстенсибле \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Идентификаторы GUID для сжатых звуковых форматов, доступных в виде стандартных звуковых форматов IEC 61937, перечислены в следующей таблице. Эти форматы схожи с существующими представлениями форматов звука с кодом 3 (AC-3) и Digital театра (DTS) в Windows.



| Тип CEA 861 | GUID подформата                                                                                                          | Описание                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | См. поток.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ вавеформатекс<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (уровень 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (уровень 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (многоканальный)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ AAC<br/>                         | Расширенное аудио кодирование (MPEG-2/4 AAC в ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0A         | 0000000a-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital \_ Plus<br/>        | Dolby Digital Plus                           |
| 0x0A         | 0000010a-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ атмос<br/> | Dolby атмос в кодировке Dolby Digital Plus  |
| 0x0f         |                                                                                                                         | Неиспользованные зарезервированные                              |



 

В следующей таблице перечислены идентификаторы GUID для сжатых звуковых форматов, которые передаются в звуковых примерах с высоким уровнем скорости.



| Тип CEA 861 | GUID подформата                                                                                           | Описание                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0B         | 0000000b-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24-разрядная, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby водо1,0:<br/> Dolby Труехд (MLP – меридианов без потерь упаковки) — 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby водо2,0: <br/> Dolby Труехд – 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов или ЛПКМ до 24 Мбит/с. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MAT21<br/> | Dolby водо2,1: <br/> Dolby Труехд – 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов или ЛПКМ до 24 Мбит/с. <br/>           |
| 0x0E         | 00000164-0000-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ WMA \_ Pro<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

Драйвер класса HD Audio, предоставляемый корпорацией Майкрософт, поддерживает форматы PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, BI (MLP). Идентификаторы GUID для сжатых звуковых форматов, которые не поддерживаются драйвером класса HD Audio и могут быть реализованы сторонними решениями, перечислены в следующей таблице.



| Тип CEA 861 | GUID подформата                                                                                              | Описание                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ АТРАК<br/>           | Акустическое кодирование с адаптивным преобразованием (АТРАК)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> \_ПОДТИП ксдатаформат \_ IEC61937 \_ один \_ битовый \_ звук<br/> | One-Bit звук                                                                  |
| 0x0D         | 0000000d-0cea-0010-8000-00aa00389b71<br/> КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ DST<br/>             | Прямой потоковый транспорт (DST) — сжатый DSD без потерь (прямая Streaming Digital). |



 

## <a name="dolby-digital-plus-format"></a>Формат Dolby Digital Plus

Когда содержимое Dolby Digital Plus передается через IEC 60958, скорость выборки ссылок должна быть в четыре раза больше частоты выборки содержимого. Dolby Digital Plus поддерживает частоту примеров содержимого 32 кГц, 44,1 кГц и 48 кГц. Такие интерфейсы, как HDMI, не поддерживают 128 кГц (32 кГц x 4), поэтому поддерживаются только тарифы на выборку содержимого (44,1 и 48 кГц).

Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937 для представления формата Dolby Digital Plus с частотой дискретизации 48 кГц, показаны в следующем примере.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby Труехд (с)

Содержимое Dolby Труехд передается через IEC 60958 в каналах 176,4 кГц/8 (требует частоту кадров IEC 60958, равном 705,6 кГц) для частотных выборок содержимого в 44,1, 88,2 и 176,4 кГц и 192 кГц/8 (требует частоту кадров IEC 60958 в 768 КГц) для частоты дискретизации для примеров содержимого 48, 96 и 192 кГц.

Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937, чтобы представить Труехд Dolby с частотой дискретизации 96 кГц, показаны в следующих примерах.

Dolby водо1,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby водо2,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby водо2,1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> Поддержка одной версии Dolby, не подразумевает поддержки Dolby для управления версиями с более низким номером версии. Так как Dolby водо2,1 имеет обратную совместимость с предыдущими версиями функции Dolby, драйвер класса, который указывает на поддержку Dolby водо2,1, обычно также указывает на поддержку Dolby водо2,0 и Dolby водо1,0, используя отдельную \_ структуру вавеформатекстенсибле IEC61937 для каждой версии.

 

## <a name="wma-pro"></a>WMA Pro

Аудио содержимое WMA Pro может быть закодировано в одном из четырех профилей, перечисленных в следующей таблице.



| Профиль | Свойство-значение                                                                                                                                                                                                                                                      | Описание                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Степпинг      | Максимальная скорость передачи — 192000 бит/с <br/> Максимальная частота выборки — 48 кГц <br/> Максимальное число каналов — 2 <br/> Максимальный размер буфера — 600 \* 1024 бит <br/> Максимальное число выборок на кадр — 2048 <br/> Максимальное число бит на кадр — 655536<br/>   | Рекомендуется для воспроизведения музыки и потоковой передачи в эфире.<br/> Максимальная скорость потока в звуковой рамке — 1536000 бит/с.<br/>          |
| M1      | Максимальная скорость передачи — 385000 бит/с <br/> Максимальная частота выборки — 48 кГц <br/> Максимальное число каналов — 6 <br/> Максимальный размер буфера — 600 \* 1024 бит <br/> Максимальное число выборок на кадр — 4096 <br/> Максимальное число бит на кадр — 131072<br/>   | Рекомендуется для фильмов с определением стандартных звуковых эффектов.<br/> Максимальная скорость потока в звуковой рамке — 1536000 бит/с.<br/> |
| M2      | Максимальная скорость передачи — 769000 бит/с <br/> Максимальная частота выборки — 96 кГц <br/> Максимальное число каналов — 6 <br/> Максимальный размер буфера — 1200 \* 1024 бит <br/> Максимальное число выборок на кадр — 4096 <br/> Максимальное число бит на кадр — 131072<br/>  | Рекомендуется для фильмов с высокой степенью четкости.<br/> Максимальная скорость в звуковой рамке — 3072000 бит/с.<br/>         |
| M3      | Максимальная скорость передачи — 3000000 бит/с <br/> Максимальная частота выборки — 96 кГц <br/> Максимальное число каналов — 8 <br/> Максимальный размер буфера — 2400 \* 1024 бит <br/> Максимальное число выборок на кадр — 4096 <br/> Максимальное число бит на кадр — 131072<br/> | Рекомендуется для цифрового кинотеатра.<br/> Максимальная скорость в звуковой рамке — 3072000 бит/с.<br/>                               |



 

Профили M0 и M1 соответствуют потоку 48 кГц/16 бит/стерео (1536000 бит/с) IEC 60958. Профили m2 и M3 соответствуют потоку 96 кГц/16 бит/стерео (3072000 бит/с) IEC 60958.

Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937 для представления WMA Pro в качестве профиля m2, показаны в следующем примере.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Форматы устройств](device-formats.md)
</dt> </dl>

 

 




