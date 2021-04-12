---
title: Интерфейсы виртуализации удаленный рабочий стол
description: API виртуализации удаленный рабочий стол поддерживает следующие интерфейсы.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338281"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="54b2e-103">Интерфейсы виртуализации удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="54b2e-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="54b2e-104">API виртуализации удаленный рабочий стол поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="54b2e-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54b2e-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="54b2e-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="54b2e-106">**итссббасенотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-107">Предоставляет методы, которые сообщают о состоянии и сообщениях об ошибках подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="54b2e-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-108">**итссбклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="54b2e-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="54b2e-109">Предоставляет методы и свойства, хранящие сведения о состоянии входящего запроса на подключение от клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="54b2e-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-110">**итссбклиентконнектионпропертисет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="54b2e-111">Может использоваться для определения пользовательских свойств подключения клиента в соответствии с соответствующими настройками.</span><span class="sxs-lookup"><span data-stu-id="54b2e-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-112">**итссбенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="54b2e-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="54b2e-113">Предоставляет методы и свойства, содержащие сведения о среде, в которой размещен конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="54b2e-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="54b2e-114">Этот интерфейс можно использовать для хранения сведений о физическом сервере, на котором размещены виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="54b2e-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-115">**итссбенвиронментпропертисет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="54b2e-116">Может использоваться для определения пользовательских свойств среды, в которой размещаются целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="54b2e-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-117">**итссбфилтерплугинсторе**</span><span class="sxs-lookup"><span data-stu-id="54b2e-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="54b2e-118">Отфильтровать хранилище подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="54b2e-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-119">**итссбженерикнотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-120">Предоставляет методы, которые сообщают о завершении и получают время ожидания от RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-121">**итссбглобалсторе**</span><span class="sxs-lookup"><span data-stu-id="54b2e-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="54b2e-122">Предоставляет методы, которые запрашивают целевые компьютеры, сеансы, среды и фермы, добавленные в хранилище RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-123">**итссблоадбаланцересулт**</span><span class="sxs-lookup"><span data-stu-id="54b2e-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="54b2e-124">Предоставляет методы и свойства, которые хранят целевое имя, возвращаемое алгоритмом балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="54b2e-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-125">**итссблоадбаланЦинг**</span><span class="sxs-lookup"><span data-stu-id="54b2e-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="54b2e-126">Предоставляет методы, которые можно использовать для предоставления пользовательского алгоритма балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="54b2e-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-127">**итссблоадбаланЦингнотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-128">Предоставляет методы, возвращающие результат алгоритма балансировки нагрузки для RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-129">**итссборчестратион**</span><span class="sxs-lookup"><span data-stu-id="54b2e-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="54b2e-130">Предоставляет методы, которые RDCB использует для обеспечения готовности целевого объекта перед тем, как клиент перенаправляется к нему.</span><span class="sxs-lookup"><span data-stu-id="54b2e-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-131">**итссборчестратионнотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-132">Предоставляет методы, возвращающие объект [**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) для RDCB после успешной подготовки целевого объекта к соединению.</span><span class="sxs-lookup"><span data-stu-id="54b2e-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-133">**итссбплацемент**</span><span class="sxs-lookup"><span data-stu-id="54b2e-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="54b2e-134">Предоставляет методы для подготовки среды (компьютера, на котором размещается виртуальная машина).</span><span class="sxs-lookup"><span data-stu-id="54b2e-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-135">**итссбплацементнотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-136">Предоставляет методы, возвращающие сведения о средах для RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-137">**итссбплугин**</span><span class="sxs-lookup"><span data-stu-id="54b2e-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="54b2e-138">Предоставляет методы, которые инициализируют и завершают подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="54b2e-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-139">**итссбплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-140">Предоставляет методы, уведомляющие RDCB о инициализации или завершении работы подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="54b2e-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-141">**итссбплугинпропертисет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="54b2e-142">Может использоваться для определения настраиваемых свойств подключаемого модуля соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="54b2e-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-143">**итссбпропертисет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="54b2e-144">Может использоваться для определения пользовательских свойств соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="54b2e-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-145">**итссбпровидер**</span><span class="sxs-lookup"><span data-stu-id="54b2e-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="54b2e-146">Предоставляет методы, которые создают реализации по умолчанию для объектов, используемых в удаленный рабочий стол виртуализации.</span><span class="sxs-lookup"><span data-stu-id="54b2e-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-147">**итссбпровисионинг**</span><span class="sxs-lookup"><span data-stu-id="54b2e-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="54b2e-148">Предоставляет методы, создающие и обслуживающие виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="54b2e-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-149">**итссбпровисионингплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-150">Предоставляет методы, уведомляющие RDCB о подготовке виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="54b2e-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-151">**итссбресаурценотификатион**</span><span class="sxs-lookup"><span data-stu-id="54b2e-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="54b2e-152">Предоставляет методы, которые RDCB используют для уведомления подключаемых модулей любых изменений состояния, происходящих в объектах сеансов, целевых объектов и подключений клиентов.</span><span class="sxs-lookup"><span data-stu-id="54b2e-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-153">**итссбресаурценотификатионекс**</span><span class="sxs-lookup"><span data-stu-id="54b2e-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="54b2e-154">Предоставляет методы, которые RDCB используют для уведомления подключаемых модулей любых изменений состояния, происходящих в объектах сеансов, целевых объектов и подключений клиентов.</span><span class="sxs-lookup"><span data-stu-id="54b2e-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-155">**итссбресаурцеплугин**</span><span class="sxs-lookup"><span data-stu-id="54b2e-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="54b2e-156">Предоставляет методы, расширяющие возможности RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-157">**итссбресаурцеплугинсторе**</span><span class="sxs-lookup"><span data-stu-id="54b2e-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="54b2e-158">Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="54b2e-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-159">**итссбресаурцеплугинсторикс**</span><span class="sxs-lookup"><span data-stu-id="54b2e-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="54b2e-160">Предоставляет методы, позволяющие подключаемым модулям ресурсов хранить объекты, такие как сеансы и целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="54b2e-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-161">**итссбсервиценотификатион**</span><span class="sxs-lookup"><span data-stu-id="54b2e-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="54b2e-162">Предоставляет методы, которые RDCB используются для уведомления подключаемых модулей об изменениях состояния, происходящих в самом RDCB.</span><span class="sxs-lookup"><span data-stu-id="54b2e-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-163">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="54b2e-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="54b2e-164">Отображает свойства, хранящие сведения о пользовательском сеансе.</span><span class="sxs-lookup"><span data-stu-id="54b2e-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-165">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="54b2e-166">Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="54b2e-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-167">**итссбтаржетекс**</span><span class="sxs-lookup"><span data-stu-id="54b2e-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="54b2e-168">Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="54b2e-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-169">**итссбтаржетпропертисет**</span><span class="sxs-lookup"><span data-stu-id="54b2e-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="54b2e-170">Наследовать от этого интерфейса, чтобы определить набор настраиваемых целевых свойств.</span><span class="sxs-lookup"><span data-stu-id="54b2e-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-171">**итссбтаскинфо**</span><span class="sxs-lookup"><span data-stu-id="54b2e-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="54b2e-172">Отображает свойства, используемые компонентом подключение к удаленному рабочему столу Broker для задания очереди подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="54b2e-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-173">**итссбтаскплугин**</span><span class="sxs-lookup"><span data-stu-id="54b2e-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="54b2e-174">Предоставляет методы, которые обновляют очередь задач для подключаемых модулей подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="54b2e-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-175">**итссбтаскплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="54b2e-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="54b2e-176">Предоставляет методы, которые сообщают о состоянии и сообщениях об ошибках для RDCB задач.</span><span class="sxs-lookup"><span data-stu-id="54b2e-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="54b2e-177">**ивтссбплугин**</span><span class="sxs-lookup"><span data-stu-id="54b2e-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="54b2e-178">Используется для расширения возможностей посредника сеансов служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="54b2e-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="54b2e-179">Реализуйте этот интерфейс, если требуется предоставить подключаемый модуль, переопределяющий логику перенаправления посредника сеансов служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="54b2e-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 