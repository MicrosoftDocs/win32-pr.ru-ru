---
description: Сообщение LINE \_ проксистатус отправляется при изменении доступных прокси-серверов в строке, открытой в данный момент приложением.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Сообщение LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675564"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="f7955-103">Строка \_ сообщения проксистатус</span><span class="sxs-lookup"><span data-stu-id="f7955-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="f7955-104">Сообщение **Line \_ проксистатус** отправляется при изменении доступных прокси-серверов в строке, открытой в данный момент приложением.</span><span class="sxs-lookup"><span data-stu-id="f7955-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="f7955-105">ТАПИСРВ создает это сообщение во время выполнения функции [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) с помощью линепроксистатус \_ Open и Линепроксистатус \_ аллопенфоракд или [**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose) функции, используя Линепроксистатус \_ Close (все [**\_ константы LINEPROXYSTATUS**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="f7955-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f7955-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7955-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7955-107">*двдевице*</span><span class="sxs-lookup"><span data-stu-id="f7955-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f7955-108">Маркер приложения для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="f7955-108">The application's handle to the line device.</span></span> <span data-ttu-id="f7955-109">Это связано с обработчиком агента.</span><span class="sxs-lookup"><span data-stu-id="f7955-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="f7955-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="f7955-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f7955-111">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="f7955-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="f7955-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f7955-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7955-113">Указывает состояние очереди, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="f7955-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="f7955-114">Может быть одной или несколькими [**\_ константами линепроксистатус**](lineproxystatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f7955-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7955-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f7955-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7955-116">Если *dwParam1* имеет значение линепроксистатус \_ Open или Линепроксистатус \_ Close, *dwParam2* указывает на связанный тип запроса прокси-сервера, который является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="f7955-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="f7955-117">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентграуп</span><span class="sxs-lookup"><span data-stu-id="f7955-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="f7955-118">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентстате</span><span class="sxs-lookup"><span data-stu-id="f7955-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="f7955-119">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентактивити</span><span class="sxs-lookup"><span data-stu-id="f7955-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="f7955-120">ЛИНЕПРОКСИРЕКУЕСТ \_ жетаженткапс</span><span class="sxs-lookup"><span data-stu-id="f7955-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="f7955-121">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентстатус</span><span class="sxs-lookup"><span data-stu-id="f7955-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="f7955-122">ЛИНЕПРОКСИРЕКУЕСТ \_ ажентспеЦифик</span><span class="sxs-lookup"><span data-stu-id="f7955-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="f7955-123">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентактивитилист</span><span class="sxs-lookup"><span data-stu-id="f7955-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="f7955-124">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентграуплист</span><span class="sxs-lookup"><span data-stu-id="f7955-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="f7955-125">ЛИНЕПРОКСИРЕКУЕСТ \_ креатеажент</span><span class="sxs-lookup"><span data-stu-id="f7955-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="f7955-126">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентмеасурементпериод</span><span class="sxs-lookup"><span data-stu-id="f7955-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="f7955-127">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентинфо</span><span class="sxs-lookup"><span data-stu-id="f7955-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="f7955-128">ЛИНЕПРОКСИРЕКУЕСТ \_ креатеажентсессион</span><span class="sxs-lookup"><span data-stu-id="f7955-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="f7955-129">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентсессионлист</span><span class="sxs-lookup"><span data-stu-id="f7955-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="f7955-130">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентсессионстате</span><span class="sxs-lookup"><span data-stu-id="f7955-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="f7955-131">ЛИНЕПРОКСИРЕКУЕСТ \_ жетажентсессионинфо</span><span class="sxs-lookup"><span data-stu-id="f7955-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="f7955-132">ЛИНЕПРОКСИРЕКУЕСТ \_ жеткуеуелист</span><span class="sxs-lookup"><span data-stu-id="f7955-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="f7955-133">ЛИНЕПРОКСИРЕКУЕСТ \_ сеткуеуемеасурементпериод</span><span class="sxs-lookup"><span data-stu-id="f7955-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="f7955-134">ЛИНЕПРОКСИРЕКУЕСТ \_ жеткуеуеинфо</span><span class="sxs-lookup"><span data-stu-id="f7955-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="f7955-135">ЛИНЕПРОКСИРЕКУЕСТ \_ жетграуплист</span><span class="sxs-lookup"><span data-stu-id="f7955-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="f7955-136">ЛИНЕПРОКСИРЕКУЕСТ \_ сетажентстатикс</span><span class="sxs-lookup"><span data-stu-id="f7955-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="f7955-137">В противном случае *dwParam2* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="f7955-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f7955-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f7955-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f7955-139">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f7955-139">Reserved.</span></span> <span data-ttu-id="f7955-140">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f7955-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7955-141">Требования</span><span class="sxs-lookup"><span data-stu-id="f7955-141">Requirements</span></span>



| <span data-ttu-id="f7955-142">Требование</span><span class="sxs-lookup"><span data-stu-id="f7955-142">Requirement</span></span> | <span data-ttu-id="f7955-143">Значение</span><span class="sxs-lookup"><span data-stu-id="f7955-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f7955-144">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f7955-144">TAPI version</span></span><br/> | <span data-ttu-id="f7955-145">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="f7955-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="f7955-146">Header</span><span class="sxs-lookup"><span data-stu-id="f7955-146">Header</span></span><br/>       | <dl> <span data-ttu-id="f7955-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7955-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7955-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7955-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7955-149">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="f7955-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="f7955-150">**линеклосе**</span><span class="sxs-lookup"><span data-stu-id="f7955-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="f7955-151">**Строка \_ проксирекуест**</span><span class="sxs-lookup"><span data-stu-id="f7955-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="f7955-152">**\_Константы линепроксирекуест**</span><span class="sxs-lookup"><span data-stu-id="f7955-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 




