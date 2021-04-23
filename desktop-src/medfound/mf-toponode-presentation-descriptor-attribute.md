---
description: Содержит указатель на дескриптор представления для источника мультимедиа.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Атрибут MF_TOPONODE_PRESENTATION_DESCRIPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811020"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="44e8a-103">\_ \_ \_ Атрибут дескриптора представления MF топоноде</span><span class="sxs-lookup"><span data-stu-id="44e8a-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="44e8a-104">Содержит указатель на дескриптор представления для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="44e8a-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="44e8a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="44e8a-105">Data type</span></span>

<span data-ttu-id="44e8a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="44e8a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="44e8a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44e8a-107">Remarks</span></span>

<span data-ttu-id="44e8a-108">Этот атрибут применяется к исходным узлам (_ \* MF \_ TOPOLOGY \_ саурцестреам \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="44e8a-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="44e8a-109">Значение атрибута является указателем на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="44e8a-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="44e8a-110">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="44e8a-110">This attribute is required.</span></span>

<span data-ttu-id="44e8a-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="44e8a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e8a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="44e8a-112">Requirements</span></span>



| <span data-ttu-id="44e8a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="44e8a-113">Requirement</span></span> | <span data-ttu-id="44e8a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="44e8a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44e8a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44e8a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44e8a-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44e8a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="44e8a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44e8a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44e8a-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44e8a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="44e8a-119">Header</span><span class="sxs-lookup"><span data-stu-id="44e8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e8a-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e8a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e8a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44e8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e8a-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44e8a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44e8a-123">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="44e8a-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="44e8a-124">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="44e8a-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="44e8a-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="44e8a-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="44e8a-126">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44e8a-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




