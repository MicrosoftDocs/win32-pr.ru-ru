---
description: Задает относительный приоритет потока для ветви топологии.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154982"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="31e18-103">\_ \_ \_ \_ Атрибут приоритета MMCSS топоноде ворккуеуе MF</span><span class="sxs-lookup"><span data-stu-id="31e18-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="31e18-104">Задает относительный приоритет потока для ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="31e18-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="31e18-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="31e18-105">Data type</span></span>

<span data-ttu-id="31e18-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="31e18-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="31e18-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31e18-107">Remarks</span></span>

<span data-ttu-id="31e18-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="31e18-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="31e18-109">Атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="31e18-109">The attribute is optional.</span></span>

<span data-ttu-id="31e18-110">Для этого атрибута требуются атрибуты класса [MF \_ топоноде \_ Ворккуеуе \_ ID](mf-toponode-workqueue-id-attribute.md) и [MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) на одном узле.</span><span class="sxs-lookup"><span data-stu-id="31e18-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="31e18-111">Значение атрибута — это относительный приоритет потока рабочей очереди для этой ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="31e18-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="31e18-112">[Служба диспетчера классов мультимедиа](../procthread/multimedia-class-scheduler-service.md) (MMCSS) использует относительный приоритет, если он задает приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="31e18-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="31e18-113">Дополнительные сведения см. в разделе [**авсетммсреадприорити**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span><span class="sxs-lookup"><span data-stu-id="31e18-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="31e18-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="31e18-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e18-115">Требования</span><span class="sxs-lookup"><span data-stu-id="31e18-115">Requirements</span></span>



| <span data-ttu-id="31e18-116">Требование</span><span class="sxs-lookup"><span data-stu-id="31e18-116">Requirement</span></span> | <span data-ttu-id="31e18-117">Значение</span><span class="sxs-lookup"><span data-stu-id="31e18-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31e18-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31e18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31e18-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="31e18-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31e18-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31e18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31e18-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="31e18-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31e18-122">Header</span><span class="sxs-lookup"><span data-stu-id="31e18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e18-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e18-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e18-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31e18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e18-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31e18-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31e18-126">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="31e18-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="31e18-127">Усовершенствования рабочей очереди и потоков</span><span class="sxs-lookup"><span data-stu-id="31e18-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="31e18-128">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="31e18-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="31e18-129">**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**</span><span class="sxs-lookup"><span data-stu-id="31e18-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="31e18-130">**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**</span><span class="sxs-lookup"><span data-stu-id="31e18-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="31e18-131">**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="31e18-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
