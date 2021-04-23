---
description: В этом разделе приведен пример использования градиентов в OM-модели XPS.
ms.assetid: c58c9e5a-c871-4b44-a1be-0aceafa2f805
title: Градиенты модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5aac5fcce4ebd662d834705d1e8d84140f09000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711689"
---
# <a name="xps-om-gradients"></a><span data-ttu-id="a9d6f-103">Градиенты модели XPS</span><span class="sxs-lookup"><span data-stu-id="a9d6f-103">XPS OM Gradients</span></span>

<span data-ttu-id="a9d6f-104">В этом разделе приведен пример использования градиентов в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="a9d6f-104">This topic provides an example of using gradients in an XPS OM.</span></span>

## <a name="add-a-new-stop-to-an-existing-gradient"></a><span data-ttu-id="a9d6f-105">Добавление новой позиции к существующему градиенту</span><span class="sxs-lookup"><span data-stu-id="a9d6f-105">Add a new stop to an existing gradient</span></span>

<span data-ttu-id="a9d6f-106">Следующий пример кода добавляет новую точку на градиент кисти линейного градиента.</span><span class="sxs-lookup"><span data-stu-id="a9d6f-106">The following code example adds a new stop to the gradient of a linear-gradient brush.</span></span>


```C++
    // brush is the pointer to the gradient brush that will get 
    //  the new gradient and is initialized outside of this code example

    // this is the start of the method that updates the brush
    HRESULT                           hr = S_OK;
    XPS_COLOR                         xpsColorStop;
    IXpsOMGradientStopCollection      *stops;
    IXpsOMGradientStop                *xpsNewGradientStop = NULL, *thisStop = NULL, *nextStop = NULL;
    UINT32                            thisStopIdx, numStops;
    FLOAT                             thisStopOffset, nextStopOffset, newStopOffset;
    BOOL                              bUpdated = FALSE;

    // define the new stop color to be yellow
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xFF;
    xpsColorStop.value.sRGB.green = 0xFF;
    xpsColorStop.value.sRGB.blue  = 0x00;
    
    // create a new gradient stop by setting the color and location 
    // this stop will be half way between the start and end point
    newStopOffset = 0.5f;
    hr = xpsFactory->CreateGradientStop(&xpsColorStop, NULL, newStopOffset, &xpsNewGradientStop);

    // get the collection of gradient stops from the brush
    hr = brush->GetGradientStops (&stops);

    hr = stops->GetCount (&numStops);
    // there will never be less than two stops
    
    // insert the new stop so that the stops are sorted by offset
    // if an existing stop has the same offset as the new one,
    // overwrite the existing stop with the new stop.
    for (thisStopIdx = 0; thisStopIdx < (numStops-1); thisStopIdx++) {
        hr = stops->GetAt(thisStopIdx, &thisStop);
        hr = stops->GetAt(thisStopIdx+1, &nextStop);
    
        hr = thisStop->GetOffset (&thisStopOffset);
        hr = nextStop->GetOffset (&nextStopOffset);

        if (newStopOffset < thisStopOffset) {
            // insert at thisStopIdx
            stops->InsertAt(thisStopIdx, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        } 
        if ((newStopOffset > thisStopOffset) && (newStopOffset < nextStopOffset)) {
            // the new stop goes in between them
            stops->InsertAt (thisStopIdx+1, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        } 

        if (newStopOffset == thisStopOffset ) {
            // then overwrite the old one
            stops->SetAt (thisStopIdx, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        }

        if (newStopOffset == nextStopOffset ) {
            // then overwrite the old one
            stops->SetAt (thisStopIdx+1, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        }

        // on the last entry, see if this stop is greater than the last entry
        // in the collection. If so, append the new one to the end.
        if ((thisStopIdx == (numStops-2)) && (newStopOffset > nextStopOffset )) {
            // then overwrite the old one
            stops->Append ( xpsNewGradientStop );
            bUpdated = TRUE;
            break; // done, so leave loop
        }
        if (NULL != thisStop) {thisStop->Release(); thisStop = NULL;}
        if (NULL != nextStop) {nextStop->Release(); nextStop = NULL;}
    }
    if (NULL != thisStop) {thisStop->Release(); thisStop = NULL;}
    if (NULL != nextStop) {nextStop->Release(); nextStop = NULL;}

    // make sure that the new stop was put somewhere in the collection
    _ASSERT (bUpdated);
    return S_OK;
```



## <a name="related-topics"></a><span data-ttu-id="a9d6f-107">См. также</span><span class="sxs-lookup"><span data-stu-id="a9d6f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d6f-108">**Интерфейс Икспсомградиентстоп**</span><span class="sxs-lookup"><span data-stu-id="a9d6f-108">**IXpsOMGradientStop Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)
</dt> <dt>

[<span data-ttu-id="a9d6f-109">**Интерфейс Икспсомградиентстопколлектион**</span><span class="sxs-lookup"><span data-stu-id="a9d6f-109">**IXpsOMGradientStopCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)
</dt> </dl>

 

 



