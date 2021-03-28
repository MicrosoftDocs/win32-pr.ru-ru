---
description: Не каждое устройство вывода поддерживает весь набор графических функций.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Получение возможностей принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984809"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="6ce16-103">Получение возможностей принтера</span><span class="sxs-lookup"><span data-stu-id="6ce16-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="6ce16-104">Не каждое устройство вывода поддерживает весь набор графических функций.</span><span class="sxs-lookup"><span data-stu-id="6ce16-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="6ce16-105">Например, из-за аппаратных ограничений большинство векторных плоттеров не поддерживает передачу битовых блоков.</span><span class="sxs-lookup"><span data-stu-id="6ce16-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="6ce16-106">Приложение может определить, поддерживает ли устройство определенную графическую функцию, вызвав функцию [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , указав соответствующий индекс и проверив возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6ce16-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="6ce16-107">В следующем примере показано, как приложение проверяет принтер, чтобы определить, поддерживает ли он передачу битовых блоков.</span><span class="sxs-lookup"><span data-stu-id="6ce16-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



