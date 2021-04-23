---
description: Содержит указатель на дескриптор потока для источника мультимедиа.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Атрибут MF_TOPONODE_STREAM_DESCRIPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701699"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="acae1-103">\_ \_ \_ Атрибут дескриптора потока MF топоноде</span><span class="sxs-lookup"><span data-stu-id="acae1-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="acae1-104">Содержит указатель на дескриптор потока для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="acae1-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="acae1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="acae1-105">Data type</span></span>

<span data-ttu-id="acae1-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="acae1-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="acae1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acae1-107">Remarks</span></span>

<span data-ttu-id="acae1-108">Этот атрибут применяется к исходным узлам (_ \* MF \_ TOPOLOGY \_ саурцестреам \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="acae1-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="acae1-109">Значение атрибута является указателем на интерфейс [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) дескриптора потока.</span><span class="sxs-lookup"><span data-stu-id="acae1-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="acae1-110">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="acae1-110">This attribute is required.</span></span>

<span data-ttu-id="acae1-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="acae1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="acae1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="acae1-112">Requirements</span></span>



| <span data-ttu-id="acae1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="acae1-113">Requirement</span></span> | <span data-ttu-id="acae1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="acae1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acae1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acae1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="acae1-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acae1-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="acae1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acae1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="acae1-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="acae1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="acae1-119">Header</span><span class="sxs-lookup"><span data-stu-id="acae1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="acae1-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="acae1-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acae1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acae1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acae1-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acae1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="acae1-123">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="acae1-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="acae1-124">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="acae1-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="acae1-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="acae1-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="acae1-126">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="acae1-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




