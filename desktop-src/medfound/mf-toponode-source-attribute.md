---
description: Содержит указатель на источник мультимедиа, связанный с узлом топологии.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: Атрибут MF_TOPONODE_SOURCE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543255"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="7b506-103">\_ \_ Исходный атрибут MF топоноде</span><span class="sxs-lookup"><span data-stu-id="7b506-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="7b506-104">Содержит указатель на источник мультимедиа, связанный с узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="7b506-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b506-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7b506-105">Data type</span></span>

<span data-ttu-id="7b506-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="7b506-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="7b506-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b506-107">Remarks</span></span>

<span data-ttu-id="7b506-108">Этот атрибут применяется к исходным узлам (_ \* MF \_ TOPOLOGY \_ саурцестреам \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="7b506-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="7b506-109">Значение атрибута является указателем на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7b506-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="7b506-110">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="7b506-110">This attribute is required.</span></span>

<span data-ttu-id="7b506-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="7b506-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b506-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7b506-112">Requirements</span></span>



| <span data-ttu-id="7b506-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7b506-113">Requirement</span></span> | <span data-ttu-id="7b506-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7b506-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b506-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b506-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7b506-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b506-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7b506-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b506-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7b506-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b506-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7b506-119">Header</span><span class="sxs-lookup"><span data-stu-id="7b506-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b506-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b506-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b506-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b506-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b506-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b506-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b506-123">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="7b506-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="7b506-124">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="7b506-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="7b506-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="7b506-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="7b506-126">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="7b506-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




