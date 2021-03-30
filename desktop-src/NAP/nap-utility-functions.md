---
title: Функции служебной программы NAP
description: Следующие служебные функции поддерживают интерфейс API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775335"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="26852-103">Функции служебной программы NAP</span><span class="sxs-lookup"><span data-stu-id="26852-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="26852-104">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="26852-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="26852-105">Следующие служебные функции поддерживают интерфейс API NAP.</span><span class="sxs-lookup"><span data-stu-id="26852-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="26852-106">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределитель памяти COM (CoTaskMemAlloc и CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="26852-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="26852-107">В параметрах — выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="26852-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="26852-108">ВЫХОДНЫЕ параметры, выделенные вызываемым методом, освобожденные вызывающим объектом с помощью Котаскмем \* ()</span><span class="sxs-lookup"><span data-stu-id="26852-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="26852-109">ВХОДные и выходные параметры, вызываемые вызывающей стороной, освобождаются и перераспределяются вызывающей стороной в конечном итоге с помощью Котаскмем \* ()</span><span class="sxs-lookup"><span data-stu-id="26852-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="26852-110">В функциях Фрикскскс () все внедренные указатели также будут освобождены.</span><span class="sxs-lookup"><span data-stu-id="26852-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="26852-111">**аллокконнектионс**</span><span class="sxs-lookup"><span data-stu-id="26852-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="26852-112">**аллоккаунтедстринг**</span><span class="sxs-lookup"><span data-stu-id="26852-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="26852-113">**аллокфиксупинфо**</span><span class="sxs-lookup"><span data-stu-id="26852-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="26852-114">**фриконнектионс**</span><span class="sxs-lookup"><span data-stu-id="26852-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="26852-115">**фрикаунтедстринг**</span><span class="sxs-lookup"><span data-stu-id="26852-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="26852-116">**фрификсупинфо**</span><span class="sxs-lookup"><span data-stu-id="26852-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="26852-117">**фриисолатионинфо**</span><span class="sxs-lookup"><span data-stu-id="26852-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="26852-118">**фриисолатионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="26852-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="26852-119">**фринапкомпонентрегистратионинфоаррай**</span><span class="sxs-lookup"><span data-stu-id="26852-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="26852-120">**фринетворксох**</span><span class="sxs-lookup"><span data-stu-id="26852-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="26852-121">**фриприватедата**</span><span class="sxs-lookup"><span data-stu-id="26852-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="26852-122">**фрисох**</span><span class="sxs-lookup"><span data-stu-id="26852-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="26852-123">**фрисохаттрибутевалуе**</span><span class="sxs-lookup"><span data-stu-id="26852-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="26852-124">**фрисистемхеалсажентстате**</span><span class="sxs-lookup"><span data-stu-id="26852-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="26852-125">**инитиализенапажентнотифиер**</span><span class="sxs-lookup"><span data-stu-id="26852-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="26852-126">**унинитиализенапажентнотифиер**</span><span class="sxs-lookup"><span data-stu-id="26852-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




