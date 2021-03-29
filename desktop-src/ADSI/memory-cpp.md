---
title: Свободной. CPP
description: В примере компонента поставщика пример кода, отображающий выделение памяти и освобождение ресурсов, находится в памяти. cpp. Поддерживаемые подпрограммы перечислены в следующей таблице.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654117"
---
# <a name="memorycpp"></a><span data-ttu-id="a1e81-104">Свободной. CPP</span><span class="sxs-lookup"><span data-stu-id="a1e81-104">MEMORY.CPP</span></span>

<span data-ttu-id="a1e81-105">В примере компонента поставщика пример кода, отображающий выделение памяти и освобождение ресурсов, находится в памяти. cpp.</span><span class="sxs-lookup"><span data-stu-id="a1e81-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="a1e81-106">Поддерживаемые подпрограммы перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a1e81-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="a1e81-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a1e81-107">Item</span></span>                | <span data-ttu-id="a1e81-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a1e81-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a1e81-109">**аллокпровмем**</span><span class="sxs-lookup"><span data-stu-id="a1e81-109">**AllocProvMem**</span></span>    | <span data-ttu-id="a1e81-110">Выделение указанной памяти.</span><span class="sxs-lookup"><span data-stu-id="a1e81-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="a1e81-111">**фрипровмем**</span><span class="sxs-lookup"><span data-stu-id="a1e81-111">**FreeProvMem**</span></span>     | <span data-ttu-id="a1e81-112">Указана свободная память.</span><span class="sxs-lookup"><span data-stu-id="a1e81-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="a1e81-113">**реаллокпровмем**</span><span class="sxs-lookup"><span data-stu-id="a1e81-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="a1e81-114">Выделение непрерывной памяти.</span><span class="sxs-lookup"><span data-stu-id="a1e81-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="a1e81-115">**аллокпровстр**</span><span class="sxs-lookup"><span data-stu-id="a1e81-115">**AllocProvStr**</span></span>    | <span data-ttu-id="a1e81-116">Выделение строки LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="a1e81-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="a1e81-117">**фрипровстр**</span><span class="sxs-lookup"><span data-stu-id="a1e81-117">**FreeProvStr**</span></span>     | <span data-ttu-id="a1e81-118">Свободная строка, если она еще не освобождена.</span><span class="sxs-lookup"><span data-stu-id="a1e81-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="a1e81-119">**реаллокпровстр**</span><span class="sxs-lookup"><span data-stu-id="a1e81-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="a1e81-120">Выделение непрерывной памяти.</span><span class="sxs-lookup"><span data-stu-id="a1e81-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="a1e81-121">**проваллокстринг**</span><span class="sxs-lookup"><span data-stu-id="a1e81-121">**ProvAllocString**</span></span> | <span data-ttu-id="a1e81-122">Проверяет строку и первый параметр.</span><span class="sxs-lookup"><span data-stu-id="a1e81-122">Verifies string and first parameter.</span></span> <span data-ttu-id="a1e81-123">Если ОК, выполнит выделение.</span><span class="sxs-lookup"><span data-stu-id="a1e81-123">If OK, then performs allocation.</span></span> |



 

 

 




