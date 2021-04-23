---
title: Управление устройствами
description: Устройства на основе UPnP контролируются предоставляемыми ими службами.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888884"
---
# <a name="controlling-devices"></a><span data-ttu-id="907b8-103">Управление устройствами</span><span class="sxs-lookup"><span data-stu-id="907b8-103">Controlling Devices</span></span>

<span data-ttu-id="907b8-104">Устройства на основе UPnP контролируются предоставляемыми ими службами.</span><span class="sxs-lookup"><span data-stu-id="907b8-104">UPnP-based devices are controlled by the services they expose.</span></span> <span data-ttu-id="907b8-105">Служба UPnP является наименьшей управляемой сущностью в архитектуре UPnP.</span><span class="sxs-lookup"><span data-stu-id="907b8-105">A UPnP service is the smallest controllable entity in the UPnP architecture.</span></span> <span data-ttu-id="907b8-106">Устройства предоставляют одну службу для каждой основной функции, которую они выполняют.</span><span class="sxs-lookup"><span data-stu-id="907b8-106">Devices expose one service for each primary function they perform.</span></span> <span data-ttu-id="907b8-107">Сложные устройства обычно состоят из нескольких простых служб и других устройств.</span><span class="sxs-lookup"><span data-stu-id="907b8-107">Complex devices are typically composed of several simple services and other devices.</span></span>

<span data-ttu-id="907b8-108">Служба состоит из набора переменных состояния и набора действий, которые могут вызываться приложением для работы с этими переменными состояния.</span><span class="sxs-lookup"><span data-stu-id="907b8-108">A service consists of a set of state variables and a set of actions an application can invoke that operate on those state variables.</span></span> <span data-ttu-id="907b8-109">В API контрольной точки с технологией UPnP службы представлены объектами **службы** , которые предоставляют интерфейс [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="907b8-109">In the Control Point API with UPnP technology, services are represented by **Service** objects that expose the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

<span data-ttu-id="907b8-110">Тип службы определяет переменные состояния и действия, поддерживаемые конкретной службой.</span><span class="sxs-lookup"><span data-stu-id="907b8-110">A service type defines the state variables and actions supported by a particular service.</span></span> <span data-ttu-id="907b8-111">Например, тип службы для службы часов определяет действия **setTime** и- **времени** , а также переменную состояния **времени** .</span><span class="sxs-lookup"><span data-stu-id="907b8-111">For example, the service type for a clock service defines **GetTime** and **SetTime** actions, along with a **Time** state variable.</span></span>

<span data-ttu-id="907b8-112">Идентификатор службы отличает несколько распространенных типов служб на одном устройстве.</span><span class="sxs-lookup"><span data-stu-id="907b8-112">A service ID differentiates multiple common service types within a single device.</span></span> <span data-ttu-id="907b8-113">Например, в будильнике может быть две службы часов: один для обычных часов, другой — для оповещения.</span><span class="sxs-lookup"><span data-stu-id="907b8-113">For example, there can be two clock services in an alarm clock, one for the regular clock and the other for the alarm.</span></span> <span data-ttu-id="907b8-114">Необходимо иметь способ различать две службы, имеющие одинаковые типы служб.</span><span class="sxs-lookup"><span data-stu-id="907b8-114">There needs to be a way to differentiate between the two services, which have identical service types.</span></span> <span data-ttu-id="907b8-115">Идентификатор службы предоставляет уникальный способ идентификации экземпляра типа службы.</span><span class="sxs-lookup"><span data-stu-id="907b8-115">The service ID provides a unique way of identifying an instance of a service type.</span></span> <span data-ttu-id="907b8-116">Затем этот идентификатор службы используется для доступа к правильной службе из коллекции [**иупнпсервицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) , так как тип службы не является уникальным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="907b8-116">Then, this service ID is used to access the correct service from the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) collection, because service type is not a unique identifier.</span></span> <span data-ttu-id="907b8-117">Интерфейс [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) также позволяет приложениям регистрировать функцию обратного вызова с помощью объекта службы.</span><span class="sxs-lookup"><span data-stu-id="907b8-117">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface also allows applications to register a callback function with the service object.</span></span> <span data-ttu-id="907b8-118">При изменении значения переменной состояния службы объект службы вызывает зарегистрированный обратный вызов для уведомления приложения об изменении.</span><span class="sxs-lookup"><span data-stu-id="907b8-118">When the value of a service's state variable changes, the service object invokes the registered callback to notify the application of the change.</span></span> <span data-ttu-id="907b8-119">Инфраструктура UPnP также вызывает этот обратный вызов для уведомления приложений, когда экземпляр службы становится недоступным.</span><span class="sxs-lookup"><span data-stu-id="907b8-119">The UPnP framework also invokes this callback to notify applications when a service instance has become unavailable.</span></span> <span data-ttu-id="907b8-120">Служба может стать недоступной по ряду причин, включая временный сбой сети.</span><span class="sxs-lookup"><span data-stu-id="907b8-120">The service can become unavailable for a variety of reasons, including transient network failure.</span></span>

<span data-ttu-id="907b8-121">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="907b8-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="907b8-122">Получение объектов службы</span><span class="sxs-lookup"><span data-stu-id="907b8-122">Obtaining Service Objects</span></span>](obtaining-service-objects.md)
-   [<span data-ttu-id="907b8-123">Регистрация обратного вызова</span><span class="sxs-lookup"><span data-stu-id="907b8-123">Registering a Callback</span></span>](registering-a-callback.md)
-   [<span data-ttu-id="907b8-124">Запрос переменных состояния</span><span class="sxs-lookup"><span data-stu-id="907b8-124">Querying State Variables</span></span>](querying-state-variables.md)
-   [<span data-ttu-id="907b8-125">Вызов действий</span><span class="sxs-lookup"><span data-stu-id="907b8-125">Invoking Actions</span></span>](invoking-actions.md)

 

 




