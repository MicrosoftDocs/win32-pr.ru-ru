---
description: Если этот бит установлен, текст в элементе управления отображается в одной строке. Если текст выходит за пределы полей элемента управления, он усекается и многоточие (&\# 0034;... &\# 0034;) вставляется в конец для указания усечения. Если этот бит не задан, текст переносится.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Атрибут управления "без переноса"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673903"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="ccea8-105">Атрибут управления "без переноса"</span><span class="sxs-lookup"><span data-stu-id="ccea8-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="ccea8-106">Если этот бит установлен, текст в элементе управления отображается в одной строке.</span><span class="sxs-lookup"><span data-stu-id="ccea8-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="ccea8-107">Если текст выходит за пределы полей элемента управления, он усекается, а в конце вставляется многоточие (...), чтобы указать усечение.</span><span class="sxs-lookup"><span data-stu-id="ccea8-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="ccea8-108">Если этот бит не задан, текст переносится.</span><span class="sxs-lookup"><span data-stu-id="ccea8-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ccea8-109">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="ccea8-109">Valid Controls</span></span>

[<span data-ttu-id="ccea8-110">Text</span><span class="sxs-lookup"><span data-stu-id="ccea8-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="ccea8-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ccea8-111">Value</span></span>



| <span data-ttu-id="ccea8-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="ccea8-112">Decimal</span></span> | <span data-ttu-id="ccea8-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="ccea8-113">Hexadecimal</span></span> | <span data-ttu-id="ccea8-114">Константа</span><span class="sxs-lookup"><span data-stu-id="ccea8-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="ccea8-115">262144</span><span class="sxs-lookup"><span data-stu-id="ccea8-115">262144</span></span>  | <span data-ttu-id="ccea8-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="ccea8-116">0x00040000</span></span>  | <span data-ttu-id="ccea8-117">**мсидбконтролаттрибутесноврап**</span><span class="sxs-lookup"><span data-stu-id="ccea8-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ccea8-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccea8-118">Remarks</span></span>

<span data-ttu-id="ccea8-119">Чтобы задать этот атрибут для элемента управления, включите бит перетекания в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ccea8-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ccea8-120">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ccea8-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



