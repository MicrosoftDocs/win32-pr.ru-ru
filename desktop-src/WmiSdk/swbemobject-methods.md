---
description: Объект SWbemObject предоставляет следующие методы.
ms.assetid: F1534655-488C-4C78-BFE3-B7477149458B
ms.tgt_platform: multiple
title: Методы SWbemObject
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4061782aa586bb3d628a7dd3b81254288da03d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898546"
---
# <a name="swbemobject-methods"></a><span data-ttu-id="ae5c5-103">Методы SWbemObject</span><span class="sxs-lookup"><span data-stu-id="ae5c5-103">SWbemObject Methods</span></span>

<span data-ttu-id="ae5c5-104">Объект [**SWbemObject**](swbemobject.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ae5c5-104">The [**SWbemObject**](swbemobject.md) object exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ae5c5-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ae5c5-105">In this section</span></span>

-   [<span data-ttu-id="ae5c5-106">**Метод сопоставления \_**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-106">**Associators\_ method**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="ae5c5-107">**\_Метод ассоЦиаторсасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-107">**AssociatorsAsync\_ method**</span></span>](swbemobject-associatorsasync-.md)
-   [<span data-ttu-id="ae5c5-108">**Clone, \_ метод**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-108">**Clone\_ method**</span></span>](swbemobject-clone-.md)
-   [<span data-ttu-id="ae5c5-109">**\_Метод CompareTo**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-109">**CompareTo\_ method**</span></span>](swbemobject-compareto-.md)
-   [<span data-ttu-id="ae5c5-110">**\_Метод Delete**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-110">**Delete\_ method**</span></span>](swbemobject-delete-.md)
-   [<span data-ttu-id="ae5c5-111">**\_Метод DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-111">**DeleteAsync\_ method**</span></span>](swbemobject-deleteasync-.md)
-   [<span data-ttu-id="ae5c5-112">**\_Метод ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-112">**ExecMethod\_ method**</span></span>](swbemobject-execmethod-.md)
-   [<span data-ttu-id="ae5c5-113">**\_Метод ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-113">**ExecMethodAsync\_ method**</span></span>](swbemobject-execmethodasync-.md)
-   [<span data-ttu-id="ae5c5-114">**\_Метод жетобжекттекст**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-114">**GetObjectText\_ method**</span></span>](swbemobject-getobjecttext-.md)
-   [<span data-ttu-id="ae5c5-115">**Instances, \_ метод**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-115">**Instances\_ method**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="ae5c5-116">**\_Метод инстанцесасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-116">**InstancesAsync\_ method**</span></span>](swbemobject-instancesasync-.md)
-   [<span data-ttu-id="ae5c5-117">**\_Метод размещения**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-117">**Put\_ method**</span></span>](swbemobject-put-.md)
-   [<span data-ttu-id="ae5c5-118">**\_Метод путасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-118">**PutAsync\_ method**</span></span>](swbemobject-putasync-.md)
-   [<span data-ttu-id="ae5c5-119">**Метод References \_**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-119">**References\_ method**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="ae5c5-120">**\_Метод референцесасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-120">**ReferencesAsync\_ method**</span></span>](swbemobject-referencesasync-.md)
-   [<span data-ttu-id="ae5c5-121">**\_Метод спавндериведкласс**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-121">**SpawnDerivedClass\_ method**</span></span>](swbemobject-spawnderivedclass-.md)
-   [<span data-ttu-id="ae5c5-122">**\_Метод спавнинстанце**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-122">**SpawnInstance\_ method**</span></span>](swbemobject-spawninstance-.md)
-   [<span data-ttu-id="ae5c5-123">**Метод подклассов \_**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-123">**Subclasses\_ method**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="ae5c5-124">**\_Метод субклассесасинк**</span><span class="sxs-lookup"><span data-stu-id="ae5c5-124">**SubclassesAsync\_ method**</span></span>](swbemobject-subclassesasync-.md)

 

 



