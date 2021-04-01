---
description: Если этот бит задан, элементы, перечисленные в элементе управления, отображаются в указанном порядке. Если бит не задан, элементы отображаются в алфавитном порядке.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Отсортированный атрибут элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072628"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="54692-104">Отсортированный атрибут элемента управления</span><span class="sxs-lookup"><span data-stu-id="54692-104">Sorted Control Attribute</span></span>

<span data-ttu-id="54692-105">Если этот бит задан, элементы, перечисленные в элементе управления, отображаются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="54692-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="54692-106">Если бит не задан, элементы отображаются в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="54692-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="54692-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="54692-107">Valid Controls</span></span>

[<span data-ttu-id="54692-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="54692-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="54692-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="54692-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="54692-110">Элемент управления ListView</span><span class="sxs-lookup"><span data-stu-id="54692-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="54692-111">Значение</span><span class="sxs-lookup"><span data-stu-id="54692-111">Value</span></span>



| <span data-ttu-id="54692-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="54692-112">Decimal</span></span> | <span data-ttu-id="54692-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="54692-113">Hexadecimal</span></span> | <span data-ttu-id="54692-114">Константа</span><span class="sxs-lookup"><span data-stu-id="54692-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="54692-115">65536</span><span class="sxs-lookup"><span data-stu-id="54692-115">65536</span></span>   | <span data-ttu-id="54692-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="54692-116">0x00010000</span></span>  | <span data-ttu-id="54692-117">**мсидбконтролаттрибутессортед**</span><span class="sxs-lookup"><span data-stu-id="54692-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54692-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54692-118">Remarks</span></span>

<span data-ttu-id="54692-119">Чтобы отсортировать элементы в [ComboBox](combobox-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в столбце Порядок [таблицы ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="54692-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="54692-120">Чтобы отсортировать элементы в [ListBox](listbox-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в столбце Порядок [таблицы ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="54692-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="54692-121">Чтобы отсортировать элементы в [ListView](listview-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в [таблице ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="54692-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="54692-122">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="54692-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



