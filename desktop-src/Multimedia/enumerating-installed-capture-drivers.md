---
title: Перечисление установленных драйверов записи
description: Перечисление установленных драйверов записи
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- Функция Капжетдривердескриптион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988653"
---
# <a name="enumerating-installed-capture-drivers"></a>Перечисление установленных драйверов записи

В следующем примере функция [**капжетдривердескриптион**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) используется для получения имен и версий установленных драйверов записи.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




