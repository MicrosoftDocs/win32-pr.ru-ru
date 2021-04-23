---
title: ЭФФЕКТЫ. окна
description: Атрибут Window указывает или получает значение, указывающее, будет ли визуализация отображаться в окне или без окон, то есть независимо от того, будет ли весь прямоугольник элемента управления видимым в любое время или же он может быть обрезан.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- ЭФФЕКТЫ. оконный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699205"
---
# <a name="effectswindowed"></a><span data-ttu-id="5546b-104">ЭФФЕКТЫ. окна</span><span class="sxs-lookup"><span data-stu-id="5546b-104">EFFECTS.windowed</span></span>

<span data-ttu-id="5546b-105">Атрибут **Window** указывает или получает значение, указывающее, будет ли визуализация отображаться в окне или без окон, то есть независимо от того, будет ли весь прямоугольник элемента управления видимым в любое время или же он может быть обрезан.</span><span class="sxs-lookup"><span data-stu-id="5546b-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="5546b-106">Этот атрибут можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="5546b-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="5546b-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5546b-107">Possible Values</span></span>

<span data-ttu-id="5546b-108">Этот атрибут является **логическим** , заданным во время разработки, и затем доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5546b-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="5546b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5546b-109">Value</span></span> | <span data-ttu-id="5546b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5546b-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="5546b-111">true</span><span class="sxs-lookup"><span data-stu-id="5546b-111">true</span></span>  | <span data-ttu-id="5546b-112">Элемент управления будет отображаться в окне.</span><span class="sxs-lookup"><span data-stu-id="5546b-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="5546b-113">false</span><span class="sxs-lookup"><span data-stu-id="5546b-113">false</span></span> | <span data-ttu-id="5546b-114">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5546b-114">Default.</span></span> <span data-ttu-id="5546b-115">Элемент управления будет безоконным.</span><span class="sxs-lookup"><span data-stu-id="5546b-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5546b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5546b-116">Remarks</span></span>

<span data-ttu-id="5546b-117">Если требуется Непрямоугольное окно визуализации или если какая-либо часть окна охватывается изображением, этот атрибут должен иметь значение false.</span><span class="sxs-lookup"><span data-stu-id="5546b-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="5546b-118">Это потребует некоторой производительности для выполнения необходимой обрезки.</span><span class="sxs-lookup"><span data-stu-id="5546b-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="5546b-119">Если для **окон** задано значение true, все изображения, охватывающие окно визуализации, игнорируются, а в окне визуализации отображается z-порядок самого высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5546b-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="5546b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5546b-120">Requirements</span></span>



| <span data-ttu-id="5546b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5546b-121">Requirement</span></span> | <span data-ttu-id="5546b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5546b-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5546b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="5546b-123">Version</span></span><br/> | <span data-ttu-id="5546b-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="5546b-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5546b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5546b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5546b-126">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="5546b-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





