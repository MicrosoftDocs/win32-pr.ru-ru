---
description: Указывает время начала для презентаций, помещенных в очередь после первой презентации.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Атрибут MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692544"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="0bb4e-103">\_ \_ Время начала топологии \_ MF \_ для \_ \_ атрибута переключателя представления</span><span class="sxs-lookup"><span data-stu-id="0bb4e-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="0bb4e-104">Указывает время начала для презентаций, помещенных в очередь после первой презентации.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="0bb4e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0bb4e-105">Data type</span></span>

<span data-ttu-id="0bb4e-106">**Int64** хранится как **UINT64**</span><span class="sxs-lookup"><span data-stu-id="0bb4e-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="0bb4e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="0bb4e-107">Get/set</span></span>

<span data-ttu-id="0bb4e-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="0bb4e-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="0bb4e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="0bb4e-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0bb4e-110">Применение</span><span class="sxs-lookup"><span data-stu-id="0bb4e-110">Applies To</span></span>

[<span data-ttu-id="0bb4e-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="0bb4e-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="0bb4e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bb4e-112">Remarks</span></span>

<span data-ttu-id="0bb4e-113">Когда приложение помещает в очередь первый показ в сеансе мультимедиа, приложение задает время начала в параметре *пварстартпоситион* метода [**Имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) .</span><span class="sxs-lookup"><span data-stu-id="0bb4e-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="0bb4e-114">Однако для всех последующих презентаций время запуска определяется \_ \_ атрибутом времени начала топологии MF в \_ \_ \_ \_ топологии.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="0bb4e-115">Время начала указывается в единицах 100-наносекундных относительно начала презентации.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="0bb4e-116">Например, если значение равно 50000000, воспроизведение начнется через 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="0bb4e-117">Если этот атрибут не задан, время начала по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="0bb4e-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="0bb4e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb4e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0bb4e-119">Requirements</span></span>



| <span data-ttu-id="0bb4e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0bb4e-120">Requirement</span></span> | <span data-ttu-id="0bb4e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0bb4e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb4e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bb4e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb4e-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0bb4e-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0bb4e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bb4e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb4e-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0bb4e-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0bb4e-126">Header</span><span class="sxs-lookup"><span data-stu-id="0bb4e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb4e-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb4e-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb4e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bb4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb4e-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0bb4e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0bb4e-130">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="0bb4e-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




