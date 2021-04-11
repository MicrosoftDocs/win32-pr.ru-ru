---
description: Передача из файла типа-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Передача из файла типа-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080938"
---
# <a name="transmit-from-type-1-file"></a>Передача из файла типа-1

Чтобы передать файл типа 1 при предварительном просмотре файла, используйте граф фильтра, показанный на следующей схеме.

![Тип-1. Передача с предварительной версией](images/dv1-transmit.png)

Фильтры в этой диаграмме включают:

-   [Разделитель AVI](avi-splitter-filter.md) АНАЛИЗИРУЕТ файл AVI. Для DV-файла типа 1 закрепление вывода обеспечивает чередование DV.
-   Фильтр [бесконечного ПИН-кода tee](infinite-pin-tee-filter.md) разделяет DV с чередованием на поток передачи и поток предварительного просмотра. Оба потока содержат одни и те же данные с чередованием. (В этом графе вместо [смарт-tee](smart-tee-filter.md)используется неограниченный ПИН-код tee, так как при чтении из файла не существует опасности удаления кадров, как и в случае с динамической записью.)
-   [Разделитель DV](dv-splitter-filter.md) разделяет поток с чередованием на видеопоток видео, декодированный [видеодекодером DV](dv-video-decoder-filter.md)и звуковым потоком. Оба потока являются рендерерд для предварительной версии.

Выполните сборку этого графа следующим образом:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  Вызовите [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника к графу фильтра.
2.  Создайте разделитель AVI и бесконечный ПИН-код tee и добавьте их в граф.
3.  Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр источника к разделителю AVI. Указание носителя \_ с чередованием для обеспечения сбоя метода, если исходный файл не является ФАЙЛОМ DV типа 1. В этом случае можно выполнить откат и попытаться создать граф передачи типа 2.
4.  Вызовите **RenderStream** еще раз, чтобы направить поток с чередованием из разделителя AVI на бесконечный ПИН-код Tee
5.  Вызовите RenderStream третий раз, чтобы направить один поток из бесконечного ПИН-кода tee в фильтр МСДВ для передачи на устройство.
6.  Вызовите **RenderStream** один раз, чтобы создать раздел для предварительного просмотра диаграммы.

Если вы не хотите использовать предварительную версию, просто подключите источник файла к фильтру МСДВ:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



