---
description: Записать DV в Распакованный RGB
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Записать DV в Распакованный RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139415"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Записать DV в Распакованный RGB

В этом примере показано, как записать DV с камеры и сохранить его в файле как несжатый RGB при предварительном просмотре. Используйте граф фильтра, показанный на следующей схеме.

![запись несжатого RGB в файл](images/dv-rgb-cap.png)

Фильтр разделителя DV разделяет аудио-или видеофайлы с чередованием на отдельные видео и звуковые потоки. видео с цифровой кодировкой преобразуется в фильтр [видеодекодеров DV](dv-video-decoder-filter.md) , который выводит несжатое видео в формате RGB. Видео RGB направляется через фильтр Smart tee в фильтр мультиплексора (для записи) и модуль подготовки видео (для предварительного просмотра). В то же время поток аудио из разделителя DV проходит через фильтр неограниченного ПИН-кода tee для камеры AVI и модуля подготовки звука. Диспетчер графов фильтров сохраняет все эти потоки в синхронизированном виде, используя метки времени для образцов и время ссылки на граф.

Эта диаграмма может показаться ненужной сложной, но она гарантирует, что поток видео с цифровой кодировкой будет декодирован только один раз, что снизит требования к ЦП. Кроме того, обратите внимание, что видео проходит через фильтр Smart tee, когда звук проходит через фильтр неограниченного ПИН-кода Tee. Smart tee может удалить кадры предварительного просмотра, чтобы улучшить производительность отслеживания, что желательно для видео, но не для звука, когда удаленные образцы очень заметны. Кроме того, так как для звука требуется намного более низкая пропускная способность, чем в видеоролике, существует сравнительно немало шансов на удаление звука в файле.

Эту диаграмму необходимо создавать по одному разделу за раз, но метод RenderStream по-прежнему может помочь. Используйте следующий код:


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



Необходимо создать разделитель DV, видеодекодер DV, Smart tee и неограниченный ПИН-код tee и добавить каждый из них в граф фильтра. (Для краткости эти шаги пропускаются из предыдущего кода.) В этом примере используется метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) для поиска ПИН-кодов записи и предварительного просмотра в фильтре Smart Tee. захват всегда выводит ПИН-код 0, а Предварительная версия — выходной ПИН-код 1.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



