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
# <a name="custom-file-formats"></a>Пользовательские форматы файлов

При наличии пользовательского фильтра мультиплексора или модуля записи файлов, поддерживающего собственный формат файлов, можно указать идентификатор CLSID в качестве первого параметра метода [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Дополнительные сведения об этом использовании см. в разделе [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



