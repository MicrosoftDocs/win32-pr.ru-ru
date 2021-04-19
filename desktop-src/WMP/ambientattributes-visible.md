---
title: Амбиентаттрибутес. Visible
description: Атрибут Visible указывает или получает видимость для элемента управления.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Амбиентаттрибутес. видимый проигрыватель Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698957"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="651b3-104">Амбиентаттрибутес. Visible</span><span class="sxs-lookup"><span data-stu-id="651b3-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="651b3-105">Атрибут **Visible** указывает или получает видимость для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="651b3-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="651b3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="651b3-106">Possible Values</span></span>

<span data-ttu-id="651b3-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="651b3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="651b3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="651b3-108">Value</span></span> | <span data-ttu-id="651b3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="651b3-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="651b3-110">true</span><span class="sxs-lookup"><span data-stu-id="651b3-110">true</span></span>  | <span data-ttu-id="651b3-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="651b3-111">Default.</span></span> <span data-ttu-id="651b3-112">Элемент управления является видимым.</span><span class="sxs-lookup"><span data-stu-id="651b3-112">The control is visible.</span></span> |
| <span data-ttu-id="651b3-113">false</span><span class="sxs-lookup"><span data-stu-id="651b3-113">false</span></span> | <span data-ttu-id="651b3-114">Элемент управления невидим.</span><span class="sxs-lookup"><span data-stu-id="651b3-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="651b3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="651b3-115">Remarks</span></span>

<span data-ttu-id="651b3-116">Этот атрибут полезен для скрытия элементов управления, например при переключении кнопки паузы на кнопку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="651b3-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="651b3-117">Если значение равно false, элемент управления не отображается, а события щелчка передаются в элемент управления, лежащий за ним.</span><span class="sxs-lookup"><span data-stu-id="651b3-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="651b3-118">Если значение равно true, элемент управления является видимым и получает событие Click.</span><span class="sxs-lookup"><span data-stu-id="651b3-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="651b3-119">Значение по умолчанию для элемента **АВТОМЕНЮ** — false.</span><span class="sxs-lookup"><span data-stu-id="651b3-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="651b3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="651b3-120">Requirements</span></span>



| <span data-ttu-id="651b3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="651b3-121">Requirement</span></span> | <span data-ttu-id="651b3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="651b3-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="651b3-123">Версия</span><span class="sxs-lookup"><span data-stu-id="651b3-123">Version</span></span><br/> | <span data-ttu-id="651b3-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="651b3-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="651b3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="651b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651b3-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="651b3-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





