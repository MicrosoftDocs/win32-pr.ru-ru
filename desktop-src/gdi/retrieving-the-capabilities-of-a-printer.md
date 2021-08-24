---
description: Не каждое устройство вывода поддерживает весь набор графических функций.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Получение возможностей принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779064"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>Получение возможностей принтера

Не каждое устройство вывода поддерживает весь набор графических функций. Например, из-за аппаратных ограничений большинство векторных плоттеров не поддерживает передачу битовых блоков. Приложение может определить, поддерживает ли устройство определенную графическую функцию, вызвав функцию [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , указав соответствующий индекс и проверив возвращаемое значение.

В следующем примере показано, как приложение проверяет принтер, чтобы определить, поддерживает ли он передачу битовых блоков.


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



 

 



