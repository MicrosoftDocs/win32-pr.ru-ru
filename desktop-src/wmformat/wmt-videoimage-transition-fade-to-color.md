---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Вмсдкидл. h)
description: Переход от исчезания к цвету разрешается из изображения в кадр сплошного цвета.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694920"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="838af-104">ВМТ \_ видеоимаже \_ Переход \_ \_ к \_ цвету</span><span class="sxs-lookup"><span data-stu-id="838af-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="838af-105">Переход от исчезания к цвету разрешается из изображения в кадр сплошного цвета.</span><span class="sxs-lookup"><span data-stu-id="838af-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="838af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="838af-106">Parameters</span></span>

<span data-ttu-id="838af-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="838af-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="838af-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="838af-108">Parameter</span></span>         | <span data-ttu-id="838af-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="838af-109">Structure member</span></span> | <span data-ttu-id="838af-110">Описание</span><span class="sxs-lookup"><span data-stu-id="838af-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838af-111">Красный</span><span class="sxs-lookup"><span data-stu-id="838af-111">Red</span></span>               | <span data-ttu-id="838af-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="838af-112">**fEffectPara0**</span></span> | <span data-ttu-id="838af-113">Красное значение цвета фона.</span><span class="sxs-lookup"><span data-stu-id="838af-113">Red value of the background color.</span></span> <span data-ttu-id="838af-114">Задайте значение в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="838af-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="838af-115">Зеленый</span><span class="sxs-lookup"><span data-stu-id="838af-115">Green</span></span>             | <span data-ttu-id="838af-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="838af-116">**fEffectPara1**</span></span> | <span data-ttu-id="838af-117">Зеленое значение цвета фона.</span><span class="sxs-lookup"><span data-stu-id="838af-117">Green value of the background color.</span></span> <span data-ttu-id="838af-118">Задайте значение в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="838af-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="838af-119">Синий</span><span class="sxs-lookup"><span data-stu-id="838af-119">Blue</span></span>              | <span data-ttu-id="838af-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="838af-120">**fEffectPara2**</span></span> | <span data-ttu-id="838af-121">Синее значение цвета фона.</span><span class="sxs-lookup"><span data-stu-id="838af-121">Blue value of the background color.</span></span> <span data-ttu-id="838af-122">Задайте значение в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="838af-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="838af-123">Вес фона</span><span class="sxs-lookup"><span data-stu-id="838af-123">Background weight</span></span> | <span data-ttu-id="838af-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="838af-124">**fEffectPara3**</span></span> | <span data-ttu-id="838af-125">Вес цвета фона.</span><span class="sxs-lookup"><span data-stu-id="838af-125">Weight of the background color.</span></span> <span data-ttu-id="838af-126">Этот параметр выражает процентный показатель цвета фона в наборе в виде десятичного значения.</span><span class="sxs-lookup"><span data-stu-id="838af-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="838af-127">Например, для смешения цвета фона с 30%, установив для изображения 70% набора значение 0,30.</span><span class="sxs-lookup"><span data-stu-id="838af-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="838af-128">Требования</span><span class="sxs-lookup"><span data-stu-id="838af-128">Requirements</span></span>



| <span data-ttu-id="838af-129">Требование</span><span class="sxs-lookup"><span data-stu-id="838af-129">Requirement</span></span> | <span data-ttu-id="838af-130">Значение</span><span class="sxs-lookup"><span data-stu-id="838af-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="838af-131">Header</span><span class="sxs-lookup"><span data-stu-id="838af-131">Header</span></span><br/> | <dl> <span data-ttu-id="838af-132"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="838af-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838af-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="838af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838af-134">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="838af-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





