---
description: Эти константы используются в двух контекстах.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Константы LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679661"
---
# <a name="lineproxyrequest_-constants"></a><span data-ttu-id="2b046-103">\_Константы линепроксирекуест</span><span class="sxs-lookup"><span data-stu-id="2b046-103">LINEPROXYREQUEST\_ Constants</span></span>

<span data-ttu-id="2b046-104">Эти константы используются в двух контекстах.</span><span class="sxs-lookup"><span data-stu-id="2b046-104">These constants are used in two contexts.</span></span> <span data-ttu-id="2b046-105">Во-первых, их можно использовать в массиве значений **типа DWORD** в структуре [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , передаваемой с помощью [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) \_ , если указан параметр прокси линеопеноптион, чтобы указать, какие функции приложение обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="2b046-105">First, they can be used in an array of **DWORD** values in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) when the LINEOPENOPTION\_PROXY option is specified, to indicate which functions the application is willing to handle.</span></span> <span data-ttu-id="2b046-106">Во-вторых, они используются в [**строке \_ проксирекуест**](line-proxyrequest.md) , передаваемой в приложение обработчика сообщением **Line \_ проксирекуест** , чтобы указать тип обрабатываемого запроса и формат данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="2b046-106">Second, they are used in the [**LINE\_PROXYREQUEST**](line-proxyrequest.md) passed to the handler application by a **LINE\_PROXYREQUEST** message to indicate the type of request that is to be processed and the format of the data in the buffer.</span></span>

<dl> <dt>

<span data-ttu-id="2b046-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ ажентспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="2b046-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST\_AGENTSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-108">Связано с [**линеажентспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span><span class="sxs-lookup"><span data-stu-id="2b046-108">Associated with [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ креатеажент**</span><span class="sxs-lookup"><span data-stu-id="2b046-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST\_CREATEAGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-110">Связано с [**линекреатеажент**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span><span class="sxs-lookup"><span data-stu-id="2b046-110">Associated with [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ креатеажентсессион**</span><span class="sxs-lookup"><span data-stu-id="2b046-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST\_CREATEAGENTSESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-112">Связано с [**линекреатеажентсессион**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span><span class="sxs-lookup"><span data-stu-id="2b046-112">Associated with [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентактивитилист**</span><span class="sxs-lookup"><span data-stu-id="2b046-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST\_GETAGENTACTIVITYLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-114">Связано с [**линежетажентактивитилист**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span><span class="sxs-lookup"><span data-stu-id="2b046-114">Associated with [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетаженткапс**</span><span class="sxs-lookup"><span data-stu-id="2b046-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST\_GETAGENTCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-116">Связано с [**линежетаженткапс**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span><span class="sxs-lookup"><span data-stu-id="2b046-116">Associated with [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентграуплист**</span><span class="sxs-lookup"><span data-stu-id="2b046-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST\_GETAGENTGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-118">Связано с [**линежетажентграуплист**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span><span class="sxs-lookup"><span data-stu-id="2b046-118">Associated with [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентинфо**</span><span class="sxs-lookup"><span data-stu-id="2b046-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST\_GETAGENTINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-120">Связано с [**линежетажентинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span><span class="sxs-lookup"><span data-stu-id="2b046-120">Associated with [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентсессионинфо**</span><span class="sxs-lookup"><span data-stu-id="2b046-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-122">Связано с [**линежетажентсессионинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span><span class="sxs-lookup"><span data-stu-id="2b046-122">Associated with [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентсессионлист**</span><span class="sxs-lookup"><span data-stu-id="2b046-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-124">Связано с [**линежетажентсессионлист**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span><span class="sxs-lookup"><span data-stu-id="2b046-124">Associated with [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентстатус**</span><span class="sxs-lookup"><span data-stu-id="2b046-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST\_GETAGENTSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-126">Связано с [**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span><span class="sxs-lookup"><span data-stu-id="2b046-126">Associated with [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жетграуплист**</span><span class="sxs-lookup"><span data-stu-id="2b046-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST\_GETGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-128">Связано с [**линежетграуплист**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span><span class="sxs-lookup"><span data-stu-id="2b046-128">Associated with [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жеткуеуеинфо**</span><span class="sxs-lookup"><span data-stu-id="2b046-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST\_GETQUEUEINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-130">Связано с [**линежеткуеуеинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span><span class="sxs-lookup"><span data-stu-id="2b046-130">Associated with [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ жеткуеуелист**</span><span class="sxs-lookup"><span data-stu-id="2b046-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST\_GETQUEUELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-132">Связано с [**линежеткуеуелист**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span><span class="sxs-lookup"><span data-stu-id="2b046-132">Associated with [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентактивити**</span><span class="sxs-lookup"><span data-stu-id="2b046-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST\_SETAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-134">Связано с [**линесетажентактивити**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span><span class="sxs-lookup"><span data-stu-id="2b046-134">Associated with [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентграуп**</span><span class="sxs-lookup"><span data-stu-id="2b046-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST\_SETAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-136">Связано с [**линесетажентграуп**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span><span class="sxs-lookup"><span data-stu-id="2b046-136">Associated with [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентмеасурементпериод**</span><span class="sxs-lookup"><span data-stu-id="2b046-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-138">Связано с [**линесетажентмеасурементпериод**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="2b046-138">Associated with [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентсессионстате**</span><span class="sxs-lookup"><span data-stu-id="2b046-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST\_SETAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-140">Связано с [**линесетажентсессионстате**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span><span class="sxs-lookup"><span data-stu-id="2b046-140">Associated with [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентстате**</span><span class="sxs-lookup"><span data-stu-id="2b046-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST\_SETAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-142">Связано с [**линесетажентстате**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span><span class="sxs-lookup"><span data-stu-id="2b046-142">Associated with [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентстатикс**</span><span class="sxs-lookup"><span data-stu-id="2b046-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST\_SETAGENTSTATEEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-144">Связано с [**линесетажентстатикс**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span><span class="sxs-lookup"><span data-stu-id="2b046-144">Associated with [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2b046-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**ЛИНЕПРОКСИРЕКУЕСТ \_ сеткуеуемеасурементпериод**</span><span class="sxs-lookup"><span data-stu-id="2b046-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2b046-146">Связано с [**линесеткуеуемеасурементпериод**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="2b046-146">Associated with [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b046-147">Требования</span><span class="sxs-lookup"><span data-stu-id="2b046-147">Requirements</span></span>



| <span data-ttu-id="2b046-148">Требование</span><span class="sxs-lookup"><span data-stu-id="2b046-148">Requirement</span></span> | <span data-ttu-id="2b046-149">Значение</span><span class="sxs-lookup"><span data-stu-id="2b046-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2b046-150">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2b046-150">TAPI version</span></span><br/> | <span data-ttu-id="2b046-151">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b046-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2b046-152">Header</span><span class="sxs-lookup"><span data-stu-id="2b046-152">Header</span></span><br/>       | <dl> <span data-ttu-id="2b046-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b046-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b046-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b046-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b046-155">Константы центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2b046-155">Call Center Constants</span></span>](call-center-constants.md)
</dt> <dt>

[<span data-ttu-id="2b046-156">Функции центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2b046-156">Call Center Functions</span></span>](call-center-functions.md)
</dt> </dl>

 

 




