---
description: Если этот бит задан, текст заменяется изображением значка, а текстовый столбец в таблице управления является внешним ключом в двоичную таблицу.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Атрибут элемента управления Icon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650622"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="bae33-103">Атрибут элемента управления Icon</span><span class="sxs-lookup"><span data-stu-id="bae33-103">Icon Control Attribute</span></span>

<span data-ttu-id="bae33-104">Если этот бит задан, текст заменяется изображением значка, а текстовый столбец в [таблице управления](control-table.md) является внешним ключом в [двоичную таблицу](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="bae33-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="bae33-105">Если этот бит не задан, текст в элементе управления указывается в столбце text [таблицы Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="bae33-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="bae33-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="bae33-106">Valid Controls</span></span>

[<span data-ttu-id="bae33-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="bae33-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="bae33-108">PushButton</span><span class="sxs-lookup"><span data-stu-id="bae33-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="bae33-109">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="bae33-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="bae33-110">Значение</span><span class="sxs-lookup"><span data-stu-id="bae33-110">Value</span></span>



| <span data-ttu-id="bae33-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="bae33-111">Decimal</span></span> | <span data-ttu-id="bae33-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="bae33-112">Hexadecimal</span></span> | <span data-ttu-id="bae33-113">Константа</span><span class="sxs-lookup"><span data-stu-id="bae33-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="bae33-114">5242288</span><span class="sxs-lookup"><span data-stu-id="bae33-114">5242288</span></span> | <span data-ttu-id="bae33-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="bae33-115">0x00080000</span></span>  | <span data-ttu-id="bae33-116">**мсидбконтролаттрибутесикон**</span><span class="sxs-lookup"><span data-stu-id="bae33-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bae33-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bae33-117">Remarks</span></span>

<span data-ttu-id="bae33-118">Чтобы задать этот атрибут для элемента управления, включите биты значков в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="bae33-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="bae33-119">Текстовый столбец в таблице управления используется в качестве внешнего ключа для [двоичной таблицы](binary-table.md), поэтому элемент управления не может содержать как изображение значка, так и текст.</span><span class="sxs-lookup"><span data-stu-id="bae33-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="bae33-120">Не задавайте биты значка и [точечного рисунка](bitmap-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="bae33-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="bae33-121">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="bae33-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



