---
description: ICE10 проверяет, что состояние объявления дочерних компонентов совпадает с родительским компонентом.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663678"
---
# <a name="ice10"></a><span data-ttu-id="62866-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="62866-103">ICE10</span></span>

<span data-ttu-id="62866-104">ICE10 проверяет, что состояние объявления дочерних компонентов совпадает с родительским компонентом.</span><span class="sxs-lookup"><span data-stu-id="62866-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="62866-105">Дочерняя функция может не запрещать объявление, пока ее родительский компонент допускает объявление.</span><span class="sxs-lookup"><span data-stu-id="62866-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="62866-106">Таким образом, следующее сочетание родительских и дочерних атрибутов является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="62866-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="62866-107">Это сочетание является недопустимым, поскольку оно бы отключило родительский элемент всякий раз, когда ожидается объявление родителя.</span><span class="sxs-lookup"><span data-stu-id="62866-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="62866-108">Однако обратная возможность разрешена.</span><span class="sxs-lookup"><span data-stu-id="62866-108">However, the reverse is allowed.</span></span> <span data-ttu-id="62866-109">Дочерний элемент может быть помечен в качестве предпочтительного, когда родительский элемент помечен для запрета объявления.</span><span class="sxs-lookup"><span data-stu-id="62866-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="62866-110">Пользовательское действие ICE10 определяет состояние родительского и дочернего компонентов из столбца Attributes таблицы [Feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="62866-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="62866-111">Обратите внимание, что можно установить состояние компонента равным 0, и его родительский или дочерний набор будет использовать или запретить объявление.</span><span class="sxs-lookup"><span data-stu-id="62866-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="62866-112">Результат</span><span class="sxs-lookup"><span data-stu-id="62866-112">Result</span></span>

<span data-ttu-id="62866-113">ICE10 отправляет сообщение об ошибке, если столбец Attributes таблицы [Features](feature-table.md) содержит несоответствие в состоянии объявления.</span><span class="sxs-lookup"><span data-stu-id="62866-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="62866-114">Пример</span><span class="sxs-lookup"><span data-stu-id="62866-114">Example</span></span>

<span data-ttu-id="62866-115">ICE10 отправляет следующее сообщение об ошибке для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="62866-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="62866-116">Обратите внимание, что в этом примере Microsoft Excel и Microsoft Word являются дочерними компонентами Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="62866-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="62866-117">Таблица [компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="62866-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="62866-118">Функция</span><span class="sxs-lookup"><span data-stu-id="62866-118">Feature</span></span> | <span data-ttu-id="62866-119">\_Родительский компонент функции</span><span class="sxs-lookup"><span data-stu-id="62866-119">Feature\_Parent</span></span> | <span data-ttu-id="62866-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62866-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="62866-121">Office</span><span class="sxs-lookup"><span data-stu-id="62866-121">Office</span></span>  | <span data-ttu-id="62866-122">NULL</span><span class="sxs-lookup"><span data-stu-id="62866-122">Null</span></span>            | <span data-ttu-id="62866-123">4</span><span class="sxs-lookup"><span data-stu-id="62866-123">4</span></span>          |
| <span data-ttu-id="62866-124">Excel</span><span class="sxs-lookup"><span data-stu-id="62866-124">Excel</span></span>   | <span data-ttu-id="62866-125">Office</span><span class="sxs-lookup"><span data-stu-id="62866-125">Office</span></span>          | <span data-ttu-id="62866-126">4</span><span class="sxs-lookup"><span data-stu-id="62866-126">4</span></span>          |
| <span data-ttu-id="62866-127">Word</span><span class="sxs-lookup"><span data-stu-id="62866-127">Word</span></span>    | <span data-ttu-id="62866-128">Office</span><span class="sxs-lookup"><span data-stu-id="62866-128">Office</span></span>          | <span data-ttu-id="62866-129">8</span><span class="sxs-lookup"><span data-stu-id="62866-129">8</span></span>          |



 

<span data-ttu-id="62866-130">В этом примере Word имеет значение запрет объявления, которое конфликтует с состоянием разрешения родительского элемента Office.</span><span class="sxs-lookup"><span data-stu-id="62866-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="62866-131">В некоторых случаях ICE10 отправляет следующую ошибку:</span><span class="sxs-lookup"><span data-stu-id="62866-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="62866-132">Это означает недопустимую ссылку на внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="62866-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="62866-133">Исправление заключается в том, чтобы дочерняя точка указывала на правильную родительскую функцию, или добавить запись для родительского компонента "Parent" в таблицу [компонентов](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="62866-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62866-134">См. также</span><span class="sxs-lookup"><span data-stu-id="62866-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62866-135">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="62866-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



