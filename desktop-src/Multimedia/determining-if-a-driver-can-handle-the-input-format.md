---
title: Определение того, может ли драйвер управлять входным форматом
description: Определение того, может ли драйвер управлять входным форматом
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Диспетчер сжатия видео (ВКМ), формат ввода
- ВКМ (диспетчер сжатия видео), формат ввода
- Макрос Икдравкуери
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497294"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Определение того, может ли драйвер управлять входным форматом

В следующем примере показано, как проверить формат ввода с помощью макроса [**икдравкуери**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




