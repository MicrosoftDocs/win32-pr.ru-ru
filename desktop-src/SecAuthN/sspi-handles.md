---
description: Содержит список дескрипторов, используемых API-интерфейсом SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Дескрипторы SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fadebea7ff6b32f0058106595718a24d589854a662ef7b504ce6d7e8e5bc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916973"
---
# <a name="sspi-handles"></a>Дескрипторы SSPI

SSPI использует следующие типы дескрипторов и указатель на эти дескрипторы:

-   **Сечандле** и **псечандле**
-   **Кредхандле** и **пкредхандле**
-   **Кткссандле** и **пкткссандле**

Эти типы обработчиков и указатели на эти типы обработчиков определяются следующим образом.


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



