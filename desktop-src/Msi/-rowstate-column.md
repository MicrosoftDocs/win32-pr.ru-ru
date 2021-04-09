---
description: Зарезервированное имя столбца \_ RowState представляет непостоянное состояние, связанное с каждой строкой таблицы в таблице базы данных установщика.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState столбец
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080690"
---
# <a name="_rowstate-column"></a><span data-ttu-id="583b0-103">\_RowState, столбец</span><span class="sxs-lookup"><span data-stu-id="583b0-103">\_RowState Column</span></span>

<span data-ttu-id="583b0-104">Зарезервированное имя столбца \_ RowState представляет непостоянное состояние, связанное с каждой строкой таблицы в таблице базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="583b0-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="583b0-105">Псевдо-столбец имеет тип [Integer](integer.md), а значение состоит из набора битовых флагов.</span><span class="sxs-lookup"><span data-stu-id="583b0-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="583b0-106">Все биты доступны для чтения, но можно задать только UserInfo и временные биты.</span><span class="sxs-lookup"><span data-stu-id="583b0-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="583b0-107">Эти данные доступны только при условии, что таблицы заблокированы или используются (то есть пока существует представление, содержащее таблицы).</span><span class="sxs-lookup"><span data-stu-id="583b0-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="583b0-108">В следующей таблице показаны атрибуты, которые может иметь строка.</span><span class="sxs-lookup"><span data-stu-id="583b0-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="583b0-109">Имя</span><span class="sxs-lookup"><span data-stu-id="583b0-109">Name</span></span>           | <span data-ttu-id="583b0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="583b0-110">Value</span></span> | <span data-ttu-id="583b0-111">Значение</span><span class="sxs-lookup"><span data-stu-id="583b0-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="583b0-112">ираусеринфо</span><span class="sxs-lookup"><span data-stu-id="583b0-112">iraUserInfo</span></span>    | <span data-ttu-id="583b0-113">0x01</span><span class="sxs-lookup"><span data-stu-id="583b0-113">0x01</span></span>  | <span data-ttu-id="583b0-114">Атрибут предназначен для внешнего использования.</span><span class="sxs-lookup"><span data-stu-id="583b0-114">The attribute is for external use.</span></span> <span data-ttu-id="583b0-115">Это значение можно обновить.</span><span class="sxs-lookup"><span data-stu-id="583b0-115">This value can be updated.</span></span>  |
| <span data-ttu-id="583b0-116">иратемпорари</span><span class="sxs-lookup"><span data-stu-id="583b0-116">iraTemporary</span></span>   | <span data-ttu-id="583b0-117">0x02</span><span class="sxs-lookup"><span data-stu-id="583b0-117">0x02</span></span>  | <span data-ttu-id="583b0-118">Строка не является постоянной.</span><span class="sxs-lookup"><span data-stu-id="583b0-118">The row is not persistent.</span></span> <span data-ttu-id="583b0-119">Это значение можно обновить.</span><span class="sxs-lookup"><span data-stu-id="583b0-119">This value can be updated.</span></span>          |
| <span data-ttu-id="583b0-120">ирамодифиед</span><span class="sxs-lookup"><span data-stu-id="583b0-120">iraModified</span></span>    | <span data-ttu-id="583b0-121">0x04</span><span class="sxs-lookup"><span data-stu-id="583b0-121">0x04</span></span>  | <span data-ttu-id="583b0-122">Строка была обновлена.</span><span class="sxs-lookup"><span data-stu-id="583b0-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="583b0-123">ираинсертед</span><span class="sxs-lookup"><span data-stu-id="583b0-123">iraInserted</span></span>    | <span data-ttu-id="583b0-124">0x08</span><span class="sxs-lookup"><span data-stu-id="583b0-124">0x08</span></span>  | <span data-ttu-id="583b0-125">Строка была вставлена.</span><span class="sxs-lookup"><span data-stu-id="583b0-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="583b0-126">ирамержефаилед</span><span class="sxs-lookup"><span data-stu-id="583b0-126">iraMergeFailed</span></span> | <span data-ttu-id="583b0-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="583b0-127">0x0F</span></span>  | <span data-ttu-id="583b0-128">Предпринята попытка выполнить слияние с неидентичными неключевыми данными.</span><span class="sxs-lookup"><span data-stu-id="583b0-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="583b0-129">Биты с 6 по 8 зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="583b0-129">Bits 6 through 8 are reserved.</span></span>

 

 



