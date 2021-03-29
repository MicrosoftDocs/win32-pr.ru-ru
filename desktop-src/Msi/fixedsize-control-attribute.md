---
description: Если установлен бит управления FixedSize, изображение обрезается или выравнивается по центру элемента управления без изменения его формы или размера.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Атрибут элемента управления FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809508"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="a88d6-103">Атрибут элемента управления FixedSize</span><span class="sxs-lookup"><span data-stu-id="a88d6-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="a88d6-104">Если установлен бит управления FixedSize, изображение обрезается или выравнивается по центру элемента управления без изменения его формы или размера.</span><span class="sxs-lookup"><span data-stu-id="a88d6-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="a88d6-105">Если этот бит не установлен, изображение растягивается для соответствия элементу управления.</span><span class="sxs-lookup"><span data-stu-id="a88d6-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a88d6-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="a88d6-106">Valid Controls</span></span>

[<span data-ttu-id="a88d6-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="a88d6-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="a88d6-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="a88d6-108">CheckBox</span></span>](checkbox-control.md)

<span data-ttu-id="a88d6-109">[Значок](icon-control.md):</span><span class="sxs-lookup"><span data-stu-id="a88d6-109">[Icon](icon-control.md)</span></span>

[<span data-ttu-id="a88d6-110">PushButton</span><span class="sxs-lookup"><span data-stu-id="a88d6-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="a88d6-111">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="a88d6-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="a88d6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a88d6-112">Value</span></span>



| <span data-ttu-id="a88d6-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="a88d6-113">Decimal</span></span> | <span data-ttu-id="a88d6-114">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="a88d6-114">Hexadecimal</span></span> | <span data-ttu-id="a88d6-115">Константа</span><span class="sxs-lookup"><span data-stu-id="a88d6-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="a88d6-116">1048576</span><span class="sxs-lookup"><span data-stu-id="a88d6-116">1048576</span></span> | <span data-ttu-id="a88d6-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="a88d6-117">0x00100000</span></span>  | <span data-ttu-id="a88d6-118">**мсидбконтролаттрибутесфикседсизе**</span><span class="sxs-lookup"><span data-stu-id="a88d6-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a88d6-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a88d6-119">Remarks</span></span>

<span data-ttu-id="a88d6-120">Чтобы задать этот атрибут для элемента управления, включите бит FixedSize в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="a88d6-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="a88d6-121">Установка бита FixedSize не влияет на [CheckBox](checkbox-control.md), [кнопка](pushbutton-control.md)или [радиобуттонграуп](radiobuttongroup-control.md) , если не задано ни [точечный рисунок](bitmap-control-attribute.md) , ни [значок](icon-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a88d6-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="a88d6-122">Установка бита FixedSize не влияет на элемент управления "значок" или на значок, связанный со значком, если биты [иконсизе](iconsize-control-attribute.md) не заданы.</span><span class="sxs-lookup"><span data-stu-id="a88d6-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="a88d6-123">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="a88d6-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



