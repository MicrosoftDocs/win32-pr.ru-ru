---
description: Если этот бит задан, в элементе управления отображаются все тома, участвующие в текущей установке, а также все тома RAM-дисков. Если этот бит не задан, в списке элементов управления отображаются тома текущей установки.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Атрибут элемента управления Рамдискволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673673"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="212d6-104">Атрибут элемента управления Рамдискволуме</span><span class="sxs-lookup"><span data-stu-id="212d6-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="212d6-105">Если этот бит задан, в элементе управления отображаются все тома, участвующие в текущей установке, а также все тома RAM-дисков.</span><span class="sxs-lookup"><span data-stu-id="212d6-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="212d6-106">Если этот бит не задан, в списке элементов управления отображаются тома текущей установки.</span><span class="sxs-lookup"><span data-stu-id="212d6-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="212d6-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="212d6-107">Valid Controls</span></span>

[<span data-ttu-id="212d6-108">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="212d6-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="212d6-109">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="212d6-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="212d6-110">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="212d6-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="212d6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="212d6-111">Value</span></span>



| <span data-ttu-id="212d6-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="212d6-112">Decimal</span></span> | <span data-ttu-id="212d6-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="212d6-113">Hexadecimal</span></span> | <span data-ttu-id="212d6-114">Константа</span><span class="sxs-lookup"><span data-stu-id="212d6-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="212d6-115">1048567</span><span class="sxs-lookup"><span data-stu-id="212d6-115">1048567</span></span> | <span data-ttu-id="212d6-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="212d6-116">0x00100000</span></span>  | <span data-ttu-id="212d6-117">**мсидбконтролаттрибутесрамдискволуме**</span><span class="sxs-lookup"><span data-stu-id="212d6-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="212d6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="212d6-118">Remarks</span></span>

<span data-ttu-id="212d6-119">Чтобы задать этот атрибут для элемента управления, включите бит Рамдискволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="212d6-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="212d6-120">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="212d6-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



