---
description: Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Атрибут MFT_CONNECTED_STREAM_ATTRIBUTE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898730"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="08a99-103">\_ \_ Атрибут атрибута потока, подключенного к MFT \_</span><span class="sxs-lookup"><span data-stu-id="08a99-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="08a99-104">Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).</span><span class="sxs-lookup"><span data-stu-id="08a99-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="08a99-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="08a99-105">Data type</span></span>

<span data-ttu-id="08a99-106">**Имфаттрибутес \** _ хранится как _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="08a99-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="08a99-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="08a99-107">Get/set</span></span>

<span data-ttu-id="08a99-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="08a99-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="08a99-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="08a99-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="08a99-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a99-110">Remarks</span></span>

<span data-ttu-id="08a99-111">Приложения обычно не используют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="08a99-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="08a99-112">Этот атрибут используется для МФТС, которые действуют как прокси-серверы для аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="08a99-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="08a99-113">Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="08a99-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="08a99-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="08a99-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a99-115">Требования</span><span class="sxs-lookup"><span data-stu-id="08a99-115">Requirements</span></span>



| <span data-ttu-id="08a99-116">Требование</span><span class="sxs-lookup"><span data-stu-id="08a99-116">Requirement</span></span> | <span data-ttu-id="08a99-117">Значение</span><span class="sxs-lookup"><span data-stu-id="08a99-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a99-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08a99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08a99-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="08a99-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="08a99-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08a99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08a99-121">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="08a99-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="08a99-122">Header</span><span class="sxs-lookup"><span data-stu-id="08a99-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a99-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a99-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a99-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08a99-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a99-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08a99-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08a99-126">MFT \_ подключено \_ к \_ аппаратному \_ потоку</span><span class="sxs-lookup"><span data-stu-id="08a99-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="08a99-127">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="08a99-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="08a99-128">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="08a99-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




