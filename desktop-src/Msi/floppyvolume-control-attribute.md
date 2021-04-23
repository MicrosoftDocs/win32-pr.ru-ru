---
description: Если задан бит управления Флоппиволуме, в элементе управления отображаются все тома, вовлеченные в текущую установку, а также все гибкие тома.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Атрибут элемента управления Флоппиволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544271"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="6aee8-103">Атрибут элемента управления Флоппиволуме</span><span class="sxs-lookup"><span data-stu-id="6aee8-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="6aee8-104">Если задан бит управления Флоппиволуме, в элементе управления отображаются все тома, вовлеченные в текущую установку, а также все гибкие тома.</span><span class="sxs-lookup"><span data-stu-id="6aee8-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="6aee8-105">Если этот бит не задан, элемент управления перечисляет тома в текущей установке.</span><span class="sxs-lookup"><span data-stu-id="6aee8-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6aee8-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="6aee8-106">Valid Controls</span></span>

[<span data-ttu-id="6aee8-107">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="6aee8-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="6aee8-108">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="6aee8-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="6aee8-109">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="6aee8-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="6aee8-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6aee8-110">Value</span></span>



| <span data-ttu-id="6aee8-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="6aee8-111">Decimal</span></span> | <span data-ttu-id="6aee8-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="6aee8-112">Hexadecimal</span></span> | <span data-ttu-id="6aee8-113">Константа</span><span class="sxs-lookup"><span data-stu-id="6aee8-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="6aee8-114">2097152</span><span class="sxs-lookup"><span data-stu-id="6aee8-114">2097152</span></span> | <span data-ttu-id="6aee8-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="6aee8-115">0x00200000</span></span>  | <span data-ttu-id="6aee8-116">**мсидбконтролаттрибутесфлоппиволуме**</span><span class="sxs-lookup"><span data-stu-id="6aee8-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6aee8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6aee8-117">Remarks</span></span>

<span data-ttu-id="6aee8-118">Чтобы задать этот атрибут для элемента управления, включите бит Флоппиволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6aee8-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6aee8-119">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6aee8-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



