---
description: Содержит код ошибки последней ошибки подключения для данного узла топологии.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Атрибут MF_TOPONODE_ERRORCODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154990"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="293cd-103">\_ \_ Атрибут ошибки MF топоноде</span><span class="sxs-lookup"><span data-stu-id="293cd-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="293cd-104">Содержит код ошибки последней ошибки подключения для данного узла топологии.</span><span class="sxs-lookup"><span data-stu-id="293cd-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="293cd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="293cd-105">Data type</span></span>

<span data-ttu-id="293cd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="293cd-106">**UINT32**</span></span>

<span data-ttu-id="293cd-107">Ттреат как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="293cd-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="293cd-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="293cd-108">Remarks</span></span>

<span data-ttu-id="293cd-109">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="293cd-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="293cd-110">Значением этого атрибута является значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="293cd-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="293cd-111">В сеансе мультимедиа или загрузчике топологии может быть задан атрибут.</span><span class="sxs-lookup"><span data-stu-id="293cd-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="293cd-112">Приложения обычно считывают этот атрибут, но не устанавливают его.</span><span class="sxs-lookup"><span data-stu-id="293cd-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="293cd-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="293cd-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="293cd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="293cd-114">Requirements</span></span>



| <span data-ttu-id="293cd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="293cd-115">Requirement</span></span> | <span data-ttu-id="293cd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="293cd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="293cd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="293cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="293cd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="293cd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="293cd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="293cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="293cd-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="293cd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="293cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="293cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="293cd-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="293cd-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293cd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="293cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293cd-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="293cd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="293cd-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="293cd-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="293cd-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="293cd-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="293cd-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="293cd-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="293cd-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="293cd-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




