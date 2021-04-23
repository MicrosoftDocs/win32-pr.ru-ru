---
description: 'Содержит указатель на маркер, предоставленный методу Имфмедиастреам:: Рекуестсампле.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Атрибут MFSampleExtension_Token (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719422"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="6ff80-103">\_Атрибут токена мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="6ff80-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="6ff80-104">Содержит указатель на маркер, предоставленный методу [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="6ff80-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ff80-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ff80-105">Data type</span></span>

<span data-ttu-id="6ff80-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="6ff80-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="6ff80-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="6ff80-107">Get/set</span></span>

<span data-ttu-id="6ff80-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="6ff80-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="6ff80-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="6ff80-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6ff80-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="6ff80-110">Applies to</span></span>

[<span data-ttu-id="6ff80-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="6ff80-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="6ff80-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ff80-112">Remarks</span></span>

<span data-ttu-id="6ff80-113">Этот атрибут применяется к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6ff80-113">This attribute applies to media samples.</span></span> <span data-ttu-id="6ff80-114">Значением атрибута является указатель **IUnknown** , который передается в параметр *птокен* метода [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="6ff80-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="6ff80-115">Вызывающий объект использует этот атрибут для наблюдения за состоянием запроса.</span><span class="sxs-lookup"><span data-stu-id="6ff80-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="6ff80-116">При написании пользовательского источника мультимедиа установите этот атрибут в образце, когда поток мультимедиа доставляет пример в ответ на метод [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , если значение *Птокен* не равно **null**.</span><span class="sxs-lookup"><span data-stu-id="6ff80-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="6ff80-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="6ff80-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff80-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6ff80-118">Requirements</span></span>



| <span data-ttu-id="6ff80-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6ff80-119">Requirement</span></span> | <span data-ttu-id="6ff80-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6ff80-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff80-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ff80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff80-122">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6ff80-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6ff80-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ff80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff80-124">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6ff80-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6ff80-125">Header</span><span class="sxs-lookup"><span data-stu-id="6ff80-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff80-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff80-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff80-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ff80-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff80-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ff80-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ff80-129">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="6ff80-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ff80-130">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="6ff80-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




