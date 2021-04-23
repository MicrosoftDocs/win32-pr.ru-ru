---
description: Это сочетание РТЛРО порядка чтения справа налево, атрибуты Ригхталигнед и Лефтскролл.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Атрибут управления BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650716"
---
# <a name="bidi-control-attribute"></a><span data-ttu-id="ffd99-103">Атрибут управления BiDi</span><span class="sxs-lookup"><span data-stu-id="ffd99-103">BiDi Control Attribute</span></span>

<span data-ttu-id="ffd99-104">Это сочетание [ртлро](rtlro-control-attribute.md)порядка чтения справа налево, атрибуты [ригхталигнед](rightaligned-control-attribute.md)и [лефтскролл](leftscroll-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd99-104">This is a combination of the right-to-left reading order [RTLRO](rtlro-control-attribute.md), the [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ffd99-105">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="ffd99-105">Valid Controls</span></span>

[<span data-ttu-id="ffd99-106">скроллаблетекст</span><span class="sxs-lookup"><span data-stu-id="ffd99-106">ScrollableText</span></span>](scrollabletext-control.md)

 

[<span data-ttu-id="ffd99-107">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="ffd99-107">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="ffd99-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="ffd99-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="ffd99-109">директорилист</span><span class="sxs-lookup"><span data-stu-id="ffd99-109">DirectoryList</span></span>](directorylist-control.md)

 

[<span data-ttu-id="ffd99-110">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="ffd99-110">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="ffd99-111">Правка</span><span class="sxs-lookup"><span data-stu-id="ffd99-111">Edit</span></span>](edit-control.md)

 

[<span data-ttu-id="ffd99-112">ListBox</span><span class="sxs-lookup"><span data-stu-id="ffd99-112">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="ffd99-113">ListView</span><span class="sxs-lookup"><span data-stu-id="ffd99-113">ListView</span></span>](listview-control.md)

 

[<span data-ttu-id="ffd99-114">селектионтри</span><span class="sxs-lookup"><span data-stu-id="ffd99-114">SelectionTree</span></span>](selectiontree-control.md)

 

[<span data-ttu-id="ffd99-115">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="ffd99-115">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="ffd99-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ffd99-116">Value</span></span>



| <span data-ttu-id="ffd99-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="ffd99-117">Decimal</span></span> | <span data-ttu-id="ffd99-118">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="ffd99-118">Hexadecimal</span></span> | <span data-ttu-id="ffd99-119">Константа</span><span class="sxs-lookup"><span data-stu-id="ffd99-119">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="ffd99-120">224</span><span class="sxs-lookup"><span data-stu-id="ffd99-120">224</span></span>     | <span data-ttu-id="ffd99-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="ffd99-121">0x000000E0</span></span>  | <span data-ttu-id="ffd99-122">**мсидбконтролаттрибутесбиди**</span><span class="sxs-lookup"><span data-stu-id="ffd99-122">**msidbControlAttributesBiDi**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ffd99-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffd99-123">Remarks</span></span>

<span data-ttu-id="ffd99-124">Чтобы задать этот атрибут для элемента управления, включите двунаправленный бит в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ffd99-124">To set this attribute on a control, include the BiDi bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ffd99-125">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ffd99-125">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



