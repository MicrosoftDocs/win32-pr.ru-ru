---
description: Функция Кокреатеактивити используется для отправки пакетной работы в систему COM+. Это позволяет приложениям, основанным на сценариях, поддерживать конфигурацию службы COM+ на уровне приложения.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Использование служб COM+ через Кокреатеактивити
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701273"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="d9a3d-104">Использование служб COM+ через Кокреатеактивити</span><span class="sxs-lookup"><span data-stu-id="d9a3d-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="d9a3d-105">Функция [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) используется для отправки пакетной работы в систему com+.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="d9a3d-106">Это позволяет приложениям, основанным на сценариях, поддерживать конфигурацию службы COM+ на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="d9a3d-107">Требуемые службы COM+ настраиваются с помощью объекта [**ксервицеконфиг**](cserviceconfig.md) , который передается в функцию.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="d9a3d-108">Функция создает объект действия и возвращает интерфейс [**исервицеактивити**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="d9a3d-109">Пакетная работа может быть отправлена либо синхронно, либо асинхронно с помощью методов [**синчронаускалл**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) или [**асинчронаускалл**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) **исервицеактивити** соответственно.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="d9a3d-110">Указатель на интерфейс [**исервицекалл**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) передается в каждый из этих методов, и пакетная работа реализуется разработчиком в методе [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) интерфейса **исервицекалл** .</span><span class="sxs-lookup"><span data-stu-id="d9a3d-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="d9a3d-111">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="d9a3d-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="d9a3d-112">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d9a3d-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d9a3d-113">Visual Basic</span></span>

<span data-ttu-id="d9a3d-114">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="d9a3d-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="d9a3d-115">C/C++</span></span>

<span data-ttu-id="d9a3d-116">В следующем фрагменте кода показано, как использовать службы COM+ через [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span><span class="sxs-lookup"><span data-stu-id="d9a3d-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="d9a3d-117">Обработка ошибок опущена для краткости.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="d9a3d-118">Этот фрагмент кода использует объект [**ксервицеконфиг**](cserviceconfig.md) , который был создан и настроен в [настройке служб COM+ с помощью ксервицеконфиг](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="d9a3d-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="d9a3d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d9a3d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9a3d-120">**кокреатеактивити**</span><span class="sxs-lookup"><span data-stu-id="d9a3d-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="d9a3d-121">Настройка служб COM+ с помощью Ксервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="d9a3d-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="d9a3d-122">**ксервицеконфиг**</span><span class="sxs-lookup"><span data-stu-id="d9a3d-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="d9a3d-123">Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин</span><span class="sxs-lookup"><span data-stu-id="d9a3d-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



