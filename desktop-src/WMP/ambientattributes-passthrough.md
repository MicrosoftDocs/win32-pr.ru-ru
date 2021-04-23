---
title: Амбиентаттрибутес. passThrough
description: Атрибут passThrough указывает или получает значение, указывающее, будет ли элемент управления передавать все события мыши через элемент управления под ним.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Амбиентаттрибутес. транзитный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694766"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="00faa-104">Амбиентаттрибутес. passThrough</span><span class="sxs-lookup"><span data-stu-id="00faa-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="00faa-105">Атрибут **passThrough** указывает или получает значение, указывающее, будет ли элемент управления передавать все события мыши через элемент управления под ним.</span><span class="sxs-lookup"><span data-stu-id="00faa-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="00faa-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="00faa-106">Possible Values</span></span>

<span data-ttu-id="00faa-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="00faa-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="00faa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="00faa-108">Value</span></span> | <span data-ttu-id="00faa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="00faa-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="00faa-110">true</span><span class="sxs-lookup"><span data-stu-id="00faa-110">true</span></span>  | <span data-ttu-id="00faa-111">Элемент управления передает события в элемент управления под ним.</span><span class="sxs-lookup"><span data-stu-id="00faa-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="00faa-112">false</span><span class="sxs-lookup"><span data-stu-id="00faa-112">false</span></span> | <span data-ttu-id="00faa-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00faa-113">Default.</span></span> <span data-ttu-id="00faa-114">Элемент управления не передает события через.</span><span class="sxs-lookup"><span data-stu-id="00faa-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="00faa-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00faa-115">Remarks</span></span>

<span data-ttu-id="00faa-116">Этот атрибут полезен, если, например, текстовый элемент управления располагается поверх элемента управления "Кнопка" только для предоставления меток.</span><span class="sxs-lookup"><span data-stu-id="00faa-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="00faa-117">В этом случае щелчки элемента управления "текст" должны передаваться в элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="00faa-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="00faa-118">Атрибут **passThrough** не поддерживается элементами **представления**, вложенного **представления** и **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="00faa-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="00faa-119">Он не будет работать с элементом **Video** , если *видео*. **окно без окон** имеет значение false или элемент **Effects** , если он имеет *эффект*. для **окон** задано значение true.</span><span class="sxs-lookup"><span data-stu-id="00faa-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="00faa-120">Требования</span><span class="sxs-lookup"><span data-stu-id="00faa-120">Requirements</span></span>



| <span data-ttu-id="00faa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="00faa-121">Requirement</span></span> | <span data-ttu-id="00faa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="00faa-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="00faa-123">Версия</span><span class="sxs-lookup"><span data-stu-id="00faa-123">Version</span></span><br/> | <span data-ttu-id="00faa-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="00faa-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00faa-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00faa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00faa-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="00faa-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





