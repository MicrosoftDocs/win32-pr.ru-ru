---
description: Запись файла DV типа 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Запись файла DV типа 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894202"
---
# <a name="capture-a-type-2-dv-file"></a>Запись файла DV типа 2

AVI-файл типа 2 DV содержит два потока, один из которых содержит видео DV и другое, содержащее звук. Чтобы записать файл типа 2 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.

![Тип 2. запись с предварительным просмотром](images/dv2-cap.png)

Этот граф почти тот же, что и граф для записи типа 1 (см. раздел [запись файла DV типа 1](capture-a-type-1-dv-file.md)). Однако перед достижением фильтра [мультиплексора AVI](avi-mux-filter.md) поток отслеживания проходит через фильтр [разделителя DV](dv-splitter-filter.md) . Поэтому мультиплексор AVI получает два потока: аудиопоток и видео в кодировке DV.

Выполните сборку этого графа следующим образом:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Создайте разделитель DV и добавьте его в граф фильтра.
2.  Вызовите [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , чтобы подключить фильтр мультиплексора AVI к фильтру записи файлов.
3.  Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр записи Мсдв к разделителю DV. Этот вызов также подключает один из выходных контактов разделителя DV к мультиплексору AVI.
4.  Вызовите RenderStream еще раз, чтобы подключить другой ПИН-код разделителя DV к мультиплексору камеры AVI.
5.  Вызовите RenderStream третий раз, чтобы отобразить предварительный просмотр потока. Пропустите этот шаг, если не хотите выполнять предварительный просмотр видео.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



