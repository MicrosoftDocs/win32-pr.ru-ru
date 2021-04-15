---
description: Запись файла DV типа 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Запись файла DV типа 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555053"
---
# <a name="capture-a-type-1-dv-file"></a>Запись файла DV типа 1

Файл AVI типа 1 DV содержит один поток с чередованием. Чтобы записать файл типа 1 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.

![запись типа 1 с предварительным просмотром](images/dv1-cap.png)

Фильтры в этой диаграмме включают:

-   Фильтр [Smart tee](smart-tee-filter.md) разделяет DV с чередованием на поток записи и предварительный просмотр потока. Оба потока содержат одни и те же данные с чередованием.
-   Средство [мультиплексирования](avi-mux-filter.md) и [записи файлов](file-writer-filter.md) AVI записывает поток с чередованием на диск.
-   [Разделитель DV](dv-splitter-filter.md) разделяет поток с чередованием на поток видео в DV и аудиопоток. Оба потока являются рендерерд для предварительной версии.
-   [Видеодекодер DV](dv-video-decoder-filter.md) дедекодирует видеопоток видео для предварительного просмотра.

Выполните сборку этого графа следующим образом:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Вызовите [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , чтобы подключить фильтр мультиплексора AVI к фильтру записи файлов.
2.  Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) с захватом категории ПИН-кода \_ \_ для отображения потока отслеживания. Построитель графов записи автоматически вставляет интеллектуальный фильтр Tee.
3.  Вызовите RenderStream еще раз, но с помощью предварительной версии категории ПИН-кода \_ \_ для отображения предварительного просмотра потока. Пропустите этот вызов, если вы не хотите просматривать видео.

Для обоих вызовов RenderStream типом носителя является носитель с \_ чередованием, что означает чередование DV-видео. В этом коде построитель диаграмм записи автоматически добавляет каждый необходимый фильтр, за исключением фильтра записи МСДВ.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



