---
description: Если этот бит задан, в элементе управления отображаются все тома, вовлеченные в текущую установку, а также все удаленные тома. Если этот бит не задан, элемент управления перечисляет тома в текущей установке.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Атрибут элемента управления Ремотеволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673261"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="99a44-104">Атрибут элемента управления Ремотеволуме</span><span class="sxs-lookup"><span data-stu-id="99a44-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="99a44-105">Если этот бит задан, в элементе управления отображаются все тома, вовлеченные в текущую установку, а также все удаленные тома.</span><span class="sxs-lookup"><span data-stu-id="99a44-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="99a44-106">Если этот бит не задан, элемент управления перечисляет тома в текущей установке.</span><span class="sxs-lookup"><span data-stu-id="99a44-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="99a44-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="99a44-107">Valid Controls</span></span>

[<span data-ttu-id="99a44-108">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="99a44-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="99a44-109">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="99a44-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="99a44-110">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="99a44-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="99a44-111">Значение</span><span class="sxs-lookup"><span data-stu-id="99a44-111">Value</span></span>



| <span data-ttu-id="99a44-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="99a44-112">Decimal</span></span> | <span data-ttu-id="99a44-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="99a44-113">Hexadecimal</span></span> | <span data-ttu-id="99a44-114">Константа</span><span class="sxs-lookup"><span data-stu-id="99a44-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="99a44-115">262144</span><span class="sxs-lookup"><span data-stu-id="99a44-115">262144</span></span>  | <span data-ttu-id="99a44-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="99a44-116">0x00040000</span></span>  | <span data-ttu-id="99a44-117">**мсидбконтролаттрибутесремотеволуме**</span><span class="sxs-lookup"><span data-stu-id="99a44-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="99a44-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99a44-118">Remarks</span></span>

<span data-ttu-id="99a44-119">Чтобы задать этот атрибут для элемента управления, включите бит Ремотеволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="99a44-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="99a44-120">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="99a44-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



