---
title: Перечисление установленных драйверов записи
description: Перечисление установленных драйверов записи
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- Функция Капжетдривердескриптион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a053b2de7a69a712914926dbd2ab72be9d1732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986575"
---
# <a name="enumerating-installed-capture-drivers"></a><span data-ttu-id="af74c-104">Перечисление установленных драйверов записи</span><span class="sxs-lookup"><span data-stu-id="af74c-104">Enumerating Installed Capture Drivers</span></span>

<span data-ttu-id="af74c-105">В следующем примере функция [**капжетдривердескриптион**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) используется для получения имен и версий установленных драйверов записи.</span><span class="sxs-lookup"><span data-stu-id="af74c-105">The following example uses the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function to obtain the names and versions of the installed capture drivers.</span></span>


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="af74c-106">См. также</span><span class="sxs-lookup"><span data-stu-id="af74c-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af74c-107">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="af74c-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




