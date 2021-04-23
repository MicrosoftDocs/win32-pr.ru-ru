---
description: Указывает режим использования кодировщика УВК H. 264.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: Атрибут MF_MT_H264_USAGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145604"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="80e88-103">\_ \_ Атрибут использования H264 Single bitrate MF MT \_</span><span class="sxs-lookup"><span data-stu-id="80e88-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="80e88-104">Указывает режим использования кодировщика УВК H. 264.</span><span class="sxs-lookup"><span data-stu-id="80e88-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="80e88-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80e88-105">Data type</span></span>

<span data-ttu-id="80e88-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="80e88-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="80e88-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="80e88-107">Get/set</span></span>

<span data-ttu-id="80e88-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="80e88-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="80e88-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="80e88-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="80e88-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="80e88-110">Applies to</span></span>

[<span data-ttu-id="80e88-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="80e88-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="80e88-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80e88-112">Remarks</span></span>

<span data-ttu-id="80e88-113">Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB.</span><span class="sxs-lookup"><span data-stu-id="80e88-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="80e88-114">Значение соответствует полю **бусаже** в элементе управления зонда/commit УВК 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="80e88-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e88-115">Требования</span><span class="sxs-lookup"><span data-stu-id="80e88-115">Requirements</span></span>



| <span data-ttu-id="80e88-116">Требование</span><span class="sxs-lookup"><span data-stu-id="80e88-116">Requirement</span></span> | <span data-ttu-id="80e88-117">Значение</span><span class="sxs-lookup"><span data-stu-id="80e88-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80e88-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80e88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80e88-119">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="80e88-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="80e88-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80e88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80e88-121">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="80e88-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="80e88-122">Header</span><span class="sxs-lookup"><span data-stu-id="80e88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e88-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="80e88-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e88-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80e88-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e88-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80e88-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80e88-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80e88-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




