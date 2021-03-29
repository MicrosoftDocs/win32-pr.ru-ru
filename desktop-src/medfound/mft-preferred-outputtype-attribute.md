---
description: Указывает предпочтительный выходной формат кодировщика.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Атрибут MFT_PREFERRED_OUTPUTTYPE_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898725"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="917f0-103">\_ \_ Атрибут атрибута OUTPUTTYPE, предпочтительный для MFT \_</span><span class="sxs-lookup"><span data-stu-id="917f0-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="917f0-104">Указывает предпочтительный выходной формат кодировщика.</span><span class="sxs-lookup"><span data-stu-id="917f0-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="917f0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="917f0-105">Data type</span></span>

<span data-ttu-id="917f0-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Имфаттрибутес \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="917f0-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="917f0-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="917f0-107">Get/set</span></span>

<span data-ttu-id="917f0-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="917f0-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="917f0-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="917f0-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="917f0-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="917f0-110">Applies to</span></span>

[<span data-ttu-id="917f0-111">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="917f0-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="917f0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="917f0-112">Remarks</span></span>

<span data-ttu-id="917f0-113">Этот атрибут может быть задан для объекта активации, возвращаемого функцией [**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="917f0-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="917f0-114">Атрибут применяется только в том случае, если объект активации настроен для создания кодировщика.</span><span class="sxs-lookup"><span data-stu-id="917f0-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="917f0-115">Значением атрибута является тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="917f0-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="917f0-116">Объект активации задает этот тип выходных данных для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="917f0-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="917f0-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="917f0-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="917f0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="917f0-118">Requirements</span></span>



| <span data-ttu-id="917f0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="917f0-119">Requirement</span></span> | <span data-ttu-id="917f0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="917f0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="917f0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="917f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="917f0-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="917f0-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="917f0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="917f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="917f0-124">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="917f0-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="917f0-125">Header</span><span class="sxs-lookup"><span data-stu-id="917f0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="917f0-126"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="917f0-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917f0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="917f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917f0-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="917f0-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="917f0-129">**мфкреатетрансформактивате**</span><span class="sxs-lookup"><span data-stu-id="917f0-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="917f0-130">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="917f0-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




