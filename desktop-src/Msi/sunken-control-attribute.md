---
description: Если этот бит установлен, то элемент управления отображается с утопленным, трехмерным видом.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Атрибут утопленного элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155119"
---
# <a name="sunken-control-attribute"></a><span data-ttu-id="921db-103">Атрибут утопленного элемента управления</span><span class="sxs-lookup"><span data-stu-id="921db-103">Sunken Control Attribute</span></span>

<span data-ttu-id="921db-104">Если этот бит установлен, то элемент управления отображается с утопленным, трехмерным видом.</span><span class="sxs-lookup"><span data-stu-id="921db-104">If this bit is set, the control is displayed with a sunken, three dimensional look.</span></span> <span data-ttu-id="921db-105">Результат этого бита стиля отличается для разных элементов управления и версий Windows.</span><span class="sxs-lookup"><span data-stu-id="921db-105">The effect of this style bit is different on different controls and versions of Windows.</span></span> <span data-ttu-id="921db-106">На некоторых элементах управления он не имеет видимого результата.</span><span class="sxs-lookup"><span data-stu-id="921db-106">On some controls it has no visible effect.</span></span> <span data-ttu-id="921db-107">Если система не поддерживает атрибут утопленного элемента управления, элемент управления отображается в визуальном стиле по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="921db-107">If the system does not support the Sunken control attribute, the control is displayed in the default visual style.</span></span> <span data-ttu-id="921db-108">Если этот бит не задан, элемент управления отображается с визуальным стилем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="921db-108">If this bit is not set, the control is displayed with the default visual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="921db-109">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="921db-109">Valid Controls</span></span>

<span data-ttu-id="921db-110">Все элементы управления.</span><span class="sxs-lookup"><span data-stu-id="921db-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="921db-111">Значение</span><span class="sxs-lookup"><span data-stu-id="921db-111">Value</span></span>



| <span data-ttu-id="921db-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="921db-112">Decimal</span></span> | <span data-ttu-id="921db-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="921db-113">Hexadecimal</span></span> | <span data-ttu-id="921db-114">Константа</span><span class="sxs-lookup"><span data-stu-id="921db-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="921db-115">4</span><span class="sxs-lookup"><span data-stu-id="921db-115">4</span></span>       | <span data-ttu-id="921db-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="921db-116">0x00000004</span></span>  | <span data-ttu-id="921db-117">**мсидбконтролаттрибутессункен**</span><span class="sxs-lookup"><span data-stu-id="921db-117">**msidbControlAttributesSunken**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="921db-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="921db-118">Remarks</span></span>

<span data-ttu-id="921db-119">Чтобы задать этот атрибут для элемента управления, включите Утопленный бит в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="921db-119">To set this attribute on a control, include the Sunken bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="921db-120">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="921db-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



