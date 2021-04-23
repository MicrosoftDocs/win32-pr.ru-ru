---
description: Указывает и настраивает службы, которые должны быть активными в домене службы, который был указан при вызове либо Кокреатеактивити, либо Коентерсервицедомаин.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Класс Ксервицеконфиг (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701177"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="9764e-103">Класс Ксервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="9764e-103">CServiceConfig class</span></span>

<span data-ttu-id="9764e-104">Указывает и настраивает службы, которые должны быть активными в домене службы, который был указан при вызове либо [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , либо [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span><span class="sxs-lookup"><span data-stu-id="9764e-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9764e-105">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="9764e-105">When to implement</span></span>

<span data-ttu-id="9764e-106">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="9764e-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="9764e-107">Требование</span><span class="sxs-lookup"><span data-stu-id="9764e-107">Requirement</span></span> | <span data-ttu-id="9764e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9764e-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9764e-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="9764e-109">CLSID</span></span>      | <span data-ttu-id="9764e-110">\_КСЕРВИЦЕКОНФИГ CLSID</span><span class="sxs-lookup"><span data-stu-id="9764e-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9764e-111">ProgID:</span><span class="sxs-lookup"><span data-stu-id="9764e-111">ProgID</span></span>     | <span data-ttu-id="9764e-112">L "КОМСВКС. Ксервицеконфиг "</span><span class="sxs-lookup"><span data-stu-id="9764e-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9764e-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="9764e-113">Interfaces</span></span> | [<span data-ttu-id="9764e-114">**исервицекомтиинтринсиксконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="9764e-115">**исервицеиисинтринсиксконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="9764e-116">**исервицеинхеританцеконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="9764e-117">**исервицепартитионконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="9764e-118">**исервицескссконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="9764e-119">**исервицесинчронизатионконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="9764e-120">**исервицесреадпулконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="9764e-121">**исервицетраккерконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="9764e-122">**исервицетрансактионконфиг**</span><span class="sxs-lookup"><span data-stu-id="9764e-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="9764e-123">Назначение</span><span class="sxs-lookup"><span data-stu-id="9764e-123">When to use</span></span>

<span data-ttu-id="9764e-124">Этот класс используется для настройки служб, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="9764e-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="9764e-125">[**Кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) и [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) позволяют использовать службы, настроенные этим классом, без необходимости привязывать эти службы к компоненту перед их использованием.</span><span class="sxs-lookup"><span data-stu-id="9764e-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="9764e-126">Этот класс не предназначен для использования в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9764e-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="9764e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9764e-127">Remarks</span></span>

<span data-ttu-id="9764e-128">Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9764e-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="9764e-129">Объекты, создаваемые из класса **ксервицеконфиг** , объединяют Свободный потоковый маршалеру, чтобы их можно было хранить в средах выполнения системы и повторно использовать в разных апартаментах.</span><span class="sxs-lookup"><span data-stu-id="9764e-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="9764e-130">Чтобы настроить отдельную службу, вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса, связанного со службой, а затем вызовите методы для этого интерфейса, чтобы установить соответствующую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9764e-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9764e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9764e-131">Requirements</span></span>



| <span data-ttu-id="9764e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9764e-132">Requirement</span></span> | <span data-ttu-id="9764e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9764e-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9764e-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9764e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9764e-135">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="9764e-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9764e-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9764e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9764e-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9764e-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9764e-138">Header</span><span class="sxs-lookup"><span data-stu-id="9764e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9764e-139"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="9764e-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9764e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9764e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9764e-141">**кокреатеактивити**</span><span class="sxs-lookup"><span data-stu-id="9764e-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="9764e-142">**кокреатефрисреадедмаршалер**</span><span class="sxs-lookup"><span data-stu-id="9764e-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="9764e-143">**коентерсервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="9764e-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="9764e-144">**колеавесервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="9764e-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="9764e-145">Службы COM+ без компонентов</span><span class="sxs-lookup"><span data-stu-id="9764e-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

