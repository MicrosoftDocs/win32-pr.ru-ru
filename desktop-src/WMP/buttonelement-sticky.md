---
title: БУТТОНЕЛЕМЕНТ. Клейкие
description: Атрибут «закрепление» указывает или получает значение, указывающее, является ли БУТТОНЕЛЕМЕНТ переключателем, то есть является ли он кнопкой с двумя состояниями или с одним состоянием.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- БУТТОНЕЛЕМЕНТ. закрепление проигрывателя Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695136"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="1e382-104">БУТТОНЕЛЕМЕНТ. Клейкие</span><span class="sxs-lookup"><span data-stu-id="1e382-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="1e382-105">Атрибут « **закрепление** » указывает или получает значение, указывающее, является ли **буттонелемент** переключателем, то есть является ли он кнопкой с двумя состояниями или с одним состоянием.</span><span class="sxs-lookup"><span data-stu-id="1e382-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="1e382-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1e382-106">Possible Values</span></span>

<span data-ttu-id="1e382-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1e382-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1e382-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1e382-108">Value</span></span> | <span data-ttu-id="1e382-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1e382-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="1e382-110">true</span><span class="sxs-lookup"><span data-stu-id="1e382-110">true</span></span>  | <span data-ttu-id="1e382-111">**Буттонелемент** .</span><span class="sxs-lookup"><span data-stu-id="1e382-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="1e382-112">false</span><span class="sxs-lookup"><span data-stu-id="1e382-112">false</span></span> | <span data-ttu-id="1e382-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e382-113">Default.</span></span> <span data-ttu-id="1e382-114">**Буттонелемент** не закреплен.</span><span class="sxs-lookup"><span data-stu-id="1e382-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e382-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e382-115">Remarks</span></span>

<span data-ttu-id="1e382-116">Если для атрибута **закрепления** задано значение true, элемент Button будет переходить в состояние down при щелчке и останется в этом состоянии до повторного нажатия.</span><span class="sxs-lookup"><span data-stu-id="1e382-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="1e382-117">Если элемент Button находится в состоянии Down, атрибут **Down** будет иметь значение true и будет отображена соответствующая часть группы кнопок **довнимаже** .</span><span class="sxs-lookup"><span data-stu-id="1e382-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e382-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1e382-118">Requirements</span></span>



| <span data-ttu-id="1e382-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1e382-119">Requirement</span></span> | <span data-ttu-id="1e382-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1e382-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1e382-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1e382-121">Version</span></span><br/> | <span data-ttu-id="1e382-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="1e382-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e382-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e382-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e382-124">**БУТТОНЕЛЕМЕНТ, элемент**</span><span class="sxs-lookup"><span data-stu-id="1e382-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="1e382-125">**БУТТОНЕЛЕМЕНТ.**</span><span class="sxs-lookup"><span data-stu-id="1e382-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="1e382-126">**BUTTONGROUP. Довнимаже**</span><span class="sxs-lookup"><span data-stu-id="1e382-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





