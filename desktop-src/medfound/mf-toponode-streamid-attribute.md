---
description: Идентификатор потока приемника потока, связанного с этим узлом топологии.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Атрибут MF_TOPONODE_STREAMID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711283"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="4826b-103">\_Атрибут MF топоноде \_ STREAMID</span><span class="sxs-lookup"><span data-stu-id="4826b-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="4826b-104">Идентификатор потока приемника потока, связанного с этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="4826b-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="4826b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4826b-105">Data type</span></span>

<span data-ttu-id="4826b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4826b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4826b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4826b-107">Remarks</span></span>

<span data-ttu-id="4826b-108">Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="4826b-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="4826b-109">Когда сеанс мультимедиа загружает топологию, он запрашивает приемник потока, используя указанный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4826b-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="4826b-110">В случае сбоя он пытается добавить новый приемник потока в приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4826b-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="4826b-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4826b-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4826b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4826b-112">Requirements</span></span>



| <span data-ttu-id="4826b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4826b-113">Requirement</span></span> | <span data-ttu-id="4826b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4826b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4826b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4826b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4826b-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4826b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4826b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4826b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4826b-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4826b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4826b-119">Header</span><span class="sxs-lookup"><span data-stu-id="4826b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4826b-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4826b-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4826b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4826b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4826b-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4826b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4826b-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="4826b-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4826b-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4826b-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4826b-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="4826b-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4826b-126">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="4826b-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




