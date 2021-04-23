---
description: Содержит свойства конфигурации кодировщика.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Атрибут MFT_PREFERRED_ENCODER_PROFILE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991425"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="d6dc9-103">\_Атрибут предпочтительного \_ профиля КОДИРОВЩИКа MFT \_</span><span class="sxs-lookup"><span data-stu-id="d6dc9-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="d6dc9-104">Содержит свойства конфигурации кодировщика.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6dc9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6dc9-105">Data type</span></span>

<span data-ttu-id="d6dc9-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Имфаттрибутес \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="d6dc9-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="d6dc9-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="d6dc9-107">Get/set</span></span>

<span data-ttu-id="d6dc9-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="d6dc9-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d6dc9-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="d6dc9-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d6dc9-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="d6dc9-110">Applies to</span></span>

[<span data-ttu-id="d6dc9-111">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="d6dc9-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="d6dc9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6dc9-112">Remarks</span></span>

<span data-ttu-id="d6dc9-113">Этот атрибут может быть задан для объекта активации, возвращаемого функцией [**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="d6dc9-114">Атрибут применяется только в том случае, если объект активации настроен для создания кодировщика.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="d6dc9-115">Значение атрибута является указателем на хранилище атрибутов, которое само содержит свойства, заданные для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="d6dc9-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dc9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d6dc9-117">Requirements</span></span>



| <span data-ttu-id="d6dc9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d6dc9-118">Requirement</span></span> | <span data-ttu-id="d6dc9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d6dc9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dc9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6dc9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dc9-121">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d6dc9-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d6dc9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6dc9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dc9-123">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d6dc9-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d6dc9-124">Header</span><span class="sxs-lookup"><span data-stu-id="d6dc9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6dc9-125"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6dc9-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6dc9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6dc9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dc9-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6dc9-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6dc9-128">**мфкреатетрансформактивате**</span><span class="sxs-lookup"><span data-stu-id="d6dc9-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="d6dc9-129">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="d6dc9-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




