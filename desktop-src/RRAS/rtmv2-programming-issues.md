---
title: Проблемы программирования RTMv2
description: Функции RTMv2 написаны с помощью следующих допущений.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Проблемы программирования, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329843"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="49176-104">Проблемы программирования RTMv2</span><span class="sxs-lookup"><span data-stu-id="49176-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="49176-105">Функции RTMv2 написаны с помощью следующих допущений.</span><span class="sxs-lookup"><span data-stu-id="49176-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="49176-106">Функции RTMv2 не распределяют память для клиента.</span><span class="sxs-lookup"><span data-stu-id="49176-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="49176-107">Клиент всегда должен выделить память.</span><span class="sxs-lookup"><span data-stu-id="49176-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="49176-108">При отмене регистрации клиента он должен выполнять операции очистки, такие как освобождение всей выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="49176-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="49176-109">Клиенты должны правильно освобождать дескрипторы; утечки памяти могут возникать, если клиент не следит за этой практикой.</span><span class="sxs-lookup"><span data-stu-id="49176-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




