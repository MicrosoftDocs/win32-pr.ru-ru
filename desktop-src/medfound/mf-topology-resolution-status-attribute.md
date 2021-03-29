---
description: Указывает состояние попытки разрешения топологии.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Атрибут MF_TOPOLOGY_RESOLUTION_STATUS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898346"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="a0744-103">\_ \_ Атрибут состояния разрешения топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="a0744-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="a0744-104">Указывает состояние попытки разрешения топологии.</span><span class="sxs-lookup"><span data-stu-id="a0744-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="a0744-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a0744-105">Data type</span></span>

<span data-ttu-id="a0744-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a0744-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a0744-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0744-107">Remarks</span></span>

<span data-ttu-id="a0744-108">Загрузчик топологии или сеанс мультимедиа может установить этот атрибут в топологии.</span><span class="sxs-lookup"><span data-stu-id="a0744-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="a0744-109">Значение этого атрибута является **побитовым** для флагов перечисления [**\_ \_ \_ \_ флагов состояния разрешения топологии MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .</span><span class="sxs-lookup"><span data-stu-id="a0744-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="a0744-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a0744-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0744-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a0744-111">Requirements</span></span>



| <span data-ttu-id="a0744-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a0744-112">Requirement</span></span> | <span data-ttu-id="a0744-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a0744-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a0744-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0744-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0744-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0744-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a0744-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0744-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0744-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0744-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a0744-118">Header</span><span class="sxs-lookup"><span data-stu-id="a0744-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0744-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0744-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0744-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0744-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0744-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0744-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a0744-122">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="a0744-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a0744-123">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a0744-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a0744-124">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="a0744-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="a0744-125">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="a0744-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




