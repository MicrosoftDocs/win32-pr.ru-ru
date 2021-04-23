---
description: Если этот бит задан для текстового элемента управления, то вхождение символа &\# 0034; &&\# 0034; в текстовой строке отображается как сам. Если этот бит не задан, то символ, следующий за &\# 0034; &&\# 0034; в текстовой строке отображается как символ подчеркивания.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Атрибут элемента управления "префикс"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263597"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="de57f-104">Атрибут элемента управления "префикс"</span><span class="sxs-lookup"><span data-stu-id="de57f-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="de57f-105">Если этот бит задан для текстового элемента управления, то вхождение символа "&" в текстовой строке отображается как сам.</span><span class="sxs-lookup"><span data-stu-id="de57f-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="de57f-106">Если этот бит не задан, то символ, следующий за "&" в текстовой строке, отображается как символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="de57f-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="de57f-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="de57f-107">Valid Controls</span></span>

[<span data-ttu-id="de57f-108">Text</span><span class="sxs-lookup"><span data-stu-id="de57f-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="de57f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="de57f-109">Value</span></span>



| <span data-ttu-id="de57f-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="de57f-110">Decimal</span></span> | <span data-ttu-id="de57f-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="de57f-111">Hexadecimal</span></span> | <span data-ttu-id="de57f-112">Константа</span><span class="sxs-lookup"><span data-stu-id="de57f-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="de57f-113">131072</span><span class="sxs-lookup"><span data-stu-id="de57f-113">131072</span></span>  | <span data-ttu-id="de57f-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="de57f-114">0x20000</span></span>     | <span data-ttu-id="de57f-115">**мсидбконтролаттрибутеснопрефикс**</span><span class="sxs-lookup"><span data-stu-id="de57f-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="de57f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de57f-116">Remarks</span></span>

<span data-ttu-id="de57f-117">Чтобы задать этот атрибут для элемента управления, включите бит префикса в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="de57f-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="de57f-118">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="de57f-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



