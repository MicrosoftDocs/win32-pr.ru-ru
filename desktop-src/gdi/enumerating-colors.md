---
description: Вы можете определить, сколько цветов поддерживает устройство, и что они представляют, извлекая число цветов для устройства и перечисляя цвета сплошных перьев.
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: Перечисление цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984968"
---
# <a name="enumerating-colors"></a><span data-ttu-id="521e1-103">Перечисление цветов</span><span class="sxs-lookup"><span data-stu-id="521e1-103">Enumerating Colors</span></span>

<span data-ttu-id="521e1-104">Вы можете определить, сколько цветов поддерживает устройство, и что они представляют, извлекая число цветов для устройства и перечисляя цвета сплошных перьев.</span><span class="sxs-lookup"><span data-stu-id="521e1-104">You can determine how many colors a device supports and what those colors are by retrieving the count of colors for the device and enumerating the colors of the solid pens.</span></span> <span data-ttu-id="521e1-105">Чтобы получить количество цветов, используйте функцию [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) со значением нумколорс.</span><span class="sxs-lookup"><span data-stu-id="521e1-105">To retrieve the number of colors, use the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function with the NUMCOLORS value.</span></span> <span data-ttu-id="521e1-106">Чтобы перечислить сплошные перья, используйте функцию [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) и соответствующую функцию обратного вызова, которая получает сведения о каждом пере.</span><span class="sxs-lookup"><span data-stu-id="521e1-106">To enumerate solid pens, use the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function and a corresponding callback function that receives information about each pen.</span></span>


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 



