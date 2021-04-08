---
description: Содержит определяемое вызывающим объектом значение для события Метрансформмаркер.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Атрибут MF_EVENT_MFT_CONTEXT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080486"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="650f0-103">\_ \_ Атрибут контекста MFT события MF \_</span><span class="sxs-lookup"><span data-stu-id="650f0-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="650f0-104">Содержит определяемое вызывающим объектом значение для события [метрансформмаркер](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="650f0-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="650f0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="650f0-105">Data type</span></span>

<span data-ttu-id="650f0-106">**Ulong \_ Запись PTR** , сохраненная как **UINT64**</span><span class="sxs-lookup"><span data-stu-id="650f0-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="650f0-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="650f0-107">Get/set</span></span>

<span data-ttu-id="650f0-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="650f0-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="650f0-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="650f0-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="650f0-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="650f0-110">Applies to</span></span>

[<span data-ttu-id="650f0-111">**имфмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="650f0-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="650f0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="650f0-112">Remarks</span></span>

<span data-ttu-id="650f0-113">Этот атрибут используется с событием [метрансформмаркер](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="650f0-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="650f0-114">Значение атрибута берется из параметра *улпарам* метода [**Имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .</span><span class="sxs-lookup"><span data-stu-id="650f0-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="650f0-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="650f0-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="650f0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="650f0-116">Requirements</span></span>



| <span data-ttu-id="650f0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="650f0-117">Requirement</span></span> | <span data-ttu-id="650f0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="650f0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="650f0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="650f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="650f0-120">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="650f0-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="650f0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="650f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="650f0-122">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="650f0-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="650f0-123">Header</span><span class="sxs-lookup"><span data-stu-id="650f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="650f0-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="650f0-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650f0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="650f0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650f0-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="650f0-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="650f0-127">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="650f0-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="650f0-128">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="650f0-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




