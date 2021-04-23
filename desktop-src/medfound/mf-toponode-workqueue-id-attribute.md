---
description: Указывает рабочую очередь для ветви топологии.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Атрибут MF_TOPONODE_WORKQUEUE_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154983"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="6c24f-103">\_ \_ Атрибут ID ТОПОНОДЕ ворккуеуе MF \_</span><span class="sxs-lookup"><span data-stu-id="6c24f-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="6c24f-104">Указывает рабочую очередь для ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="6c24f-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c24f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6c24f-105">Data type</span></span>

<span data-ttu-id="6c24f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6c24f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6c24f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c24f-107">Remarks</span></span>

<span data-ttu-id="6c24f-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="6c24f-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="6c24f-109">Атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6c24f-109">The attribute is optional.</span></span>

<span data-ttu-id="6c24f-110">Значение атрибута является определяемым приложением идентификатором для рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="6c24f-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="6c24f-111">Приложения могут использовать этот атрибут для назначения рабочих очередей ветвей топологии.</span><span class="sxs-lookup"><span data-stu-id="6c24f-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="6c24f-112">Каждый исходный узел в топологии определяет одну ветвь.</span><span class="sxs-lookup"><span data-stu-id="6c24f-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="6c24f-113">Ветвь включает все узлы топологии, которые получают данные из этого узла.</span><span class="sxs-lookup"><span data-stu-id="6c24f-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="6c24f-114">Если этот атрибут задан, вызовите метод [**имфворккуеуесервицес:: бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) для разрешенной топологии.</span><span class="sxs-lookup"><span data-stu-id="6c24f-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="6c24f-115">Несколько ветвей в топологии могут совместно использовать одну и ту же рабочую очередь, а рабочие очереди можно повторно использовать в топологиях.</span><span class="sxs-lookup"><span data-stu-id="6c24f-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="6c24f-116">Значение этого атрибута не совпадает с идентификатором, возвращаемым функцией [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) .</span><span class="sxs-lookup"><span data-stu-id="6c24f-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="6c24f-117">Значение атрибута является определяемым приложением идентификатором и используется для связи ветвей топологии с рабочими очередями.</span><span class="sxs-lookup"><span data-stu-id="6c24f-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="6c24f-118">Когда сеанс мультимедиа выделяет новую рабочую очередь, он сохраняет фактический идентификатор рабочей очереди внутри.</span><span class="sxs-lookup"><span data-stu-id="6c24f-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="6c24f-119">Если этот атрибут задан, приложение также может назначить ветвь для задачи службы планировщика классов мультимедиа, задав атрибут [**\_ \_ \_ \_ класса топоноде ворккуеуе MMCSS**](mf-toponode-workqueue-mmcss-class-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6c24f-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="6c24f-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="6c24f-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c24f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6c24f-121">Requirements</span></span>



| <span data-ttu-id="6c24f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6c24f-122">Requirement</span></span> | <span data-ttu-id="6c24f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6c24f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c24f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c24f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c24f-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c24f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6c24f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c24f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c24f-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c24f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c24f-128">Header</span><span class="sxs-lookup"><span data-stu-id="6c24f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c24f-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c24f-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c24f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c24f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c24f-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6c24f-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c24f-132">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="6c24f-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6c24f-133">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6c24f-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6c24f-134">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="6c24f-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="6c24f-135">**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**</span><span class="sxs-lookup"><span data-stu-id="6c24f-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="6c24f-136">**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**</span><span class="sxs-lookup"><span data-stu-id="6c24f-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="6c24f-137">**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="6c24f-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="6c24f-138">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="6c24f-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c24f-139">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="6c24f-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




