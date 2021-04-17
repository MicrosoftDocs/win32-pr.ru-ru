---
title: LISTBOX. popUp
description: Атрибут popUp задает значение, указывающее, представляет ли элемент элемент управления "всплывающее окно" или "список".
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- Проигрыватель Windows Media LISTBOX. popUp
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704424"
---
# <a name="listboxpopup"></a><span data-ttu-id="8b4eb-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="8b4eb-104">LISTBOX.popUp</span></span>

<span data-ttu-id="8b4eb-105">Атрибут **popUp** задает значение, указывающее, представляет ли элемент элемент управления "всплывающее окно" или "список".</span><span class="sxs-lookup"><span data-stu-id="8b4eb-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="8b4eb-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8b4eb-106">Possible Values</span></span>

<span data-ttu-id="8b4eb-107">Этот атрибут является **логическим** , заданным только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="8b4eb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8b4eb-108">Value</span></span> | <span data-ttu-id="8b4eb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8b4eb-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="8b4eb-110">true</span><span class="sxs-lookup"><span data-stu-id="8b4eb-110">true</span></span>  | <span data-ttu-id="8b4eb-111">Элемент представляет элемент управления Popup.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="8b4eb-112">false</span><span class="sxs-lookup"><span data-stu-id="8b4eb-112">false</span></span> | <span data-ttu-id="8b4eb-113">Элемент представляет элемент управления "список".</span><span class="sxs-lookup"><span data-stu-id="8b4eb-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8b4eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b4eb-114">Remarks</span></span>

<span data-ttu-id="8b4eb-115">Элемент **Popup** представляет элемент управления "список", который отображается только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="8b4eb-116">Он идентичен элементу **ListBox** , за исключением значения по умолчанию этого атрибута, которое изменяет поведение экрана.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="8b4eb-117">Для элементов **ListBox** значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="8b4eb-118">Для элементов **Popup** значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="8b4eb-119">Вместо указания этого атрибута следует использовать элемент **ListBox** или **Popup** в соответствии с желаемым поведением.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4eb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8b4eb-120">Requirements</span></span>



| <span data-ttu-id="8b4eb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8b4eb-121">Requirement</span></span> | <span data-ttu-id="8b4eb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8b4eb-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="8b4eb-123">Версия</span><span class="sxs-lookup"><span data-stu-id="8b4eb-123">Version</span></span><br/> | <span data-ttu-id="8b4eb-124">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8b4eb-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b4eb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b4eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4eb-126">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="8b4eb-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="8b4eb-127">**Элемент POPUP**</span><span class="sxs-lookup"><span data-stu-id="8b4eb-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





