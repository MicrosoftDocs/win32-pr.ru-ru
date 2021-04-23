---
description: ICE72 проверяет, что невстроенные пользовательские действия не используются в таблице Адвтексекутесекуенце.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664267"
---
# <a name="ice72"></a><span data-ttu-id="db674-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="db674-103">ICE72</span></span>

<span data-ttu-id="db674-104">ICE72 проверяет, что невстроенные пользовательские действия не используются в [таблице адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="db674-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="db674-105">В таблице Адвтексекутесекуенце разрешается использовать пользовательские действия Type 19, Type 35 и 51 Type.</span><span class="sxs-lookup"><span data-stu-id="db674-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="db674-106">Если используются другие настраиваемые действия, объявление может работать не так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="db674-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="db674-107">Результат</span><span class="sxs-lookup"><span data-stu-id="db674-107">Result</span></span>

<span data-ttu-id="db674-108">ICE72 возвращает ошибку, если в таблице Адвексекутесекуенце используются пользовательские действия, отличные от типов 35, Type 51 и Type 19.</span><span class="sxs-lookup"><span data-stu-id="db674-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="db674-109">Пример</span><span class="sxs-lookup"><span data-stu-id="db674-109">Example</span></span>

<span data-ttu-id="db674-110">ICE72 сообщает об ошибке в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="db674-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="db674-111">Чтобы устранить эту ошибку, удалите "CA1" из таблицы Адвтексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="db674-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="db674-112">[Таблица адвтексекутесекуенце](advtexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="db674-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="db674-113">Действие</span><span class="sxs-lookup"><span data-stu-id="db674-113">Action</span></span> |
|--------|
| <span data-ttu-id="db674-114">CA1</span><span class="sxs-lookup"><span data-stu-id="db674-114">CA1</span></span>    |
| <span data-ttu-id="db674-115">CA35</span><span class="sxs-lookup"><span data-stu-id="db674-115">CA35</span></span>   |



 

<span data-ttu-id="db674-116">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="db674-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="db674-117">Действие</span><span class="sxs-lookup"><span data-stu-id="db674-117">Action</span></span> | <span data-ttu-id="db674-118">Тип</span><span class="sxs-lookup"><span data-stu-id="db674-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="db674-119">CA1</span><span class="sxs-lookup"><span data-stu-id="db674-119">CA1</span></span>    | <span data-ttu-id="db674-120">1</span><span class="sxs-lookup"><span data-stu-id="db674-120">1</span></span>    |
| <span data-ttu-id="db674-121">CA35</span><span class="sxs-lookup"><span data-stu-id="db674-121">CA35</span></span>   | <span data-ttu-id="db674-122">35</span><span class="sxs-lookup"><span data-stu-id="db674-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="db674-123">Таблицы, используемые во время выполнения</span><span class="sxs-lookup"><span data-stu-id="db674-123">Tables used during execution</span></span>

[<span data-ttu-id="db674-124">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="db674-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="db674-125">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="db674-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="db674-126">См. также</span><span class="sxs-lookup"><span data-stu-id="db674-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db674-127">Тип настраиваемого действия 19</span><span class="sxs-lookup"><span data-stu-id="db674-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="db674-128">Тип настраиваемого действия 35</span><span class="sxs-lookup"><span data-stu-id="db674-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="db674-129">Тип настраиваемого действия 51</span><span class="sxs-lookup"><span data-stu-id="db674-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="db674-130">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="db674-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



