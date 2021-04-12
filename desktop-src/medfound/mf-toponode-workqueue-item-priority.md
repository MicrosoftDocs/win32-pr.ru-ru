---
description: Указывает приоритет рабочего элемента для ветви топологии.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Атрибут MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263361"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="fe4a7-103">\_ \_ \_ Атрибут приоритета элемента MF топоноде ворккуеуе \_</span><span class="sxs-lookup"><span data-stu-id="fe4a7-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="fe4a7-104">Указывает приоритет рабочего элемента для ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="fe4a7-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe4a7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fe4a7-105">Data type</span></span>

<span data-ttu-id="fe4a7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fe4a7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fe4a7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe4a7-107">Remarks</span></span>

<span data-ttu-id="fe4a7-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="fe4a7-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="fe4a7-109">Атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fe4a7-109">The attribute is optional.</span></span>

<span data-ttu-id="fe4a7-110">Для этого атрибута требуется [атрибут \_ \_ \_ ID MF топоноде ворккуеуе](mf-toponode-workqueue-id-attribute.md) на том же узле.</span><span class="sxs-lookup"><span data-stu-id="fe4a7-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="fe4a7-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="fe4a7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4a7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fe4a7-112">Requirements</span></span>



| <span data-ttu-id="fe4a7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fe4a7-113">Requirement</span></span> | <span data-ttu-id="fe4a7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fe4a7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4a7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe4a7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4a7-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe4a7-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe4a7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe4a7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4a7-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe4a7-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe4a7-119">Header</span><span class="sxs-lookup"><span data-stu-id="fe4a7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe4a7-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe4a7-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4a7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe4a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4a7-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe4a7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe4a7-123">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="fe4a7-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe4a7-124">Усовершенствования рабочей очереди и потоков</span><span class="sxs-lookup"><span data-stu-id="fe4a7-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="fe4a7-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="fe4a7-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="fe4a7-126">**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**</span><span class="sxs-lookup"><span data-stu-id="fe4a7-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="fe4a7-127">**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**</span><span class="sxs-lookup"><span data-stu-id="fe4a7-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




