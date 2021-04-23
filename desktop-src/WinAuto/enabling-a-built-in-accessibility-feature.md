---
title: Включение встроенной функции специальных возможностей
ms.assetid: f97a445d-f93d-4462-bce5-d853f5076b9c
description: 'Дополнительные сведения: Включение встроенной функции специальных возможностей'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860b1410e48f5824923b8b16babb6bcd1527ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273084"
---
# <a name="enabling-a-built-in-accessibility-feature"></a><span data-ttu-id="33586-103">Включение встроенной функции специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="33586-103">Enabling a Built-in Accessibility Feature</span></span>

<span data-ttu-id="33586-104">В следующем фрагменте кода используется функция [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для включения функции фильтрации ввода:</span><span class="sxs-lookup"><span data-stu-id="33586-104">The following code fragment uses the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to enable the FilterKeys feature:</span></span>


```C++
FILTERKEYS fk; 
BOOL bSuccess; 
 
// Fill in the members of the FILTERKEYS structure.  
 
fk.cbSize = sizeof(FILTERKEYS); 
fk.dwFlags = (FKF_FILTERKEYSON | FKF_HOTKEYACTIVE | 
                       FKF_AVAILABLE | FKF_HOTKEYSOUND |
FKF_CLICKON); 
fk.iWaitMSec = 1000; 
fk.iDelayMSec = 1000; 
fk.iRepeatMSec = 500; 
fk.iBounceMSec = 0; 
 
// Call SystemParametersInfo with the SPI_SETFILTERKEYS flag.  
 
bSuccess = SystemParametersInfo(SPI_SETFILTERKEYS, 0, (LPVOID)
&fk, 0); 
```



 

 
