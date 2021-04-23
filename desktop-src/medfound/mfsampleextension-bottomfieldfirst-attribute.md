---
description: Задает поле превосходство для чередующихся видеокадров.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Атрибут MFSampleExtension_BottomFieldFirst (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344865"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="1e0e7-103">Мфсампликстенсион \_ боттомфиелдфирст, атрибут</span><span class="sxs-lookup"><span data-stu-id="1e0e7-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="1e0e7-104">Задает поле превосходство для чередующихся видеокадров.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="1e0e7-105">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e0e7-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1e0e7-106">Data type</span></span>

<span data-ttu-id="1e0e7-107">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e0e7-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1e0e7-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="1e0e7-108">Get/set</span></span>

<span data-ttu-id="1e0e7-109">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1e0e7-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1e0e7-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1e0e7-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1e0e7-111">Применяется к</span><span class="sxs-lookup"><span data-stu-id="1e0e7-111">Applies to</span></span>

[<span data-ttu-id="1e0e7-112">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="1e0e7-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="1e0e7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e0e7-113">Remarks</span></span>

<span data-ttu-id="1e0e7-114">Если видеокадр имеет чередование, а образец содержит два поля с чередованием, этот атрибут указывает, какое поле отображается первым.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="1e0e7-115">Если **значение равно true**, то нижнее поле является первым по времени.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="1e0e7-116">Если **значение равно false**, верхнее поле является первым.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="1e0e7-117">Если кадр является чередованием, а образец содержит одно поле, этот атрибут указывает, какое поле в образце содержит.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="1e0e7-118">Если **значение — true**, образец содержит нижнее поле.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="1e0e7-119">Если **значение равно false**, образец содержит верхнее поле.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="1e0e7-120">Если кадр является прогрессивным, этот атрибут описывает порядок упорядочивания полей при чередовании выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="1e0e7-121">Если **значение равно true**, то нижнее поле должно выводиться первыми.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="1e0e7-122">Если **значение равно false**, верхнее поле должно быть выведено первым.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="1e0e7-123">Если этот атрибут не задан, тип носителя описывает поле превосходство.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="1e0e7-124">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="1e0e7-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0e7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1e0e7-125">Requirements</span></span>



| <span data-ttu-id="1e0e7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1e0e7-126">Requirement</span></span> | <span data-ttu-id="1e0e7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1e0e7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0e7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e0e7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0e7-129">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="1e0e7-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1e0e7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e0e7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0e7-131">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1e0e7-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1e0e7-132">Header</span><span class="sxs-lookup"><span data-stu-id="1e0e7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e0e7-133"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e0e7-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0e7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e0e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0e7-135">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e0e7-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e0e7-136">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="1e0e7-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e0e7-137">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="1e0e7-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="1e0e7-138">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="1e0e7-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




