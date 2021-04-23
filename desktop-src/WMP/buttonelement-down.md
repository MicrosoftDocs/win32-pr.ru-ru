---
title: БУТТОНЕЛЕМЕНТ.
description: Атрибут Down указывает или получает значение, указывающее, находится ли элемент кнопки в положении "вверх" или "вниз".
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- БУТТОНЕЛЕМЕНТ. проигрыватель Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695126"
---
# <a name="buttonelementdown"></a><span data-ttu-id="eccb4-104">БУТТОНЕЛЕМЕНТ.</span><span class="sxs-lookup"><span data-stu-id="eccb4-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="eccb4-105">Атрибут **Down** указывает или получает значение, указывающее, находится ли элемент кнопки в положении "вверх" или "вниз".</span><span class="sxs-lookup"><span data-stu-id="eccb4-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="eccb4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="eccb4-106">Possible Values</span></span>

<span data-ttu-id="eccb4-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="eccb4-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="eccb4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eccb4-108">Value</span></span> | <span data-ttu-id="eccb4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eccb4-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="eccb4-110">true</span><span class="sxs-lookup"><span data-stu-id="eccb4-110">true</span></span>  | <span data-ttu-id="eccb4-111">Указывает, что **буттонелемент** находится в расположении вниз.</span><span class="sxs-lookup"><span data-stu-id="eccb4-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="eccb4-112">false</span><span class="sxs-lookup"><span data-stu-id="eccb4-112">false</span></span> | <span data-ttu-id="eccb4-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eccb4-113">Default.</span></span> <span data-ttu-id="eccb4-114">Указывает, что **буттонелемент** находится в положении Up.</span><span class="sxs-lookup"><span data-stu-id="eccb4-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eccb4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eccb4-115">Remarks</span></span>

<span data-ttu-id="eccb4-116">Чтобы элемент Button оставался в положении вниз, необходимо установить для параметра **закрепить** значение true.</span><span class="sxs-lookup"><span data-stu-id="eccb4-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="eccb4-117">По умолчанию **закрепление** имеет значение false, и любая попытка **установить значение** true будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="eccb4-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="eccb4-118">Если указано недопустимое значение, сохраняется предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="eccb4-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccb4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eccb4-119">Requirements</span></span>



| <span data-ttu-id="eccb4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eccb4-120">Requirement</span></span> | <span data-ttu-id="eccb4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eccb4-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="eccb4-122">Версия</span><span class="sxs-lookup"><span data-stu-id="eccb4-122">Version</span></span><br/> | <span data-ttu-id="eccb4-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="eccb4-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eccb4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eccb4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccb4-125">**БУТТОНЕЛЕМЕНТ, элемент**</span><span class="sxs-lookup"><span data-stu-id="eccb4-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="eccb4-126">**БУТТОНЕЛЕМЕНТ. Довнтултип**</span><span class="sxs-lookup"><span data-stu-id="eccb4-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





