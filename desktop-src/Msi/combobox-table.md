---
description: Строки поля со списком не рассматриваются как отдельные элементы управления. они являются частью одного поля со списком, которое функционирует как элемент управления. В этой таблице перечислены значения для каждого поля со списком.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Таблица ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651007"
---
# <a name="combobox-table"></a><span data-ttu-id="6b30c-104">Таблица ComboBox</span><span class="sxs-lookup"><span data-stu-id="6b30c-104">ComboBox Table</span></span>

<span data-ttu-id="6b30c-105">Строки поля со списком не рассматриваются как отдельные элементы управления. они являются частью одного поля со списком, которое функционирует как элемент управления.</span><span class="sxs-lookup"><span data-stu-id="6b30c-105">The lines of a combo box are not treated as individual controls; they are part of a single combo box that functions as a control.</span></span> <span data-ttu-id="6b30c-106">В этой таблице перечислены значения для каждого поля со списком.</span><span class="sxs-lookup"><span data-stu-id="6b30c-106">This table lists the values for each combo box.</span></span>

<span data-ttu-id="6b30c-107">Таблица ComboBox содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="6b30c-107">The ComboBox table has the following columns.</span></span>



| <span data-ttu-id="6b30c-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="6b30c-108">Column</span></span>   | <span data-ttu-id="6b30c-109">Type</span><span class="sxs-lookup"><span data-stu-id="6b30c-109">Type</span></span>                         | <span data-ttu-id="6b30c-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="6b30c-110">Key</span></span> | <span data-ttu-id="6b30c-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6b30c-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="6b30c-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="6b30c-112">Property</span></span> | [<span data-ttu-id="6b30c-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6b30c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="6b30c-114">Да</span><span class="sxs-lookup"><span data-stu-id="6b30c-114">Y</span></span>   | <span data-ttu-id="6b30c-115">Нет</span><span class="sxs-lookup"><span data-stu-id="6b30c-115">N</span></span>        |
| <span data-ttu-id="6b30c-116">Заказ</span><span class="sxs-lookup"><span data-stu-id="6b30c-116">Order</span></span>    | [<span data-ttu-id="6b30c-117">Integer</span><span class="sxs-lookup"><span data-stu-id="6b30c-117">Integer</span></span>](integer.md)       | <span data-ttu-id="6b30c-118">Да</span><span class="sxs-lookup"><span data-stu-id="6b30c-118">Y</span></span>   | <span data-ttu-id="6b30c-119">Нет</span><span class="sxs-lookup"><span data-stu-id="6b30c-119">N</span></span>        |
| <span data-ttu-id="6b30c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6b30c-120">Value</span></span>    | [<span data-ttu-id="6b30c-121">Формате</span><span class="sxs-lookup"><span data-stu-id="6b30c-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="6b30c-122">Нет</span><span class="sxs-lookup"><span data-stu-id="6b30c-122">N</span></span>   | <span data-ttu-id="6b30c-123">Нет</span><span class="sxs-lookup"><span data-stu-id="6b30c-123">N</span></span>        |
| <span data-ttu-id="6b30c-124">Текст</span><span class="sxs-lookup"><span data-stu-id="6b30c-124">Text</span></span>     | [<span data-ttu-id="6b30c-125">Text</span><span class="sxs-lookup"><span data-stu-id="6b30c-125">Text</span></span>](text.md)             | <span data-ttu-id="6b30c-126">Нет</span><span class="sxs-lookup"><span data-stu-id="6b30c-126">N</span></span>   | <span data-ttu-id="6b30c-127">Да</span><span class="sxs-lookup"><span data-stu-id="6b30c-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6b30c-128">Столбцы</span><span class="sxs-lookup"><span data-stu-id="6b30c-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6b30c-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="6b30c-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="6b30c-130">Именованное свойство, которое должно быть привязано к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="6b30c-130">A named property to be tied to this item.</span></span> <span data-ttu-id="6b30c-131">Все элементы, привязанные к одному и тому же свойству, становятся частью одного поля со списком.</span><span class="sxs-lookup"><span data-stu-id="6b30c-131">All the items tied to the same property become part of the same combo box.</span></span>

</dd> <dt>

<span data-ttu-id="6b30c-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Порядок</span><span class="sxs-lookup"><span data-stu-id="6b30c-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="6b30c-133">Положительное целое число, используемое для определения порядка элементов, отображаемых в одном списке полей со списком.</span><span class="sxs-lookup"><span data-stu-id="6b30c-133">A positive integer used to determine the ordering of the items that appear in a single combo box list.</span></span> <span data-ttu-id="6b30c-134">Целые числа не должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="6b30c-134">The integers do not have to be consecutive.</span></span> <span data-ttu-id="6b30c-135">Если поле со списком определено как упорядоченное, то все элементы должны иметь значение заказа.</span><span class="sxs-lookup"><span data-stu-id="6b30c-135">If a combo box is defined as ordered, then all the items should have an Order value.</span></span> <span data-ttu-id="6b30c-136">Если поле со списком определено как неупорядоченное, то этот столбец игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6b30c-136">If the combo box is defined as unordered, then this column is ignored.</span></span>

<span data-ttu-id="6b30c-137">Только положительные числа.</span><span class="sxs-lookup"><span data-stu-id="6b30c-137">Positive numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="6b30c-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="6b30c-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="6b30c-139">Строка значения, связанная с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="6b30c-139">The value string associated with this item.</span></span> <span data-ttu-id="6b30c-140">При выборе этой строки в поле со списком связанное свойство (указанное в свойстве) задается этому значению.</span><span class="sxs-lookup"><span data-stu-id="6b30c-140">Selecting this line of the combo box sets the associated property (specified in Property) to this value.</span></span>

</dd> <dt>

<span data-ttu-id="6b30c-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="6b30c-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="6b30c-142">Видимый, локализуемый текст, назначаемый элементу.</span><span class="sxs-lookup"><span data-stu-id="6b30c-142">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="6b30c-143">Если эта запись или весь столбец отсутствуют, по умолчанию используется запись в поле значение.</span><span class="sxs-lookup"><span data-stu-id="6b30c-143">If this entry or the entire column is missing, then the text defaults to the entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b30c-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b30c-144">Remarks</span></span>

<span data-ttu-id="6b30c-145">Содержимое полей Value и Text форматируется функцией [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) при создании элемента управления, поэтому они могут содержать любое выражение, которое может интерпретировать функция **мсиформатрекорд** .</span><span class="sxs-lookup"><span data-stu-id="6b30c-145">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="6b30c-146">Форматирование происходит только при создании элемента управления и не обновляется, если свойство, вовлеченное в выражение, изменяется в течение жизненного цикла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6b30c-146">The formatting occurs only when the control is created and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="6b30c-147">Проверка</span><span class="sxs-lookup"><span data-stu-id="6b30c-147">Validation</span></span>

<dl>

[<span data-ttu-id="6b30c-148">ICE03</span><span class="sxs-lookup"><span data-stu-id="6b30c-148">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6b30c-149">ICE06</span><span class="sxs-lookup"><span data-stu-id="6b30c-149">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6b30c-150">ICE17</span><span class="sxs-lookup"><span data-stu-id="6b30c-150">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="6b30c-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="6b30c-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



