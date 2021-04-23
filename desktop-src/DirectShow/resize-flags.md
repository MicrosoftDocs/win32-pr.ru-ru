---
description: Эти флаги определяют, как отображается источник видео, если его размер не соответствует выходным измерениям.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Флаги изменения размера (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689133"
---
# <a name="resize-flags"></a><span data-ttu-id="b9948-103">Изменение размера флагов</span><span class="sxs-lookup"><span data-stu-id="b9948-103">Resize Flags</span></span>

<span data-ttu-id="b9948-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b9948-104">\[Deprecated.</span></span> <span data-ttu-id="b9948-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9948-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="b9948-106">Эти флаги определяют, как отображается источник видео, если его размер не соответствует выходным измерениям.</span><span class="sxs-lookup"><span data-stu-id="b9948-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="b9948-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="b9948-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="b9948-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b9948-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="b9948-109"><dt>**Ресизеф \_ РАСТЯЖЕНИе**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9948-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="b9948-110">Изображение растягивается в соответствии с размером целевого кадра в обоих измерениях без сохранения пропорций.</span><span class="sxs-lookup"><span data-stu-id="b9948-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="b9948-111"><dt>**Ресизеф \_ Обрезать**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b9948-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="b9948-112">Размер изображения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b9948-112">The image is not resized.</span></span> <span data-ttu-id="b9948-113">Если изображение меньше целевого кадра, окружающая область будет черным.</span><span class="sxs-lookup"><span data-stu-id="b9948-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="b9948-114">Если изображение больше целевого кадра, изображение обрезается.</span><span class="sxs-lookup"><span data-stu-id="b9948-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="b9948-115"><dt>**Ресизеф \_ ПРЕСЕРВЕАСПЕКТРАТИО**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b9948-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="b9948-116">Размер изображения изменяется в соответствии с целевым кадром по одному измерению с сохранением пропорций.</span><span class="sxs-lookup"><span data-stu-id="b9948-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="b9948-117">Если отношение ширины к высоте в изображении не соответствует соотношениям в целевом кадре, создается леттербокс.</span><span class="sxs-lookup"><span data-stu-id="b9948-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="b9948-118"><dt>**Ресизеф \_ ПРЕСЕРВЕАСПЕКТРАТИО \_ нолеттербокс**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b9948-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b9948-119">Размер изображения изменяется для заполнения всего целевого фрейма с сохранением пропорций.</span><span class="sxs-lookup"><span data-stu-id="b9948-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="b9948-120">Вместо создания леттербокс в этом режиме изображение обрезается по сторонам или вдоль верхней и нижней части.</span><span class="sxs-lookup"><span data-stu-id="b9948-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="b9948-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9948-121">Remarks</span></span>

<span data-ttu-id="b9948-122">На следующих изображениях показано влияние этих флагов.</span><span class="sxs-lookup"><span data-stu-id="b9948-122">The following images show the effects of these flags.</span></span>

![изменение размера флагов](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="b9948-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b9948-124">Requirements</span></span>



| <span data-ttu-id="b9948-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b9948-125">Requirement</span></span> | <span data-ttu-id="b9948-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b9948-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9948-127">Header</span><span class="sxs-lookup"><span data-stu-id="b9948-127">Header</span></span><br/> | <dl> <span data-ttu-id="b9948-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9948-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9948-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9948-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9948-130">**Иамтимелинесрк:: Жетстретчмоде**</span><span class="sxs-lookup"><span data-stu-id="b9948-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="b9948-131">**Иамтимелинесрк:: Сетстретчмоде**</span><span class="sxs-lookup"><span data-stu-id="b9948-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




