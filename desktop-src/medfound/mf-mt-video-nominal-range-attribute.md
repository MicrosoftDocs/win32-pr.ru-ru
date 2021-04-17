---
description: Определяет Номинальный диапазон сведений о цвете в видеоролике.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Атрибут MF_MT_VIDEO_NOMINAL_RANGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674343"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="a8794-103">\_ \_ \_ Атрибут диапазона номинального видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="a8794-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="a8794-104">Определяет Номинальный диапазон сведений о цвете в видеоролике.</span><span class="sxs-lookup"><span data-stu-id="a8794-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8794-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a8794-105">Data type</span></span>

<span data-ttu-id="a8794-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a8794-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8794-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8794-107">Remarks</span></span>

<span data-ttu-id="a8794-108">Значение этого атрибута является членом перечисления [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .</span><span class="sxs-lookup"><span data-stu-id="a8794-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="a8794-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a8794-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="a8794-110">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="a8794-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="a8794-111">На выходном типе носителя для \_ \_ параметра номинальный формат видео MF MT \_ \_ можно задать значение **мфноминалранже \_ 0 \_ 255** и **мфноминалранже \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="a8794-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="a8794-112">Кодировщик H. 264/AVC должен обрабатывать **мфноминалранже \_ Unknown** как **мфноминалранже \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="a8794-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="a8794-113">H. 264/AVC-кодировщик должен отклонить тип выходного \_ носителя \_ \_ , если Номинальный диапазон для видео MF MT \_ имеет значение **мфноминалранже \_ 48 \_ 208**, **мфноминалранже \_ 64 \_ 127** или любые другие значения, не определенные в [**мфноминалранже**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span><span class="sxs-lookup"><span data-stu-id="a8794-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8794-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a8794-114">Requirements</span></span>



| <span data-ttu-id="a8794-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a8794-115">Requirement</span></span> | <span data-ttu-id="a8794-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a8794-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8794-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8794-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8794-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a8794-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a8794-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8794-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8794-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a8794-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a8794-121">Header</span><span class="sxs-lookup"><span data-stu-id="a8794-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8794-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8794-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8794-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8794-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8794-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8794-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8794-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="a8794-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a8794-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a8794-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a8794-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a8794-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a8794-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a8794-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8794-129">Расширенные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="a8794-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




