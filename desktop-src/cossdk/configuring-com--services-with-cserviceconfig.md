---
description: Настройка служб COM+ с помощью Ксервицеконфиг
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Настройка служб COM+ с помощью Ксервицеконфиг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807187"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="bcfc8-103">Настройка служб COM+ с помощью Ксервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="bcfc8-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="bcfc8-104">Класс [**ксервицеконфиг**](cserviceconfig.md) используется для настройки служб COM+, которые могут использоваться без компонентов.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="bcfc8-105">Он выполняет статистическую обработку свободных потоков, поэтому его можно использовать в разных апартаментах.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="bcfc8-106">Чтобы настроить отдельную службу, необходимо вызвать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса, связанного со службой, а затем вызвать методы для этого интерфейса, чтобы установить соответствующую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="bcfc8-107">В следующей таблице описаны интерфейсы, реализуемые с помощью класса **ксервицеконфиг** .</span><span class="sxs-lookup"><span data-stu-id="bcfc8-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="bcfc8-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="bcfc8-108">Interface</span></span>                                                                         | <span data-ttu-id="bcfc8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bcfc8-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcfc8-110">**исервицеинхеританцеконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="bcfc8-111">Интерфейс по умолчанию для класса.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-111">The default interface for the class.</span></span> <span data-ttu-id="bcfc8-112">Он используется для быстрой инициализации многих служб COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="bcfc8-113">**исервицекомтиинтринсиксконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="bcfc8-114">Используется для настройки сведений о встроенных функциях интегратора транзакций COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="bcfc8-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="bcfc8-115">COMTI позволяет разработчикам интегрировать программы транзакций на основе мэйнфреймов с приложениями на основе компонентов.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="bcfc8-116">**исервицеиисинтринсиксконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="bcfc8-117">Используется для настройки сведений о встроенных параметрах службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="bcfc8-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="bcfc8-118">**исервицепартитионконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="bcfc8-119">Используется для настройки использования разделов COM+ со службами.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="bcfc8-120">**исервицескссконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="bcfc8-121">Используется для настройки параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="bcfc8-122">**исервицесинчронизатионконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="bcfc8-123">Используется для настройки служб синхронизации COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="bcfc8-124">**исервицесреадпулконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="bcfc8-125">Используется для настройки пула потоков для службы COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="bcfc8-126">Пул потоков можно настроить только при использовании функции [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .</span><span class="sxs-lookup"><span data-stu-id="bcfc8-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="bcfc8-127">**исервицетраккерконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="bcfc8-128">Используется для настройки свойства Tracker.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="bcfc8-129">Средство отслеживания — это механизм создания отчетов, используемый кодом мониторинга для отслеживания кода, в котором работает.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="bcfc8-130">**исервицетрансактионконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="bcfc8-131">Используется для настройки службы транзакций COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="bcfc8-132">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="bcfc8-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="bcfc8-133">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="bcfc8-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bcfc8-134">Visual Basic</span></span>

<span data-ttu-id="bcfc8-135">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="bcfc8-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="bcfc8-136">C/C++</span></span>

<span data-ttu-id="bcfc8-137">В следующем фрагменте кода показано, как создать и настроить объект [**ксервицеконфиг**](cserviceconfig.md) для использования транзакций COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="bcfc8-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bcfc8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcfc8-139">**ксервицеконфиг**</span><span class="sxs-lookup"><span data-stu-id="bcfc8-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="bcfc8-140">Использование служб COM+ через Кокреатеактивити</span><span class="sxs-lookup"><span data-stu-id="bcfc8-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="bcfc8-141">Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин</span><span class="sxs-lookup"><span data-stu-id="bcfc8-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

