---
description: Если задан бит управления Фикседволуме, элемент управления отображает все тома, вовлеченные в текущую установку, а также все фиксированные внутренние жесткие диски.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Атрибут элемента управления Фикседволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898318"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="2bade-103">Атрибут элемента управления Фикседволуме</span><span class="sxs-lookup"><span data-stu-id="2bade-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="2bade-104">Если задан бит управления Фикседволуме, элемент управления отображает все тома, вовлеченные в текущую установку, а также все фиксированные внутренние жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="2bade-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="2bade-105">Если этот бит не задан, элемент управления выводит список томов в текущей установке.</span><span class="sxs-lookup"><span data-stu-id="2bade-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="2bade-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="2bade-106">Valid Controls</span></span>

[<span data-ttu-id="2bade-107">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="2bade-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="2bade-108">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="2bade-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="2bade-109">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="2bade-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="2bade-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="2bade-110">Decimal</span></span> | <span data-ttu-id="2bade-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="2bade-111">Hexadecimal</span></span> | <span data-ttu-id="2bade-112">Константа</span><span class="sxs-lookup"><span data-stu-id="2bade-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="2bade-113">131072</span><span class="sxs-lookup"><span data-stu-id="2bade-113">131072</span></span>  | <span data-ttu-id="2bade-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2bade-114">0x00020000</span></span>  | <span data-ttu-id="2bade-115">**мсидбконтролаттрибутесфикседволуме**</span><span class="sxs-lookup"><span data-stu-id="2bade-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2bade-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bade-116">Remarks</span></span>

<span data-ttu-id="2bade-117">Чтобы задать этот атрибут для элемента управления, включите бит Фикседволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="2bade-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="2bade-118">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="2bade-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



