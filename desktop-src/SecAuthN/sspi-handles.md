---
description: Содержит список дескрипторов, используемых API-интерфейсом SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Дескрипторы SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664159"
---
# <a name="sspi-handles"></a><span data-ttu-id="c7a4d-103">Дескрипторы SSPI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-103">SSPI Handles</span></span>

<span data-ttu-id="c7a4d-104">SSPI использует следующие типы дескрипторов и указатель на эти дескрипторы:</span><span class="sxs-lookup"><span data-stu-id="c7a4d-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="c7a4d-105">**Сечандле** и **псечандле**</span><span class="sxs-lookup"><span data-stu-id="c7a4d-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="c7a4d-106">**Кредхандле** и **пкредхандле**</span><span class="sxs-lookup"><span data-stu-id="c7a4d-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="c7a4d-107">**Кткссандле** и **пкткссандле**</span><span class="sxs-lookup"><span data-stu-id="c7a4d-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="c7a4d-108">Эти типы обработчиков и указатели на эти типы обработчиков определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-108">These handle types and pointers to these handle types are defined as follows.</span></span>


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



 

 



