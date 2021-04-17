---
description: Указывает, был ли извлеченный видеокадр получен из верхнего или нижнего поля.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Атрибут MFSampleExtension_DerivedFromTopField (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692792"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="b99bb-103">Мфсампликстенсион \_ дериведфромтопфиелд, атрибут</span><span class="sxs-lookup"><span data-stu-id="b99bb-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="b99bb-104">Указывает, был ли извлеченный видеокадр получен из верхнего или нижнего поля.</span><span class="sxs-lookup"><span data-stu-id="b99bb-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="b99bb-105">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b99bb-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="b99bb-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b99bb-106">Data type</span></span>

<span data-ttu-id="b99bb-107">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b99bb-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b99bb-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b99bb-108">Get/set</span></span>

<span data-ttu-id="b99bb-109">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b99bb-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b99bb-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b99bb-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b99bb-111">Применяется к</span><span class="sxs-lookup"><span data-stu-id="b99bb-111">Applies to</span></span>

[<span data-ttu-id="b99bb-112">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="b99bb-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b99bb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b99bb-113">Remarks</span></span>

<span data-ttu-id="b99bb-114">Этот атрибут допустим только для образцов с нечередованием.</span><span class="sxs-lookup"><span data-stu-id="b99bb-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="b99bb-115">Установите этот атрибут, если фрейм был раззагружен путем интерполяции одного из полей.</span><span class="sxs-lookup"><span data-stu-id="b99bb-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="b99bb-116">Если значение равно **true**, то нижнее поле было интерполяции из верхнего поля.</span><span class="sxs-lookup"><span data-stu-id="b99bb-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="b99bb-117">Если значение равно **false**, верхнее поле было интерполяция от нижнего поля.</span><span class="sxs-lookup"><span data-stu-id="b99bb-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="b99bb-118">Если атрибут не задан, кадр не был развернут.</span><span class="sxs-lookup"><span data-stu-id="b99bb-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="b99bb-119">Кадр является либо истинным прогрессивным кадром, либо чередованием кадров.</span><span class="sxs-lookup"><span data-stu-id="b99bb-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="b99bb-120">Этот атрибут является информационным.</span><span class="sxs-lookup"><span data-stu-id="b99bb-120">This attribute is informational.</span></span> <span data-ttu-id="b99bb-121">Этот атрибут может быть установлен программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="b99bb-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="b99bb-122">Если этот атрибут задан, он предоставляет указание, что можно восстановить исходное поле, удалив строки с интерполяцией.</span><span class="sxs-lookup"><span data-stu-id="b99bb-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="b99bb-123">Например, если атрибут имеет **значение true**, можно восстановить исходное верхнее поле, удалив нижнее поле с интерполяцией.</span><span class="sxs-lookup"><span data-stu-id="b99bb-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="b99bb-124">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b99bb-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99bb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b99bb-125">Requirements</span></span>



| <span data-ttu-id="b99bb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b99bb-126">Requirement</span></span> | <span data-ttu-id="b99bb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b99bb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b99bb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b99bb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b99bb-129">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="b99bb-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b99bb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b99bb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b99bb-131">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b99bb-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b99bb-132">Header</span><span class="sxs-lookup"><span data-stu-id="b99bb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b99bb-133"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b99bb-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99bb-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b99bb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99bb-135">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b99bb-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b99bb-136">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="b99bb-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="b99bb-137">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="b99bb-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="b99bb-138">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="b99bb-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




