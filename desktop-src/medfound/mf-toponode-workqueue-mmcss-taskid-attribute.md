---
description: Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543239"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="927bb-103">\_Атрибут MF топоноде \_ ворккуеуе \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="927bb-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="927bb-104">Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="927bb-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="927bb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="927bb-105">Data type</span></span>

<span data-ttu-id="927bb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="927bb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="927bb-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="927bb-107">Remarks</span></span>

<span data-ttu-id="927bb-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="927bb-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="927bb-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="927bb-109">This attribute is optional.</span></span>

<span data-ttu-id="927bb-110">Этот атрибут игнорируется, если не заданы также следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="927bb-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="927bb-111">**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**</span><span class="sxs-lookup"><span data-stu-id="927bb-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="927bb-112">**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**</span><span class="sxs-lookup"><span data-stu-id="927bb-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="927bb-113">Если приложение регистрирует один из собственных потоков с помощью MMCSS, можно использовать этот атрибут, чтобы связать рабочую очередь топологии с группой MMCSS приложения.</span><span class="sxs-lookup"><span data-stu-id="927bb-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="927bb-114">Задайте значение атрибута, равное идентификатору задачи, полученному приложением при регистрации в службе MMCSS.</span><span class="sxs-lookup"><span data-stu-id="927bb-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="927bb-115">(Идентификатор задачи возвращается в параметре *таскиндекс* функции [**авсетммсреадчарактеристикс**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) .</span><span class="sxs-lookup"><span data-stu-id="927bb-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="927bb-116">Дополнительные сведения см. в разделе [процесс и функции потока](../procthread/process-and-thread-functions.md).</span><span class="sxs-lookup"><span data-stu-id="927bb-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="927bb-117">Если вы хотите, чтобы служба MMCSS назначила новый идентификатор задачи для топологии, установите [**атрибут \_ \_ \_ \_ класса MMCSS топоноде ворккуеуе (MF**](mf-toponode-workqueue-mmcss-class-attribute.md) ), но не задавайте атрибут **MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID** .</span><span class="sxs-lookup"><span data-stu-id="927bb-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="927bb-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="927bb-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="927bb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="927bb-119">Requirements</span></span>



| <span data-ttu-id="927bb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="927bb-120">Requirement</span></span> | <span data-ttu-id="927bb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="927bb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="927bb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="927bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="927bb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="927bb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="927bb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="927bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="927bb-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="927bb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="927bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="927bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="927bb-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="927bb-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927bb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="927bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927bb-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="927bb-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="927bb-130">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="927bb-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="927bb-131">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="927bb-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="927bb-132">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="927bb-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="927bb-133">**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**</span><span class="sxs-lookup"><span data-stu-id="927bb-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="927bb-134">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="927bb-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="927bb-135">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="927bb-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
