---
description: Если этот бит задан для элемента управления ProgressBar, он рисуется как ряд мелких прямоугольников. Если этот бит не задан, индикатор хода выполнения рисуется как один непрерывный прямоугольник.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Атрибут элемента управления Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911656"
---
# <a name="progress95-control-attribute"></a><span data-ttu-id="420f2-104">Атрибут элемента управления Progress95</span><span class="sxs-lookup"><span data-stu-id="420f2-104">Progress95 Control Attribute</span></span>

<span data-ttu-id="420f2-105">Если этот бит задан для [элемента управления ProgressBar](progressbar-control.md), он рисуется как ряд мелких прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="420f2-105">If this bit is set on a [ProgressBar control](progressbar-control.md), the bar is drawn as a series of small rectangles.</span></span> <span data-ttu-id="420f2-106">Если этот бит не задан, индикатор хода выполнения рисуется как один непрерывный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="420f2-106">If this bit is not set, the progress indicator bar is drawn as a single continuous rectangle.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="420f2-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="420f2-107">Valid Controls</span></span>

[<span data-ttu-id="420f2-108">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="420f2-108">ProgressBar</span></span>](progressbar-control.md)

## <a name="value"></a><span data-ttu-id="420f2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="420f2-109">Value</span></span>



| <span data-ttu-id="420f2-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="420f2-110">Decimal</span></span> | <span data-ttu-id="420f2-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="420f2-111">Hexadecimal</span></span> | <span data-ttu-id="420f2-112">Константа</span><span class="sxs-lookup"><span data-stu-id="420f2-112">Constant</span></span>                             |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="420f2-113">65536</span><span class="sxs-lookup"><span data-stu-id="420f2-113">65536</span></span>   | <span data-ttu-id="420f2-114">0x00010000</span><span class="sxs-lookup"><span data-stu-id="420f2-114">0x00010000</span></span>  | <span data-ttu-id="420f2-115">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="420f2-115">**msidbControlAttributesProgress95**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="420f2-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="420f2-116">Remarks</span></span>

<span data-ttu-id="420f2-117">Чтобы задать этот атрибут для элемента управления, включите бит Progress95 в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="420f2-117">To set this attribute on a control, include the Progress95 bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="420f2-118">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="420f2-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



