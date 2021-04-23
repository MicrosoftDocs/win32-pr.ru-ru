---
description: Указывает задачу службы планировщика классов мультимедиа (MMCSS) для ветви топологии.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719392"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="3524c-103">\_ \_ \_ Атрибут класса MMCSS топоноде ворккуеуе MF \_</span><span class="sxs-lookup"><span data-stu-id="3524c-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="3524c-104">Указывает задачу [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md) (MMCSS) для ветви топологии.</span><span class="sxs-lookup"><span data-stu-id="3524c-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="3524c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3524c-105">Data type</span></span>

<span data-ttu-id="3524c-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="3524c-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="3524c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3524c-107">Remarks</span></span>

<span data-ttu-id="3524c-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="3524c-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="3524c-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3524c-109">This attribute is optional.</span></span>

<span data-ttu-id="3524c-110">Для этого атрибута требуется [атрибут \_ \_ \_ ID MF топоноде ворккуеуе](mf-toponode-workqueue-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3524c-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="3524c-111">Если задан этот атрибут, также необходимо установить атрибут **\_ \_ \_ идентификатора MF топоноде ворккуеуе** на том же узле.</span><span class="sxs-lookup"><span data-stu-id="3524c-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="3524c-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3524c-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3524c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3524c-113">Requirements</span></span>



| <span data-ttu-id="3524c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3524c-114">Requirement</span></span> | <span data-ttu-id="3524c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3524c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3524c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3524c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3524c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3524c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3524c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3524c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3524c-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3524c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3524c-120">Header</span><span class="sxs-lookup"><span data-stu-id="3524c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3524c-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3524c-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3524c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3524c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3524c-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3524c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3524c-124">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="3524c-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="3524c-125">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="3524c-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="3524c-126">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="3524c-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3524c-127">**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**</span><span class="sxs-lookup"><span data-stu-id="3524c-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="3524c-128">**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**</span><span class="sxs-lookup"><span data-stu-id="3524c-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="3524c-129">**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="3524c-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="3524c-130">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="3524c-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="3524c-131">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="3524c-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
