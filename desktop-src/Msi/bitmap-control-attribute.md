---
description: Если задан битовый контрольный бит, текст в элементе управления заменяется растровым изображением. Текстовый столбец в таблице управления является внешним ключом в двоичной таблице.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Атрибут элемента управления Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909055"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="b155e-104">Атрибут элемента управления Bitmap</span><span class="sxs-lookup"><span data-stu-id="b155e-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="b155e-105">Если задан битовый контрольный бит, текст в элементе управления заменяется растровым изображением.</span><span class="sxs-lookup"><span data-stu-id="b155e-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="b155e-106">Текстовый столбец в [таблице управления](control-table.md) является внешним ключом в [двоичной таблице](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="b155e-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="b155e-107">Если этот бит не задан, текст в элементе управления указывается в столбце text [таблицы Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="b155e-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b155e-108">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="b155e-108">Valid Controls</span></span>

[<span data-ttu-id="b155e-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="b155e-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="b155e-110">PushButton</span><span class="sxs-lookup"><span data-stu-id="b155e-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="b155e-111">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="b155e-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="b155e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b155e-112">Value</span></span>



| <span data-ttu-id="b155e-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="b155e-113">Decimal</span></span> | <span data-ttu-id="b155e-114">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="b155e-114">Hexadecimal</span></span> | <span data-ttu-id="b155e-115">Константа</span><span class="sxs-lookup"><span data-stu-id="b155e-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="b155e-116">262144</span><span class="sxs-lookup"><span data-stu-id="b155e-116">262144</span></span>  | <span data-ttu-id="b155e-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="b155e-117">0x00040000</span></span>  | <span data-ttu-id="b155e-118">**мсидбконтролаттрибутесбитмап**</span><span class="sxs-lookup"><span data-stu-id="b155e-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b155e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b155e-119">Remarks</span></span>

<span data-ttu-id="b155e-120">Чтобы задать этот атрибут для элемента управления, включите бит точечного рисунка в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="b155e-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="b155e-121">Текстовый столбец в таблице управления используется в качестве внешнего ключа для [двоичной таблицы](binary-table.md), поэтому элемент управления не может содержать как изображение значка, так и текст.</span><span class="sxs-lookup"><span data-stu-id="b155e-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="b155e-122">Не задавайте биты [значка](icon-control-attribute.md) и точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b155e-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="b155e-123">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="b155e-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



