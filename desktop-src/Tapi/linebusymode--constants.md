---
description: '\_Константы побитового флага линебусимоде описывают различные занятые сигналы, которые могут быть созданы коммутатором или сетью. Эти сигналы занятости обычно указывают на то, что в настоящее время используется другой ресурс, необходимый для выполнения вызова.'
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Константы LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679906"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="e00c9-104">\_Константы линебусимоде</span><span class="sxs-lookup"><span data-stu-id="e00c9-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="e00c9-105">Константы побитового флага **линебусимоде \_** описывают различные занятые сигналы, которые могут быть созданы коммутатором или сетью.</span><span class="sxs-lookup"><span data-stu-id="e00c9-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="e00c9-106">Эти сигналы занятости обычно указывают на то, что в настоящее время используется другой ресурс, необходимый для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="e00c9-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="e00c9-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**ЛИНЕБУСИМОДЕ \_ станция**</span><span class="sxs-lookup"><span data-stu-id="e00c9-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e00c9-108">Сигнал занятости означает, что станция вызываемой стороны занята.</span><span class="sxs-lookup"><span data-stu-id="e00c9-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="e00c9-109">Обычно это связано с *нормальным* сигналом занятости.</span><span class="sxs-lookup"><span data-stu-id="e00c9-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e00c9-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_магистраль линебусимоде**</span><span class="sxs-lookup"><span data-stu-id="e00c9-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e00c9-111">Сигнал занятости указывает на то, что магистраль или канал занят.</span><span class="sxs-lookup"><span data-stu-id="e00c9-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="e00c9-112">Обычно это сигнал с *быстрым* занятием.</span><span class="sxs-lookup"><span data-stu-id="e00c9-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e00c9-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**ЛИНЕБУСИМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e00c9-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e00c9-114">Конкретный режим занятости сигнала в настоящее время неизвестен, но может быть известен позже.</span><span class="sxs-lookup"><span data-stu-id="e00c9-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e00c9-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**ЛИНЕБУСИМОДЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="e00c9-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e00c9-116">Специальный режим сигнала "занят" недоступен и не может быть известен.</span><span class="sxs-lookup"><span data-stu-id="e00c9-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e00c9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e00c9-117">Remarks</span></span>

<span data-ttu-id="e00c9-118">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="e00c9-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="e00c9-119">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e00c9-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="e00c9-120">Сигналы занятости могут отправляться в виде неизменяемых тонов или сообщений за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="e00c9-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="e00c9-121">TAPI не делает никаких предположений о конкретном механизме сигнализации.</span><span class="sxs-lookup"><span data-stu-id="e00c9-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e00c9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e00c9-122">Requirements</span></span>



| <span data-ttu-id="e00c9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e00c9-123">Requirement</span></span> | <span data-ttu-id="e00c9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e00c9-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e00c9-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e00c9-125">TAPI version</span></span><br/> | <span data-ttu-id="e00c9-126">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e00c9-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e00c9-127">Header</span><span class="sxs-lookup"><span data-stu-id="e00c9-127">Header</span></span><br/>       | <dl> <span data-ttu-id="e00c9-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00c9-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




