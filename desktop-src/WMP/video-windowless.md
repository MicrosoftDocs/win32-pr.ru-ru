---
title: ВИДЕО. без окон
description: Атрибут без окон указывает или получает значение, указывающее, будет ли элемент управления видео отображаться в окне или без окон; то есть независимо от того, будет ли весь прямоугольник элемента управления видимым в любое время или же его можно обрезать.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- Проигрыватель Windows Media без окон видео
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704461"
---
# <a name="videowindowless"></a><span data-ttu-id="afaa4-104">ВИДЕО. без окон</span><span class="sxs-lookup"><span data-stu-id="afaa4-104">VIDEO.windowless</span></span>

<span data-ttu-id="afaa4-105">Атрибут без **окон** указывает или получает значение, указывающее, будет ли элемент управления видео отображаться в окне или без окон; то есть независимо от того, будет ли весь прямоугольник элемента управления видимым в любое время или же его можно обрезать.</span><span class="sxs-lookup"><span data-stu-id="afaa4-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="afaa4-106">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="afaa4-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="afaa4-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="afaa4-107">Possible Values</span></span>

<span data-ttu-id="afaa4-108">Этот атрибут является **логическим** , заданным во время разработки, и затем доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="afaa4-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="afaa4-109">Значение</span><span class="sxs-lookup"><span data-stu-id="afaa4-109">Value</span></span> | <span data-ttu-id="afaa4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="afaa4-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="afaa4-111">true</span><span class="sxs-lookup"><span data-stu-id="afaa4-111">true</span></span>  | <span data-ttu-id="afaa4-112">Элемент управления видео будет безоконным.</span><span class="sxs-lookup"><span data-stu-id="afaa4-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="afaa4-113">false</span><span class="sxs-lookup"><span data-stu-id="afaa4-113">false</span></span> | <span data-ttu-id="afaa4-114">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="afaa4-114">Default.</span></span> <span data-ttu-id="afaa4-115">Элемент управления видео будет отображаться в окне.</span><span class="sxs-lookup"><span data-stu-id="afaa4-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="afaa4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afaa4-116">Remarks</span></span>

<span data-ttu-id="afaa4-117">Если требуется Непрямоугольное видео-окно или вы хотите охватить любую часть видеоокна с изображением, этот атрибут должен иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="afaa4-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="afaa4-118">Это потребует некоторой производительности для выполнения необходимой обрезки.</span><span class="sxs-lookup"><span data-stu-id="afaa4-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="afaa4-119">Воспроизведение видео оптимизировано для необрезанного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="afaa4-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="afaa4-120">В этом случае атрибут без **окон** имеет значение false, и всегда отображается весь прямоугольник видео.</span><span class="sxs-lookup"><span data-stu-id="afaa4-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="afaa4-121">Все изображения, охватывающие окно видео, игнорируются, и в окне видео отображается z-порядок самого высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="afaa4-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="afaa4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="afaa4-122">Requirements</span></span>



| <span data-ttu-id="afaa4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="afaa4-123">Requirement</span></span> | <span data-ttu-id="afaa4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="afaa4-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="afaa4-125">Версия</span><span class="sxs-lookup"><span data-stu-id="afaa4-125">Version</span></span><br/> | <span data-ttu-id="afaa4-126">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="afaa4-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afaa4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afaa4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afaa4-128">**Элемент VIDEO**</span><span class="sxs-lookup"><span data-stu-id="afaa4-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





