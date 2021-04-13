---
title: Иерархия объектной модели
description: Объекты в объектной модели SDO упорядочиваются в иерархии. Это означает, что объекты в SDO обеспечивают доступ к другим объектам в SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413242"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="9d838-104">Иерархия объектной модели</span><span class="sxs-lookup"><span data-stu-id="9d838-104">Object Model Hierarchy</span></span>

<span data-ttu-id="9d838-105">Объекты в объектной модели SDO упорядочиваются в иерархии.</span><span class="sxs-lookup"><span data-stu-id="9d838-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="9d838-106">Это означает, что объекты в SDO обеспечивают доступ к другим объектам в SDO.</span><span class="sxs-lookup"><span data-stu-id="9d838-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="9d838-107">Объекты предоставляют доступ к другим объектам двумя способами.</span><span class="sxs-lookup"><span data-stu-id="9d838-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="9d838-108">Один из способов заключается в том, чтобы объект предоставлял интерфейс, предоставляющий методы для получения других объектов.</span><span class="sxs-lookup"><span data-stu-id="9d838-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="9d838-109">Примером такого подхода является объект компьютера.</span><span class="sxs-lookup"><span data-stu-id="9d838-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="9d838-110">Объект Machine предоставляет интерфейс [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="9d838-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="9d838-111">Метод [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) извлекает объект службы.</span><span class="sxs-lookup"><span data-stu-id="9d838-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="9d838-112">Метод [**исдомачине:: жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) извлекает объект пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d838-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![объект компьютера, предоставляющий интерфейс исдомачине](images/sdo01.png)

<span data-ttu-id="9d838-114">Дополнительные сведения см. в разделе [Получение службы и пользователя сдос](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="9d838-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="9d838-115">Второй способ, которым объекты предоставляют доступ к другим объектам, заключается в том, что коллекция объектов представляется как свойство объекта, содержащего его.</span><span class="sxs-lookup"><span data-stu-id="9d838-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="9d838-116">Чтобы получить коллекцию объектов, вызовите [**исдо::**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) GetObject свойства объекта, представляющего коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9d838-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="9d838-117">Например, чтобы получить коллекцию политик, вызовите **исдо::** GetObject в интерфейсе [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) , предоставляемом объектом NPS.</span><span class="sxs-lookup"><span data-stu-id="9d838-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="9d838-118">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9d838-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![получение коллекции политик](images/sdo02.png)

<span data-ttu-id="9d838-120">Пример кода, который получает коллекцию Policies, см. в разделе [Получение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection).</span><span class="sxs-lookup"><span data-stu-id="9d838-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="9d838-121">[**Объект данных сервера NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) имеет следующие свойства, представляющие коллекции:</span><span class="sxs-lookup"><span data-stu-id="9d838-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="9d838-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Аудиторов</span><span class="sxs-lookup"><span data-stu-id="9d838-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="9d838-123">Единственным аудитором в коллекции аудиторий является [**журнал событий NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="9d838-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="9d838-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Политике</span><span class="sxs-lookup"><span data-stu-id="9d838-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="9d838-125">Каждый [**объект политики**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) имеет свойство, представляющее коллекцию условий.</span><span class="sxs-lookup"><span data-stu-id="9d838-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Профили</span><span class="sxs-lookup"><span data-stu-id="9d838-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="9d838-127">Каждый [**объект профиля**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) в коллекциях Profiles имеет свойство, представляющее коллекцию атрибутов.</span><span class="sxs-lookup"><span data-stu-id="9d838-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="9d838-128">Список атрибутов, поддерживаемых SDO, см. в разделе [атрибуты, поддерживаемые SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) .</span><span class="sxs-lookup"><span data-stu-id="9d838-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>CHAP</span><span class="sxs-lookup"><span data-stu-id="9d838-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="9d838-130">Коллекция Protocols содержит объект протокола RADIUS, который содержит коллекцию клиентов, представляющую клиенты RADIUS.</span><span class="sxs-lookup"><span data-stu-id="9d838-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="9d838-131">См. раздел [Добавление клиента](/windows/desktop/Nps/sdo-adding-a-client) для примера кода, в котором показано, как получить коллекцию клиентов.</span><span class="sxs-lookup"><span data-stu-id="9d838-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Политики прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="9d838-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="9d838-133">Эта коллекция содержит политики сетевого доступа, используемые для обработки запросов на подключение.</span><span class="sxs-lookup"><span data-stu-id="9d838-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Профили прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="9d838-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="9d838-135">Эта коллекция содержит профили, используемые для обработки запросов на соединение.</span><span class="sxs-lookup"><span data-stu-id="9d838-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Группы серверов RADIUS</span><span class="sxs-lookup"><span data-stu-id="9d838-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="9d838-137">Каждая [**Группа серверов RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) в коллекции "группы серверов RADIUS" имеет свойство, представляющее коллекцию серверов в этой группе серверов.</span><span class="sxs-lookup"><span data-stu-id="9d838-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="9d838-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Обработчики запросов</span><span class="sxs-lookup"><span data-stu-id="9d838-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="9d838-139">Эта коллекция содержит коллекцию "оценщик сфер Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="9d838-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="9d838-140">В этой коллекции также доступны параметры "Проверка подлинности Microsoft NT SAM" и "учет Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="9d838-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9d838-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9d838-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d838-142">Объекты и свойства SDO</span><span class="sxs-lookup"><span data-stu-id="9d838-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="9d838-143">Поддерживаемые в SDO атрибуты</span><span class="sxs-lookup"><span data-stu-id="9d838-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 