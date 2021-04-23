---
title: BUTTONGROUP. Radio
description: Атрибут Radio указывает или получает значение, указывающее, состоит ли BUTTONGROUP из переключателей.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Radio
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698808"
---
# <a name="buttongroupradio"></a><span data-ttu-id="ebc87-104">BUTTONGROUP. Radio</span><span class="sxs-lookup"><span data-stu-id="ebc87-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="ebc87-105">Атрибут **Radio** указывает или получает значение, указывающее, состоит ли **BUTTONGROUP** из переключателей.</span><span class="sxs-lookup"><span data-stu-id="ebc87-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="ebc87-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ebc87-106">Possible Values</span></span>

<span data-ttu-id="ebc87-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ebc87-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ebc87-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ebc87-108">Value</span></span> | <span data-ttu-id="ebc87-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ebc87-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="ebc87-110">true</span><span class="sxs-lookup"><span data-stu-id="ebc87-110">true</span></span>  | <span data-ttu-id="ebc87-111">**BUTTONGROUP** имеет вид радио.</span><span class="sxs-lookup"><span data-stu-id="ebc87-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="ebc87-112">false</span><span class="sxs-lookup"><span data-stu-id="ebc87-112">false</span></span> | <span data-ttu-id="ebc87-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebc87-113">Default.</span></span> <span data-ttu-id="ebc87-114">**BUTTONGROUP** не является стилем радио.</span><span class="sxs-lookup"><span data-stu-id="ebc87-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ebc87-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ebc87-115">Remarks</span></span>

<span data-ttu-id="ebc87-116">Если параметру **Radio** присвоено значение true, все элементы **буттонелемент** в **BUTTONGROUP** будут закрепляться, но только одна кнопка будет находиться в неправильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ebc87-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc87-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ebc87-117">Requirements</span></span>



| <span data-ttu-id="ebc87-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ebc87-118">Requirement</span></span> | <span data-ttu-id="ebc87-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ebc87-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ebc87-120">Версия</span><span class="sxs-lookup"><span data-stu-id="ebc87-120">Version</span></span><br/> | <span data-ttu-id="ebc87-121">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ebc87-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebc87-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebc87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc87-123">**БУТТОНЕЛЕМЕНТ. Клейкие**</span><span class="sxs-lookup"><span data-stu-id="ebc87-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="ebc87-124">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="ebc87-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





