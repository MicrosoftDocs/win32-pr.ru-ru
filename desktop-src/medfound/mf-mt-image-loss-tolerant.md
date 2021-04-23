---
description: Указывает, является ли поток изображений ASF типом деградабле JPEG.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Атрибут MF_MT_IMAGE_LOSS_TOLERANT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897514"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="495ef-103">\_ \_ \_ \_ Атрибут нечувствительного к утере образа MF</span><span class="sxs-lookup"><span data-stu-id="495ef-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="495ef-104">Указывает, является ли поток изображений ASF типом деградабле JPEG.</span><span class="sxs-lookup"><span data-stu-id="495ef-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="495ef-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="495ef-105">Data type</span></span>

<span data-ttu-id="495ef-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="495ef-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="495ef-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="495ef-107">Get/set</span></span>

<span data-ttu-id="495ef-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="495ef-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="495ef-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="495ef-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="495ef-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="495ef-110">Applies to</span></span>

[<span data-ttu-id="495ef-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="495ef-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="495ef-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="495ef-112">Remarks</span></span>

<span data-ttu-id="495ef-113">Этот атрибут применяется к типу мультимедиа для потоков изображений в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="495ef-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="495ef-114">Если значение равно **true**, то поток является типом изображения деградабле JPEG.</span><span class="sxs-lookup"><span data-stu-id="495ef-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="495ef-115">В противном случае поток является типом изображения JFIF.</span><span class="sxs-lookup"><span data-stu-id="495ef-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="495ef-116">Дополнительные сведения об этих типах потоков см. в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="495ef-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="495ef-117">Помимо \_ \_ \_ \_ нечувствительного к сбоям образа, тип носителя для потока изображений ASF содержит следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="495ef-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="495ef-118">attribute</span><span class="sxs-lookup"><span data-stu-id="495ef-118">Attribute</span></span>                                                 | <span data-ttu-id="495ef-119">Описание</span><span class="sxs-lookup"><span data-stu-id="495ef-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="495ef-120">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="495ef-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="495ef-121">Содержит изображение value **мфмедиатипе \_**.</span><span class="sxs-lookup"><span data-stu-id="495ef-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="495ef-122">**\_ \_ Размер пакета MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="495ef-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="495ef-123">Задает размер изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="495ef-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="495ef-124">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="495ef-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="495ef-125">Требования</span><span class="sxs-lookup"><span data-stu-id="495ef-125">Requirements</span></span>



| <span data-ttu-id="495ef-126">Требование</span><span class="sxs-lookup"><span data-stu-id="495ef-126">Requirement</span></span> | <span data-ttu-id="495ef-127">Значение</span><span class="sxs-lookup"><span data-stu-id="495ef-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="495ef-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="495ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="495ef-129">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="495ef-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="495ef-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="495ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="495ef-131">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="495ef-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="495ef-132">Header</span><span class="sxs-lookup"><span data-stu-id="495ef-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="495ef-133"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="495ef-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495ef-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="495ef-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495ef-135">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="495ef-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="495ef-136">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="495ef-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




