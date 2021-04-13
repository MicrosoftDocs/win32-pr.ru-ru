---
description: Указывает, является ли образец носителя первым примером после разрыва в потоке.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: Атрибут MFSampleExtension_Discontinuity (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543951"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="9e7bf-103">\_Атрибут прекращения мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="9e7bf-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="9e7bf-104">Указывает, является ли образец носителя первым примером после разрыва в потоке.</span><span class="sxs-lookup"><span data-stu-id="9e7bf-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e7bf-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e7bf-105">Data type</span></span>

<span data-ttu-id="9e7bf-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="9e7bf-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9e7bf-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="9e7bf-107">Get/set</span></span>

<span data-ttu-id="9e7bf-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9e7bf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9e7bf-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9e7bf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e7bf-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="9e7bf-110">Applies to</span></span>

[<span data-ttu-id="9e7bf-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="9e7bf-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="9e7bf-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e7bf-112">Remarks</span></span>

<span data-ttu-id="9e7bf-113">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9e7bf-113">This attribute applies to media samples.</span></span> <span data-ttu-id="9e7bf-114">Если этот атрибут имеет **значение true**, это означает, что в потоке произошло прекращение, и этот пример является первым, который должен появиться после разрыва.</span><span class="sxs-lookup"><span data-stu-id="9e7bf-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="9e7bf-115">Если этот атрибут не задан, по умолчанию используется значение **false**.</span><span class="sxs-lookup"><span data-stu-id="9e7bf-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="9e7bf-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9e7bf-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7bf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9e7bf-117">Requirements</span></span>



| <span data-ttu-id="9e7bf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9e7bf-118">Requirement</span></span> | <span data-ttu-id="9e7bf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9e7bf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7bf-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e7bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7bf-121">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="9e7bf-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9e7bf-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e7bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7bf-123">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="9e7bf-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9e7bf-124">Header</span><span class="sxs-lookup"><span data-stu-id="9e7bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7bf-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7bf-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7bf-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e7bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7bf-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e7bf-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e7bf-128">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="9e7bf-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e7bf-129">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="9e7bf-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




