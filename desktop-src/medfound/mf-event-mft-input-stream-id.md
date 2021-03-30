---
description: Задает входной поток на Media Foundation преобразовании (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Атрибут MF_EVENT_MFT_INPUT_STREAM_ID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263251"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="10c49-103">\_ \_ \_ Атрибут ID входного \_ потока MFT события MF \_</span><span class="sxs-lookup"><span data-stu-id="10c49-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="10c49-104">Задает входной поток на Media Foundation преобразовании (MFT).</span><span class="sxs-lookup"><span data-stu-id="10c49-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="10c49-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="10c49-105">Data type</span></span>

<span data-ttu-id="10c49-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="10c49-106">**UINT32**</span></span>

<span data-ttu-id="10c49-107">Значение является идентификатором входного потока.</span><span class="sxs-lookup"><span data-stu-id="10c49-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="10c49-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="10c49-108">Get/set</span></span>

<span data-ttu-id="10c49-109">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="10c49-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="10c49-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="10c49-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="10c49-111">Применяется к</span><span class="sxs-lookup"><span data-stu-id="10c49-111">Applies to</span></span>

[<span data-ttu-id="10c49-112">**имфмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="10c49-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="10c49-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10c49-113">Remarks</span></span>

<span data-ttu-id="10c49-114">Этот атрибут используется со следующими событиями:</span><span class="sxs-lookup"><span data-stu-id="10c49-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="10c49-115">метрансформдраинкомплете</span><span class="sxs-lookup"><span data-stu-id="10c49-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="10c49-116">метрансформнидинпут</span><span class="sxs-lookup"><span data-stu-id="10c49-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="10c49-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="10c49-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c49-118">Требования</span><span class="sxs-lookup"><span data-stu-id="10c49-118">Requirements</span></span>



| <span data-ttu-id="10c49-119">Требование</span><span class="sxs-lookup"><span data-stu-id="10c49-119">Requirement</span></span> | <span data-ttu-id="10c49-120">Значение</span><span class="sxs-lookup"><span data-stu-id="10c49-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10c49-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10c49-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10c49-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="10c49-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="10c49-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10c49-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10c49-124">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="10c49-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="10c49-125">Header</span><span class="sxs-lookup"><span data-stu-id="10c49-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10c49-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c49-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c49-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10c49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c49-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10c49-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="10c49-129">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="10c49-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="10c49-130">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="10c49-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




