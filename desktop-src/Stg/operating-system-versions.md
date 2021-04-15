---
title: Версии операционной системы
description: Этот тип данных DWORD должен содержать тип операционной системы в слове высокого порядка и номер версии операционной системы в младшем слове. Возможные значения для операционной системы перечислены в следующей таблице.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Структурированное хранилище версий операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661739"
---
# <a name="operating-system-versions"></a>Версии операционной системы

Этот тип данных **DWORD** должен содержать тип операционной системы в слове высокого порядка и номер версии операционной системы в младшем слове. Возможные значения для операционной системы перечислены в следующей таблице.



| Операционная система       | Значение  |
|------------------------|--------|
| 32-разрядная версия Windows (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| 16-разрядная версия Windows (Win16) | 0x0000 |



 

Для операционных систем Microsoft Windows версия операционной системы — это младшее слово, возвращаемое функцией [**инверсии**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) . В следующем примере кода для Microsoft Windows правильно задается версия исходной операционной системы.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 