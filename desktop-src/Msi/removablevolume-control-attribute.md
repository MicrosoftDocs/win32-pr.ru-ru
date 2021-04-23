---
description: Если этот бит задан, элемент управления отображает все тома, вовлеченные в текущую установку, а также все съемные тома. Если этот бит не задан, элемент управления перечисляет тома в текущей установке.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Атрибут элемента управления Ремоваблеволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809496"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="ec980-104">Атрибут элемента управления Ремоваблеволуме</span><span class="sxs-lookup"><span data-stu-id="ec980-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="ec980-105">Если этот бит задан, элемент управления отображает все тома, вовлеченные в текущую установку, а также все съемные тома.</span><span class="sxs-lookup"><span data-stu-id="ec980-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="ec980-106">Если этот бит не задан, элемент управления перечисляет тома в текущей установке.</span><span class="sxs-lookup"><span data-stu-id="ec980-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ec980-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="ec980-107">Valid Controls</span></span>

[<span data-ttu-id="ec980-108">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="ec980-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="ec980-109">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="ec980-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="ec980-110">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="ec980-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="ec980-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ec980-111">Value</span></span>



| <span data-ttu-id="ec980-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="ec980-112">Decimal</span></span> | <span data-ttu-id="ec980-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="ec980-113">Hexadecimal</span></span> | <span data-ttu-id="ec980-114">Константа</span><span class="sxs-lookup"><span data-stu-id="ec980-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="ec980-115">65536</span><span class="sxs-lookup"><span data-stu-id="ec980-115">65536</span></span>   | <span data-ttu-id="ec980-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ec980-116">0x00010000</span></span>  | <span data-ttu-id="ec980-117">**мсидбконтролаттрибутесремоваблеволуме**</span><span class="sxs-lookup"><span data-stu-id="ec980-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ec980-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec980-118">Remarks</span></span>

<span data-ttu-id="ec980-119">Чтобы задать этот атрибут для элемента управления, включите бит Ремоваблеволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec980-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ec980-120">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ec980-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



