---
description: Если установлен бит управления Кдромволуме, элемент управления отображает все тома в текущей установке, а также все тома компакт-дисков.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Атрибут элемента управления Кдромволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650708"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="9c37c-103">Атрибут элемента управления Кдромволуме</span><span class="sxs-lookup"><span data-stu-id="9c37c-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="9c37c-104">Если установлен бит управления Кдромволуме, элемент управления отображает все тома в текущей установке, а также все тома компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="9c37c-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="9c37c-105">Если этот бит не задан, элемент управления отображает все тома в текущей установке.</span><span class="sxs-lookup"><span data-stu-id="9c37c-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="9c37c-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="9c37c-106">Valid Controls</span></span>

[<span data-ttu-id="9c37c-107">директорикомбо</span><span class="sxs-lookup"><span data-stu-id="9c37c-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="9c37c-108">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="9c37c-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="9c37c-109">волумеселекткомбо</span><span class="sxs-lookup"><span data-stu-id="9c37c-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="9c37c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9c37c-110">Value</span></span>



| <span data-ttu-id="9c37c-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="9c37c-111">Decimal</span></span> | <span data-ttu-id="9c37c-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="9c37c-112">Hexadecimal</span></span> | <span data-ttu-id="9c37c-113">Константа</span><span class="sxs-lookup"><span data-stu-id="9c37c-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="9c37c-114">524288</span><span class="sxs-lookup"><span data-stu-id="9c37c-114">524288</span></span>  | <span data-ttu-id="9c37c-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9c37c-115">0x00080000</span></span>  | <span data-ttu-id="9c37c-116">**мсидбконтролаттрибутескдромволуме**</span><span class="sxs-lookup"><span data-stu-id="9c37c-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c37c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c37c-117">Remarks</span></span>

<span data-ttu-id="9c37c-118">Чтобы задать этот атрибут для элемента управления, включите бит Кдромволуме в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c37c-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="9c37c-119">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="9c37c-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



