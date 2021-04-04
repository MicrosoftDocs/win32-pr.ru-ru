---
description: Строки списка не рассматриваются как отдельные элементы управления, но они являются частью списка, который выступает в качестве элемента управления. Таблица ListBox определяет значения для всех списков.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Таблица ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998796"
---
# <a name="listbox-table"></a><span data-ttu-id="02bf3-104">Таблица ListBox</span><span class="sxs-lookup"><span data-stu-id="02bf3-104">ListBox Table</span></span>

<span data-ttu-id="02bf3-105">Строки списка не рассматриваются как отдельные элементы управления, но они являются частью списка, который выступает в качестве элемента управления.</span><span class="sxs-lookup"><span data-stu-id="02bf3-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="02bf3-106">Таблица ListBox определяет значения для всех списков.</span><span class="sxs-lookup"><span data-stu-id="02bf3-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="02bf3-107">Таблица ListBox содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="02bf3-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="02bf3-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="02bf3-108">Column</span></span>   | <span data-ttu-id="02bf3-109">Type</span><span class="sxs-lookup"><span data-stu-id="02bf3-109">Type</span></span>                         | <span data-ttu-id="02bf3-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="02bf3-110">Key</span></span> | <span data-ttu-id="02bf3-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="02bf3-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="02bf3-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="02bf3-112">Property</span></span> | [<span data-ttu-id="02bf3-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="02bf3-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="02bf3-114">Да</span><span class="sxs-lookup"><span data-stu-id="02bf3-114">Y</span></span>   | <span data-ttu-id="02bf3-115">Нет</span><span class="sxs-lookup"><span data-stu-id="02bf3-115">N</span></span>        |
| <span data-ttu-id="02bf3-116">Заказ</span><span class="sxs-lookup"><span data-stu-id="02bf3-116">Order</span></span>    | [<span data-ttu-id="02bf3-117">Integer</span><span class="sxs-lookup"><span data-stu-id="02bf3-117">Integer</span></span>](integer.md)       | <span data-ttu-id="02bf3-118">Да</span><span class="sxs-lookup"><span data-stu-id="02bf3-118">Y</span></span>   | <span data-ttu-id="02bf3-119">Нет</span><span class="sxs-lookup"><span data-stu-id="02bf3-119">N</span></span>        |
| <span data-ttu-id="02bf3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="02bf3-120">Value</span></span>    | [<span data-ttu-id="02bf3-121">Формате</span><span class="sxs-lookup"><span data-stu-id="02bf3-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="02bf3-122">Нет</span><span class="sxs-lookup"><span data-stu-id="02bf3-122">N</span></span>   | <span data-ttu-id="02bf3-123">Нет</span><span class="sxs-lookup"><span data-stu-id="02bf3-123">N</span></span>        |
| <span data-ttu-id="02bf3-124">Текст</span><span class="sxs-lookup"><span data-stu-id="02bf3-124">Text</span></span>     | [<span data-ttu-id="02bf3-125">Формате</span><span class="sxs-lookup"><span data-stu-id="02bf3-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="02bf3-126">Нет</span><span class="sxs-lookup"><span data-stu-id="02bf3-126">N</span></span>   | <span data-ttu-id="02bf3-127">Да</span><span class="sxs-lookup"><span data-stu-id="02bf3-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02bf3-128">Столбцы</span><span class="sxs-lookup"><span data-stu-id="02bf3-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02bf3-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="02bf3-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="02bf3-130">Именованное свойство, которое должно быть привязано к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="02bf3-130">A named property to be tied to this item.</span></span> <span data-ttu-id="02bf3-131">Все элементы, привязанные к одному и тому же свойству, становятся частью одного списка.</span><span class="sxs-lookup"><span data-stu-id="02bf3-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="02bf3-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Порядок</span><span class="sxs-lookup"><span data-stu-id="02bf3-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="02bf3-133">Положительное целое число, используемое для определения порядка элементов, отображаемых в одном окне списка.</span><span class="sxs-lookup"><span data-stu-id="02bf3-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="02bf3-134">Если список определен как упорядоченный, то все элементы должны иметь значение заказа.</span><span class="sxs-lookup"><span data-stu-id="02bf3-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="02bf3-135">Целые числа не должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="02bf3-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="02bf3-136">Если список определен как неупорядоченный, то этот столбец игнорируется.</span><span class="sxs-lookup"><span data-stu-id="02bf3-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="02bf3-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="02bf3-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="02bf3-138">Строка значения, связанная с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="02bf3-138">The value string associated with this item.</span></span> <span data-ttu-id="02bf3-139">Если выбрать строку, связанному свойству присваивается это значение.</span><span class="sxs-lookup"><span data-stu-id="02bf3-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="02bf3-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="02bf3-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="02bf3-141">Локализуемый, видимый текст, который будет назначен элементу.</span><span class="sxs-lookup"><span data-stu-id="02bf3-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="02bf3-142">Если эта запись или весь столбец отсутствуют, по умолчанию используется соответствующая запись в поле значение.</span><span class="sxs-lookup"><span data-stu-id="02bf3-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02bf3-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02bf3-143">Remarks</span></span>

<span data-ttu-id="02bf3-144">Содержимое полей Value и Text форматируется функцией [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) при создании элемента управления, поэтому они могут содержать любое выражение, которое может интерпретировать функция **мсиформатрекорд** .</span><span class="sxs-lookup"><span data-stu-id="02bf3-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="02bf3-145">Форматирование происходит только при создании элемента управления и не обновляется, если свойство, вовлеченное в выражение, изменяется в течение жизненного цикла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="02bf3-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="02bf3-146">Проверка</span><span class="sxs-lookup"><span data-stu-id="02bf3-146">Validation</span></span>

<dl>

[<span data-ttu-id="02bf3-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="02bf3-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02bf3-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="02bf3-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02bf3-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="02bf3-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="02bf3-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="02bf3-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="02bf3-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="02bf3-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



