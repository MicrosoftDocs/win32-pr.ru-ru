---
description: Этот атрибут указывает, включаются ли файлы резервных копий отката в затраты, отображаемые элементом управления Волумекостлист.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Атрибут элемента управления Контролшовроллбакккост
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911915"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="ab74a-103">Атрибут элемента управления Контролшовроллбакккост</span><span class="sxs-lookup"><span data-stu-id="ab74a-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="ab74a-104">Этот атрибут указывает, включаются ли файлы резервных копий отката в затраты, отображаемые [элементом управления волумекостлист](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="ab74a-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="ab74a-105">Если этот бит задан и [**промптроллбакккост**](promptrollbackcost.md) свойство = P, файлы резервной копии для отката включаются в стоимость, отображаемую [элементом управления волумекостлист](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="ab74a-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="ab74a-106">Если этот бит не задан и [**промптроллбакккост**](promptrollbackcost.md) свойство = P, файлы резервной копии для отката не включаются в стоимость, отображаемую [элементом управления волумекостлист](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="ab74a-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ab74a-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="ab74a-107">Valid Controls</span></span>

[<span data-ttu-id="ab74a-108">волумекостлист</span><span class="sxs-lookup"><span data-stu-id="ab74a-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="ab74a-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ab74a-109">Value</span></span>



| <span data-ttu-id="ab74a-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="ab74a-110">Decimal</span></span> | <span data-ttu-id="ab74a-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="ab74a-111">Hexadecimal</span></span> | <span data-ttu-id="ab74a-112">Константа</span><span class="sxs-lookup"><span data-stu-id="ab74a-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="ab74a-113">4194304</span><span class="sxs-lookup"><span data-stu-id="ab74a-113">4194304</span></span> | <span data-ttu-id="ab74a-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="ab74a-114">0x00400000</span></span>  | <span data-ttu-id="ab74a-115">**мсидбконтролшовроллбакккост**</span><span class="sxs-lookup"><span data-stu-id="ab74a-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab74a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab74a-116">Remarks</span></span>

<span data-ttu-id="ab74a-117">Этот атрибут Control игнорируется, если [**промптроллбакккост**](promptrollbackcost.md) = D или F.</span><span class="sxs-lookup"><span data-stu-id="ab74a-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="ab74a-118">Если [**промптроллбакккост**](promptrollbackcost.md) = F, то издержки на откат, файлы резервной копии включаются.</span><span class="sxs-lookup"><span data-stu-id="ab74a-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="ab74a-119">Если [**промптроллбакккост**](promptrollbackcost.md) = D или [**дисаблероллбакк**](-disablerollback.md) Property = 1, то затраты на откат, файлы резервной копии не включаются.</span><span class="sxs-lookup"><span data-stu-id="ab74a-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



