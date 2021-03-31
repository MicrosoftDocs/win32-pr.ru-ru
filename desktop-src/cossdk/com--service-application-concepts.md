---
description: Основные понятия приложения службы COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Основные понятия приложения службы COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496053"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="210d0-103">Основные понятия приложения службы COM+</span><span class="sxs-lookup"><span data-stu-id="210d0-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="210d0-104">Средство администрирования служб компонентов можно использовать для настройки серверного приложения COM+ в качестве приложения службы.</span><span class="sxs-lookup"><span data-stu-id="210d0-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="210d0-105">Запуск серверного приложения COM+ в качестве службы обеспечивает следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="210d0-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="210d0-106">Если приложение всегда требуется запускать, службы компонентов могут при необходимости запуститься автоматически, а также можно перезапустить сервер при истечении времени ожидания. Например, если компьютер, на котором запущены компоненты прослушивателя очередей компонентов, перезагружается, прослушиватели очередей компонентов могут запускаться автоматически, если они настроены в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="210d0-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="210d0-107">Если приложению требуется выполнять привилегированные операции, приложение может выполняться от имени учетной записи локальной системы.</span><span class="sxs-lookup"><span data-stu-id="210d0-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="210d0-108">С этим уровнем безопасности могут работать только службы NT.</span><span class="sxs-lookup"><span data-stu-id="210d0-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="210d0-109">Приложение будет совместимо с служба кластеров Windows, которое управляет службами во время отработки отказа системы.</span><span class="sxs-lookup"><span data-stu-id="210d0-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="210d0-110">Если другие службы должны быть помечены как зависимые, службы компонентов предоставляют этот параметр.</span><span class="sxs-lookup"><span data-stu-id="210d0-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="210d0-111">Например, если приложение использует функции, предоставляемые другой службой, то служба, помеченная как зависимая, будет запущена до запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="210d0-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="210d0-112">Автоматический запуск приложения</span><span class="sxs-lookup"><span data-stu-id="210d0-112">Starting an Application Automatically</span></span>

<span data-ttu-id="210d0-113">Когда серверное приложение COM+ запускается автоматически, оно действует как служба и требует от разработчика управления сервером с помощью средства администрирования служб.</span><span class="sxs-lookup"><span data-stu-id="210d0-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="210d0-114">Средство администрирования служб можно открыть, запустив средство администрирования "службы компонентов", а затем выбрав **службы (локальные)**.</span><span class="sxs-lookup"><span data-stu-id="210d0-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="210d0-115">Запуск приложения вручную</span><span class="sxs-lookup"><span data-stu-id="210d0-115">Starting an Application Manually</span></span>

<span data-ttu-id="210d0-116">Когда серверное приложение COM+ запускается вручную, оно действует как узел DLL с параметрами безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="210d0-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="210d0-117">Служба будет запускаться вручную при активации и завершении работы автоматически по истечении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="210d0-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="210d0-118">Конфигурации службы</span><span class="sxs-lookup"><span data-stu-id="210d0-118">Service Configurations</span></span>

<span data-ttu-id="210d0-119">Независимо от типа запуска приложение может быть настроено для запуска от имени учетной записи локальной системы или назначено учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="210d0-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="210d0-120">Локальную систему и учетную запись пользователя можно настроить во время создания службы.</span><span class="sxs-lookup"><span data-stu-id="210d0-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="210d0-121">Чтобы настроить параметры безопасности, необходимо использовать средство администрирования служб.</span><span class="sxs-lookup"><span data-stu-id="210d0-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="210d0-122">Для службы также можно задать зависимости.</span><span class="sxs-lookup"><span data-stu-id="210d0-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="210d0-123">Приложение также можно запустить в каком-либо порядке, выбрав зависимости из списка других системных служб.</span><span class="sxs-lookup"><span data-stu-id="210d0-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="210d0-124">Например, системные службы могут быть помечены как зависимые и не запускают приложение, пока системные службы не будут запущены в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="210d0-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="210d0-125">Это позволит правильно инициализировать приложение службы перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="210d0-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="210d0-126">Пошаговые инструкции по настройке приложения COM+ для запуска в качестве службы см. в разделе [Настройка серверного приложения COM+ в качестве приложения службы](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="210d0-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="210d0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="210d0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="210d0-128">Задачи приложения службы COM+</span><span class="sxs-lookup"><span data-stu-id="210d0-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



