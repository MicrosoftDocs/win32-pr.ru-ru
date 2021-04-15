---
description: Лаунчкондитион таблица используется действием Лаунчкондитионс. Он содержит список условий, которые должны быть удовлетворены для начала установки.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Таблица Лаунчкондитион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682709"
---
# <a name="launchcondition-table"></a><span data-ttu-id="fed2a-104">Таблица Лаунчкондитион</span><span class="sxs-lookup"><span data-stu-id="fed2a-104">LaunchCondition Table</span></span>

<span data-ttu-id="fed2a-105">Лаунчкондитион таблица используется [действием лаунчкондитионс](launchconditions-action.md).</span><span class="sxs-lookup"><span data-stu-id="fed2a-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="fed2a-106">Он содержит список условий, которые должны быть удовлетворены для начала установки.</span><span class="sxs-lookup"><span data-stu-id="fed2a-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="fed2a-107">Таблица Лаунчкондитион содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="fed2a-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="fed2a-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="fed2a-108">Column</span></span>      | <span data-ttu-id="fed2a-109">Type</span><span class="sxs-lookup"><span data-stu-id="fed2a-109">Type</span></span>                       | <span data-ttu-id="fed2a-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="fed2a-110">Key</span></span> | <span data-ttu-id="fed2a-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="fed2a-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="fed2a-112">Условие</span><span class="sxs-lookup"><span data-stu-id="fed2a-112">Condition</span></span>   | [<span data-ttu-id="fed2a-113">Condition</span><span class="sxs-lookup"><span data-stu-id="fed2a-113">Condition</span></span>](condition.md) | <span data-ttu-id="fed2a-114">Да</span><span class="sxs-lookup"><span data-stu-id="fed2a-114">Y</span></span>   | <span data-ttu-id="fed2a-115">Нет</span><span class="sxs-lookup"><span data-stu-id="fed2a-115">N</span></span>        |
| <span data-ttu-id="fed2a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fed2a-116">Description</span></span> | [<span data-ttu-id="fed2a-117">Формате</span><span class="sxs-lookup"><span data-stu-id="fed2a-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="fed2a-118">Нет</span><span class="sxs-lookup"><span data-stu-id="fed2a-118">N</span></span>   | <span data-ttu-id="fed2a-119">Нет</span><span class="sxs-lookup"><span data-stu-id="fed2a-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fed2a-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="fed2a-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fed2a-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="fed2a-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="fed2a-122">Выражение, которое должно иметь значение true для начала установки.</span><span class="sxs-lookup"><span data-stu-id="fed2a-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="fed2a-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="fed2a-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fed2a-124">Локализуемый текст, отображаемый при сбое условия и необходимости завершения установки.</span><span class="sxs-lookup"><span data-stu-id="fed2a-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fed2a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fed2a-125">Remarks</span></span>

<span data-ttu-id="fed2a-126">Нельзя гарантировать порядок, в котором условия запуска оцениваются путем создания этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fed2a-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="fed2a-127">Если необходимо управлять порядком, в котором оцениваются условия, это следует делать с помощью настраиваемых действий типа 19 в установке.</span><span class="sxs-lookup"><span data-stu-id="fed2a-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="fed2a-128">Проверка</span><span class="sxs-lookup"><span data-stu-id="fed2a-128">Validation</span></span>

<dl>

[<span data-ttu-id="fed2a-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="fed2a-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fed2a-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="fed2a-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fed2a-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="fed2a-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fed2a-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="fed2a-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="fed2a-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="fed2a-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



