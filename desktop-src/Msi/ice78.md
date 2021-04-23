---
description: ICE78 проверяет, что таблица Адвтуисекуенце либо не существует, либо пуста. Это необходимо, поскольку во время рекламы не допускается использование пользовательского интерфейса.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154814"
---
# <a name="ice78"></a><span data-ttu-id="e4dd1-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="e4dd1-104">ICE78</span></span>

<span data-ttu-id="e4dd1-105">ICE78 проверяет, что [Таблица адвтуисекуенце](advtuisequence-table.md) либо не существует, либо пуста.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="e4dd1-106">Это необходимо, поскольку во время рекламы не допускается использование пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="e4dd1-107">Результат</span><span class="sxs-lookup"><span data-stu-id="e4dd1-107">Result</span></span>

<span data-ttu-id="e4dd1-108">ICE78 отправляет сообщение об ошибке, если таблица Адвтуисекуенце существует и не пуста.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="e4dd1-109">Пример</span><span class="sxs-lookup"><span data-stu-id="e4dd1-109">Example</span></span>

<span data-ttu-id="e4dd1-110">ICE78 сообщает о следующей ошибке в примере:</span><span class="sxs-lookup"><span data-stu-id="e4dd1-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="e4dd1-111">Действие "Action1 превышают" найдено в таблице Адвтуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="e4dd1-112">Во время рекламы не допускается использование пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="e4dd1-113">Поэтому таблица Адвтуисекуенце должна быть пустой или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="e4dd1-114">[Таблица адвтуисекуенце](advtuisequence-table.md)(частичная)</span><span class="sxs-lookup"><span data-stu-id="e4dd1-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="e4dd1-115">Действие</span><span class="sxs-lookup"><span data-stu-id="e4dd1-115">Action</span></span>  | <span data-ttu-id="e4dd1-116">Условие</span><span class="sxs-lookup"><span data-stu-id="e4dd1-116">Condition</span></span> | <span data-ttu-id="e4dd1-117">Последовательность</span><span class="sxs-lookup"><span data-stu-id="e4dd1-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="e4dd1-118">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="e4dd1-118">Action1</span></span> | <span data-ttu-id="e4dd1-119">true</span><span class="sxs-lookup"><span data-stu-id="e4dd1-119">TRUE</span></span>      | <span data-ttu-id="e4dd1-120">1</span><span class="sxs-lookup"><span data-stu-id="e4dd1-120">1</span></span>        |



 

<span data-ttu-id="e4dd1-121">Чтобы устранить эту ошибку, удалите из таблицы значение "Action1 превышают" или удалите таблицу.</span><span class="sxs-lookup"><span data-stu-id="e4dd1-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4dd1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e4dd1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4dd1-123">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e4dd1-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



