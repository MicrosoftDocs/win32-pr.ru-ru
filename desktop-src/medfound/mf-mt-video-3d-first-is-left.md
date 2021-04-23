---
description: Для формата 3D-видео указывает, какое представление является левым представлением.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Атрибут MF_MT_VIDEO_3D_FIRST_IS_LEFT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424057"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="ad794-103">\_ \_ \_ Первый трехмерный видеоролик \_ \_ — \_ левый атрибут</span><span class="sxs-lookup"><span data-stu-id="ad794-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="ad794-104">Для формата 3D-видео указывает, какое представление является левым представлением.</span><span class="sxs-lookup"><span data-stu-id="ad794-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad794-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ad794-105">Data type</span></span>

<span data-ttu-id="ad794-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad794-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad794-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad794-107">Remarks</span></span>

<span data-ttu-id="ad794-108">Для трехмерного видео каждый пример видео содержит два представления, которые обозначены как *первое представление* и *второе представление*.</span><span class="sxs-lookup"><span data-stu-id="ad794-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="ad794-109">Точный макет представлений в памяти определяется атрибутом [ \_ \_ \_ трехмерного видео в \_ формате MF MT](mf-mt-video-3d-format.md) .</span><span class="sxs-lookup"><span data-stu-id="ad794-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="ad794-110">Формат</span><span class="sxs-lookup"><span data-stu-id="ad794-110">Format</span></span>               | <span data-ttu-id="ad794-111">Первое представление</span><span class="sxs-lookup"><span data-stu-id="ad794-111">First View</span></span>              | <span data-ttu-id="ad794-112">Второе представление</span><span class="sxs-lookup"><span data-stu-id="ad794-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="ad794-113">Упакованная параллельно</span><span class="sxs-lookup"><span data-stu-id="ad794-113">Packed side-by-side</span></span>  | <span data-ttu-id="ad794-114">Левая половина буфера</span><span class="sxs-lookup"><span data-stu-id="ad794-114">Left half of the buffer</span></span> | <span data-ttu-id="ad794-115">Правая половина буфера</span><span class="sxs-lookup"><span data-stu-id="ad794-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="ad794-116">Упакованные сверху вниз</span><span class="sxs-lookup"><span data-stu-id="ad794-116">Packed top-to-bottom</span></span> | <span data-ttu-id="ad794-117">Верхняя половина буфера</span><span class="sxs-lookup"><span data-stu-id="ad794-117">Top half of the buffer</span></span>  | <span data-ttu-id="ad794-118">Нижняя половина буфера</span><span class="sxs-lookup"><span data-stu-id="ad794-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="ad794-119">MultiView</span><span class="sxs-lookup"><span data-stu-id="ad794-119">Multiview</span></span>            | <span data-ttu-id="ad794-120">Индекс буфера 0</span><span class="sxs-lookup"><span data-stu-id="ad794-120">Buffer index 0</span></span>          | <span data-ttu-id="ad794-121">Индекс буфера 1</span><span class="sxs-lookup"><span data-stu-id="ad794-121">Buffer index 1</span></span>            |
| <span data-ttu-id="ad794-122">Базовое представление</span><span class="sxs-lookup"><span data-stu-id="ad794-122">Base view</span></span>            | <span data-ttu-id="ad794-123">Весь кадр</span><span class="sxs-lookup"><span data-stu-id="ad794-123">Entire frame</span></span>            | <span data-ttu-id="ad794-124">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ad794-124">Not present</span></span>               |



 

<span data-ttu-id="ad794-125">По умолчанию первое представление представляет собой левое представление, а второе — в правильном представлении.</span><span class="sxs-lookup"><span data-stu-id="ad794-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="ad794-126">Если левое и правое представления меняются местами, установите в поле \_ \_ \_ \_ \_ \_ тип мультимедиа значение **false** для параметра 3D-видео MF.</span><span class="sxs-lookup"><span data-stu-id="ad794-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="ad794-127">В формате *базового представления* (**MFVideo3DSampleFormat \_ басевиев**) сохраняется только базовое представление, поэтому этот атрибут не применяется.</span><span class="sxs-lookup"><span data-stu-id="ad794-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad794-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ad794-128">Requirements</span></span>



| <span data-ttu-id="ad794-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ad794-129">Requirement</span></span> | <span data-ttu-id="ad794-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ad794-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad794-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad794-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ad794-132">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="ad794-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ad794-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad794-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ad794-134">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="ad794-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ad794-135">Header</span><span class="sxs-lookup"><span data-stu-id="ad794-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad794-136"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad794-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad794-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad794-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad794-138">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad794-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




