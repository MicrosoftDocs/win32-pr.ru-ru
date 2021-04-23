---
description: Пользовательские форматы файлов
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Пользовательские форматы файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361dca97fcd34b30e3c29d6ba189ad26968d4fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990130"
---
# <a name="custom-file-formats"></a><span data-ttu-id="49be8-103">Пользовательские форматы файлов</span><span class="sxs-lookup"><span data-stu-id="49be8-103">Custom File Formats</span></span>

<span data-ttu-id="49be8-104">При наличии пользовательского фильтра мультиплексора или модуля записи файлов, поддерживающего собственный формат файлов, можно указать идентификатор CLSID в качестве первого параметра метода [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="49be8-104">If you have a custom mux or file-writer filter that supports your own file format, you can specify the CLSID as the first parameter of the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



<span data-ttu-id="49be8-105">Дополнительные сведения об этом использовании см. в разделе [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="49be8-105">For more information about this usage, see [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49be8-106">См. также</span><span class="sxs-lookup"><span data-stu-id="49be8-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49be8-107">Запись видео в файл</span><span class="sxs-lookup"><span data-stu-id="49be8-107">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



