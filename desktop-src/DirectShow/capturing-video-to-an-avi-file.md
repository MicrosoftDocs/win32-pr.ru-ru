---
description: Запись видео в файл AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Запись видео в файл AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5ec58c021c5f37fed992959b33965efddb5603798ff756909879d307bca1f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689043"
---
# <a name="capturing-video-to-an-avi-file"></a>Запись видео в файл AVI

На следующем рисунке показана самая простая диаграмма для записи видео в файл AVI.

![Граф записи видео AVI](images/vidcap02.png)

Фильтр [мультиплексора AVI](avi-mux-filter.md) принимает видеопоток из ПИН-кода захвата и упаковывает его в поток AVI. Кроме того, аудиопоток может быть подключен к фильтру мультиплексора AVI. в этом случае мультиплексор будет чередовать два потока. Фильтр [записи файлов](file-writer-filter.md) записывает поток AVI на диск.

Чтобы построить граф, начните с вызова метода [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) следующим образом:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Первый параметр указывает тип файла — в данном случае это AVI. Второй параметр задает имя файла. Для AVI метод Сетаутпутфиленаме создает фильтр мультиплексора и фильтр для записи файлов и добавляет их в граф. Он также задает имя файла в фильтре записи файлов путем вызова метода [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) и соединяет два фильтра. Метод возвращает указатель на мультиплексор AVI в третьем параметре. При необходимости он возвращает указатель на интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) в четвертом параметре. Если этот интерфейс не нужен, можно присвоить этому параметру **значение NULL**, как показано в предыдущем примере.

Затем вызовите метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) для подключения фильтра записи к мультиплексору AVI следующим образом:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



Первый параметр дает категорию ПИН-кода, которая является закреплением \_ \_ захвата категории для захвата. Второй параметр задает тип носителя. Третий параметр является указателем на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра захвата. Четвертый параметр является необязательным; Он позволяет направить поток видео через промежуточный фильтр, например кодировщик, перед его передачей в фильтр мультиплексора. В противном случае присвойте этому параметру **значение NULL**, как показано в предыдущем примере. Пятый параметр — это указатель на фильтр мультиплексора. Этот указатель получается путем вызова метода Сетаутпутфиленаме.

Для записи звука вызовите RenderStream с типом носителя Media \_ Audio. Если вы записываете аудио и видео с двух отдельных устройств, рекомендуется сделать этот поток главным потоком. Это помогает предотвратить смещение между двумя потоками, поскольку фильтр мультиплексора AVI корректирует скорость воспроизведения видеопотока в соответствии с звуковым потоком. Чтобы задать главный поток, вызовите метод [**иконфигавимукс:: сетмастерстреам**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) в фильтре мультиплексора AVI:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Параметр для Сетмастерстреам — это номер потока, который определяется порядком вызова RenderStream. Например, если для видео сначала вызывается RenderStream, а затем для звукового сигнала, видео является потоком 0, а звук — потоком 1.

Кроме того, может потребоваться задать способ, которым фильтр мультиплексора AVI будет чередовать звуковые и видеопотоки, вызвав метод [**иконфигинтерлеавинг: \_ :p UT**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



При использовании \_ флага записи чередования Камера AVI выполняет чередование с частотой, подходящей для видеозаписи. Кроме того, можно использовать ЧЕРЕДОВАНИе \_ None, что означает отсутствие чередования — МУЛЬТИПЛЕКСОР AVI будет просто записывать данные в порядке поступления. Флаг ЧЕРЕДОВАНИя \_ означает, что он выполняет полное чередование, но этот режим менее подходит для видеозаписи, так как он требует наиболее полного перепрослушивания.

Кодирование видеопотока

Поток видео можно кодировать, вставив фильтр кодировщика между фильтром записи и фильтром мультиплексора AVI. Используйте [перечислитель системных устройств](system-device-enumerator.md) или средство [сопоставления фильтров](filter-mapper.md) для выбора фильтра кодировщика. (Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).)

Укажите фильтр кодировщика в качестве четвертого параметра для RenderStream, как показано жирным шрифтом в следующем примере:


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



Фильтр кодировщика может поддерживать [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) или другие интерфейсы для настройки параметров кодировки. Список возможных интерфейсов см. в разделе [интерфейсы кодирования и декодирования файлов](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



