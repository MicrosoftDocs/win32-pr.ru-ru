---
description: Указывает, можно ли изменить типы мультимедиа в этом узле топологии.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: Атрибут MF_TOPONODE_LOCKED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811026"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="d586a-103">\_Атрибут MF топоноде \_ locked</span><span class="sxs-lookup"><span data-stu-id="d586a-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="d586a-104">Указывает, можно ли изменить типы мультимедиа в этом узле топологии.</span><span class="sxs-lookup"><span data-stu-id="d586a-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="d586a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d586a-105">Data type</span></span>

<span data-ttu-id="d586a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d586a-106">**UINT32**</span></span>

<span data-ttu-id="d586a-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="d586a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d586a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d586a-108">Remarks</span></span>

<span data-ttu-id="d586a-109">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="d586a-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="d586a-110">Если значение этого атрибута отлично от нуля, то загрузчик топологии не изменит типы носителей.</span><span class="sxs-lookup"><span data-stu-id="d586a-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="d586a-111">Этот атрибут имеет значение **true** , если узел используется.</span><span class="sxs-lookup"><span data-stu-id="d586a-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="d586a-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d586a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d586a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d586a-113">Requirements</span></span>



| <span data-ttu-id="d586a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d586a-114">Requirement</span></span> | <span data-ttu-id="d586a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d586a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d586a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d586a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d586a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d586a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d586a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d586a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d586a-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d586a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d586a-120">Header</span><span class="sxs-lookup"><span data-stu-id="d586a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d586a-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d586a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d586a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d586a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d586a-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d586a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d586a-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="d586a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d586a-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d586a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d586a-126">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="d586a-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d586a-127">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="d586a-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




