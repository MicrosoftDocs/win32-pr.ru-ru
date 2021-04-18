---
title: КНОПКА. вниз
description: Атрибут Down указывает или получает значение, указывающее, находится ли кнопка в положении "вверх" или "вниз".
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- КНОПКА. проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695102"
---
# <a name="buttondown"></a><span data-ttu-id="f5907-104">КНОПКА. вниз</span><span class="sxs-lookup"><span data-stu-id="f5907-104">BUTTON.down</span></span>

<span data-ttu-id="f5907-105">Атрибут **Down** указывает или получает значение, указывающее, находится ли **кнопка** в положении "вверх" или "вниз".</span><span class="sxs-lookup"><span data-stu-id="f5907-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="f5907-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f5907-106">Possible Values</span></span>

<span data-ttu-id="f5907-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f5907-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="f5907-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f5907-108">Value</span></span> | <span data-ttu-id="f5907-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f5907-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="f5907-110">true</span><span class="sxs-lookup"><span data-stu-id="f5907-110">true</span></span>  | <span data-ttu-id="f5907-111">Указывает, что **кнопка** находится в расположении вниз.</span><span class="sxs-lookup"><span data-stu-id="f5907-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="f5907-112">false</span><span class="sxs-lookup"><span data-stu-id="f5907-112">false</span></span> | <span data-ttu-id="f5907-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5907-113">Default.</span></span> <span data-ttu-id="f5907-114">Указывает, что **кнопка** находится в положении вверх.</span><span class="sxs-lookup"><span data-stu-id="f5907-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5907-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5907-115">Remarks</span></span>

<span data-ttu-id="f5907-116">Чтобы **кнопка** оставалась в положении вниз, необходимо задать для параметра **закрепить** значение true.</span><span class="sxs-lookup"><span data-stu-id="f5907-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="f5907-117">По умолчанию **закрепление** имеет значение false, и любая попытка **установить значение** true будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="f5907-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="f5907-118">Если указано недопустимое значение, сохраняется предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="f5907-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5907-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f5907-119">Requirements</span></span>



| <span data-ttu-id="f5907-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f5907-120">Requirement</span></span> | <span data-ttu-id="f5907-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f5907-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f5907-122">Версия</span><span class="sxs-lookup"><span data-stu-id="f5907-122">Version</span></span><br/> | <span data-ttu-id="f5907-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="f5907-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5907-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5907-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5907-125">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="f5907-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="f5907-126">**КНОПКА. Довнимаже**</span><span class="sxs-lookup"><span data-stu-id="f5907-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="f5907-127">**КНОПКА. Довнтултип**</span><span class="sxs-lookup"><span data-stu-id="f5907-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





