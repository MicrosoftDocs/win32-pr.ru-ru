---
description: Строки ListView не рассматриваются как отдельные элементы управления, но они являются частью ListView, который функционирует как элемент управления. Таблица ListView определяет значения для всех элементов ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Таблица ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683276"
---
# <a name="listview-table"></a><span data-ttu-id="752b7-104">Таблица ListView</span><span class="sxs-lookup"><span data-stu-id="752b7-104">ListView Table</span></span>

<span data-ttu-id="752b7-105">Строки ListView не рассматриваются как отдельные элементы управления, но они являются частью ListView, который функционирует как элемент управления.</span><span class="sxs-lookup"><span data-stu-id="752b7-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="752b7-106">Таблица ListView определяет значения для всех элементов ListView.</span><span class="sxs-lookup"><span data-stu-id="752b7-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="752b7-107">Таблица ListView содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="752b7-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="752b7-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="752b7-108">Column</span></span>   | <span data-ttu-id="752b7-109">Type</span><span class="sxs-lookup"><span data-stu-id="752b7-109">Type</span></span>                         | <span data-ttu-id="752b7-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="752b7-110">Key</span></span> | <span data-ttu-id="752b7-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="752b7-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="752b7-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="752b7-112">Property</span></span> | [<span data-ttu-id="752b7-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="752b7-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="752b7-114">Да</span><span class="sxs-lookup"><span data-stu-id="752b7-114">Y</span></span>   | <span data-ttu-id="752b7-115">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-115">N</span></span>        |
| <span data-ttu-id="752b7-116">Заказ</span><span class="sxs-lookup"><span data-stu-id="752b7-116">Order</span></span>    | [<span data-ttu-id="752b7-117">Integer</span><span class="sxs-lookup"><span data-stu-id="752b7-117">Integer</span></span>](integer.md)       | <span data-ttu-id="752b7-118">Да</span><span class="sxs-lookup"><span data-stu-id="752b7-118">Y</span></span>   | <span data-ttu-id="752b7-119">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-119">N</span></span>        |
| <span data-ttu-id="752b7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="752b7-120">Value</span></span>    | [<span data-ttu-id="752b7-121">Формате</span><span class="sxs-lookup"><span data-stu-id="752b7-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="752b7-122">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-122">N</span></span>   | <span data-ttu-id="752b7-123">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-123">N</span></span>        |
| <span data-ttu-id="752b7-124">Текст</span><span class="sxs-lookup"><span data-stu-id="752b7-124">Text</span></span>     | [<span data-ttu-id="752b7-125">Формате</span><span class="sxs-lookup"><span data-stu-id="752b7-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="752b7-126">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-126">N</span></span>   | <span data-ttu-id="752b7-127">Да</span><span class="sxs-lookup"><span data-stu-id="752b7-127">Y</span></span>        |
| <span data-ttu-id="752b7-128">Двоичный\_</span><span class="sxs-lookup"><span data-stu-id="752b7-128">Binary\_</span></span> | [<span data-ttu-id="752b7-129">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="752b7-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="752b7-130">Нет</span><span class="sxs-lookup"><span data-stu-id="752b7-130">N</span></span>   | <span data-ttu-id="752b7-131">Да</span><span class="sxs-lookup"><span data-stu-id="752b7-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="752b7-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="752b7-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="752b7-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Свойства</span><span class="sxs-lookup"><span data-stu-id="752b7-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="752b7-134">Именованное свойство, которое должно быть привязано к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="752b7-134">A named property to be tied to this item.</span></span> <span data-ttu-id="752b7-135">Все элементы, привязанные к одному и тому же свойству, становятся частью одного и того же ListView.</span><span class="sxs-lookup"><span data-stu-id="752b7-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Порядок</span><span class="sxs-lookup"><span data-stu-id="752b7-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="752b7-137">Положительное целое число, используемое для определения порядка элементов, отображаемых в одном списке ListView.</span><span class="sxs-lookup"><span data-stu-id="752b7-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="752b7-138">Целые числа не должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="752b7-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="752b7-139">Если ListView определен как упорядоченный, то все элементы должны иметь значение упорядочения.</span><span class="sxs-lookup"><span data-stu-id="752b7-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="752b7-140">Если ListView определен как неупорядоченный, этот столбец игнорируется.</span><span class="sxs-lookup"><span data-stu-id="752b7-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="752b7-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="752b7-142">Строка значения, связанная с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="752b7-142">The value string associated with this item.</span></span> <span data-ttu-id="752b7-143">Если выбрать строку, связанному свойству присваивается это значение.</span><span class="sxs-lookup"><span data-stu-id="752b7-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="752b7-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="752b7-145">Видимый, локализуемый текст, назначаемый элементу.</span><span class="sxs-lookup"><span data-stu-id="752b7-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="752b7-146">Если эта запись или весь столбец отсутствуют, по умолчанию используется соответствующая запись в поле значение.</span><span class="sxs-lookup"><span data-stu-id="752b7-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Двоичный\_</span><span class="sxs-lookup"><span data-stu-id="752b7-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="752b7-148">Данные изображения для значка.</span><span class="sxs-lookup"><span data-stu-id="752b7-148">The image data for the icon.</span></span> <span data-ttu-id="752b7-149">Это внешний ключ для [двоичной таблицы](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="752b7-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="752b7-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="752b7-150">Remarks</span></span>

<span data-ttu-id="752b7-151">Содержимое полей Value и Text форматируется функцией [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) при создании элемента управления, поэтому они могут содержать любое выражение, которое может интерпретировать функция мсиформатрекорд.</span><span class="sxs-lookup"><span data-stu-id="752b7-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="752b7-152">Форматирование происходит только при создании элемента управления и не обновляется, если свойство, вовлеченное в выражение, изменяется в течение жизненного цикла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="752b7-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="752b7-153">Проверка</span><span class="sxs-lookup"><span data-stu-id="752b7-153">Validation</span></span>

<dl>

[<span data-ttu-id="752b7-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="752b7-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="752b7-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="752b7-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="752b7-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="752b7-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="752b7-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="752b7-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



