---
title: КНОПКА. прикрепленная
description: Атрибут «закрепление» указывает или получает значение, указывающее, является ли кнопка переключателем, то есть является ли она кнопкой с двумя состояниями или с одним состоянием.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- КНОПКА. проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694632"
---
# <a name="buttonsticky"></a><span data-ttu-id="586c3-104">КНОПКА. прикрепленная</span><span class="sxs-lookup"><span data-stu-id="586c3-104">BUTTON.sticky</span></span>

<span data-ttu-id="586c3-105">Атрибут « **закрепление** » указывает или получает значение, указывающее, является ли **кнопка** переключателем, то есть является ли она **кнопкой** с двумя состояниями или с одним состоянием.</span><span class="sxs-lookup"><span data-stu-id="586c3-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="586c3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="586c3-106">Possible Values</span></span>

<span data-ttu-id="586c3-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="586c3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="586c3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="586c3-108">Value</span></span> | <span data-ttu-id="586c3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="586c3-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="586c3-110">true</span><span class="sxs-lookup"><span data-stu-id="586c3-110">true</span></span>  | <span data-ttu-id="586c3-111">**Кнопка** закреплена.</span><span class="sxs-lookup"><span data-stu-id="586c3-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="586c3-112">false</span><span class="sxs-lookup"><span data-stu-id="586c3-112">false</span></span> | <span data-ttu-id="586c3-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="586c3-113">Default.</span></span> <span data-ttu-id="586c3-114">**Кнопка** не закреплена.</span><span class="sxs-lookup"><span data-stu-id="586c3-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="586c3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="586c3-115">Remarks</span></span>

<span data-ttu-id="586c3-116">Если параметру **закрепления** присвоено значение true, **кнопка** будет переходить в состояние down при щелчке и останется в этом состоянии до повторного нажатия.</span><span class="sxs-lookup"><span data-stu-id="586c3-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="586c3-117">Если **кнопка** находится в состоянии Down, атрибут **Down** будет иметь значение true, а будет отображено **довнимаже** .</span><span class="sxs-lookup"><span data-stu-id="586c3-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="586c3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="586c3-118">Requirements</span></span>



| <span data-ttu-id="586c3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="586c3-119">Requirement</span></span> | <span data-ttu-id="586c3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="586c3-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="586c3-121">Версия</span><span class="sxs-lookup"><span data-stu-id="586c3-121">Version</span></span><br/> | <span data-ttu-id="586c3-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="586c3-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="586c3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="586c3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586c3-124">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="586c3-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="586c3-125">**КНОПКА. вниз**</span><span class="sxs-lookup"><span data-stu-id="586c3-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="586c3-126">**КНОПКА. Довнимаже**</span><span class="sxs-lookup"><span data-stu-id="586c3-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





