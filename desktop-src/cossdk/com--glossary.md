---
description: Страница глоссария
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Глоссарий COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496122"
---
# <a name="com-glossary"></a><span data-ttu-id="15fe8-103">Глоссарий COM+</span><span class="sxs-lookup"><span data-stu-id="15fe8-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="15fe8-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**маркер доступа**</span><span class="sxs-lookup"><span data-stu-id="15fe8-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-105">Объект, описывающий контекст безопасности процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="15fe8-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="15fe8-106">Сведения в маркере включают удостоверение и привилегии учетной записи пользователя, связанной с процессом или потоком.</span><span class="sxs-lookup"><span data-stu-id="15fe8-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="15fe8-107">Когда пользователь входит в систему, система проверяет пароль пользователя, сравнивая его со сведениями, хранящимися в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="15fe8-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="15fe8-108">Если пароль прошел проверку подлинности, система создает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="15fe8-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="15fe8-109">Каждый процесс, выполняемый от имени этого пользователя, имеет копию этого маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="15fe8-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Свойства ACID**</span><span class="sxs-lookup"><span data-stu-id="15fe8-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-111">Акронимы, зафиксированные в ходе обработки транзакций для атомарных, последовательных, изолированных и устойчивых.</span><span class="sxs-lookup"><span data-stu-id="15fe8-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="15fe8-112">Эти свойства обеспечивают предсказуемое поведение, подменяя роль транзакций в качестве всех или None, разработанных для обеспечения единообразных и предсказуемых результатов в распределенной среде при возникновении независимых сбоев.</span><span class="sxs-lookup"><span data-stu-id="15fe8-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**продукта**</span><span class="sxs-lookup"><span data-stu-id="15fe8-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-114">Цепочка событий, которая приводит к созданию COM-объекта и возврату допустимого указателя на интерфейс в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="15fe8-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="15fe8-115">В COM+ объект активируется либо в собственном контексте, либо в его создателе (объект, запрашивающий активируемый объект).</span><span class="sxs-lookup"><span data-stu-id="15fe8-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="15fe8-116">Службы COM+ используют подходящую активацию объекта на основе конфигурации объекта.</span><span class="sxs-lookup"><span data-stu-id="15fe8-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="15fe8-117">В процессе активации система определяет контекст, в котором выполняется объект, инициализирует свойства контекста, проверяет разрешения на доступ и устанавливает удостоверение безопасности.</span><span class="sxs-lookup"><span data-stu-id="15fe8-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**безопасность активации**</span><span class="sxs-lookup"><span data-stu-id="15fe8-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-119">Форма защиты безопасности, определяющая, кто может запускать сервер.</span><span class="sxs-lookup"><span data-stu-id="15fe8-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="15fe8-120">Безопасность активации автоматически применяется диспетчером управления службами (SCM) определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="15fe8-121">После получения запроса от клиента для активации объекта SCM проверяет запрос на соответствие сведениям о безопасности активации, хранящимся в реестре.</span><span class="sxs-lookup"><span data-stu-id="15fe8-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="15fe8-122">Безопасность активации также проверяется на наличие активаций для одного компьютера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="15fe8-123">Также называется *безопасностью запуска*.</span><span class="sxs-lookup"><span data-stu-id="15fe8-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**тип активации**</span><span class="sxs-lookup"><span data-stu-id="15fe8-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-125">Категория активации для приложения COM+, показывающего, выполняется ли приложение в пространстве процесса клиента (в зависимости от того, является ли оно приложением библиотеки или сервера, соответственно), а также должно ли приложение запускаться как служба.</span><span class="sxs-lookup"><span data-stu-id="15fe8-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**оборот**</span><span class="sxs-lookup"><span data-stu-id="15fe8-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-127">В COM+ это логический поток, состоящий из одной или нескольких транзакций и содержащий коллекцию компонентов, сгруппированных в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="15fe8-128">Каждый COM-объект принадлежит одному действию.</span><span class="sxs-lookup"><span data-stu-id="15fe8-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="15fe8-129">Связь между объектом и действием нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="15fe8-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**процесс апартаментной модели**</span><span class="sxs-lookup"><span data-stu-id="15fe8-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-131">Процесс с двумя или более однопотоковыми апартаментами и без многопоточных подразделения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**прокси приложения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-133">Набор файлов, содержащих сведения о регистрации, которые позволяют клиенту удаленно обращаться к серверному приложению COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="15fe8-134">При установке на клиентском компьютере файл прокси приложения записывает сведения о серверном приложении на клиентский компьютер. Клиент может получить удаленный доступ к серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="15fe8-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**идентификаци**</span><span class="sxs-lookup"><span data-stu-id="15fe8-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-136">Процесс обеспечения безопасности, определяющий, что вызывающий объект приложения на самом деле — это то, что он говорит — проверка подлинности утверждения удостоверения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="15fe8-137">Для приложений COM+ проверку подлинности можно включить и настроить административно, после чего оно будет прозрачно работать в приложении.</span><span class="sxs-lookup"><span data-stu-id="15fe8-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**проверки**</span><span class="sxs-lookup"><span data-stu-id="15fe8-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-139">Процесс обеспечения безопасности, позволяющий определить, имеет ли вызывающий приложение разрешение на то, что он запрашивает.</span><span class="sxs-lookup"><span data-stu-id="15fe8-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Кэширование диспетчера ресурсов**</span><span class="sxs-lookup"><span data-stu-id="15fe8-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-141">Диспетчер ресурсов, который выступает в качестве внешнего интерфейса для другого диспетчера ресурсов и кэширует информацию локально, уменьшая затраты на доступ к базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="15fe8-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="15fe8-142">В отличие от стандартного диспетчера ресурсов, диспетчер ресурсов кэширования не участвует в восстановлении, так как никогда не сохраняет базовые данные постоянно.</span><span class="sxs-lookup"><span data-stu-id="15fe8-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**безопасность вызовов**</span><span class="sxs-lookup"><span data-stu-id="15fe8-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-144">Форма защиты безопасности, которая помогает управлять доступом к методам объекта сервера после запуска сервера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**класс (COM)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-146">Именованная конкретная реализация одного или нескольких интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="15fe8-147">Класс COM определяется идентификатором CLSID и иногда идентификатором ProgID.</span><span class="sxs-lookup"><span data-stu-id="15fe8-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Маскировка**</span><span class="sxs-lookup"><span data-stu-id="15fe8-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-149">Способность сервера маскировать свое удостоверение при выполнении вызовов от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="15fe8-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="15fe8-150">Если включена маскировка, вызовы, выполняемые сервером, который олицетворяет клиент, могут быть выполнены под удостоверением клиента.</span><span class="sxs-lookup"><span data-stu-id="15fe8-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="15fe8-151">Если маскировка отключена, вызовы сервера будут выполняться по идентификатору сервера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Приложение COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-153">Основная единица администрирования и безопасности служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="15fe8-154">Приложение COM+ — это группа COM-компонентов, которые, как правило, выполняют связанные функции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="15fe8-155">Эти компоненты более подробно состоят из COM-интерфейсов и методов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Группирование приложений COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-157">Компонент служб компонентов, позволяющий однопотоковым процессам масштабироваться и также может помочь в восстановлении после сбоев в отдельных процессах, предоставляя другим работающим процессам возможность обработки активаций.</span><span class="sxs-lookup"><span data-stu-id="15fe8-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Перезапуск приложений COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-159">Компонент служб компонентов, который значительно увеличивает общую стабильность приложений, позволяя корректно завершить процесс, связанный с приложением, и перезапустить его.</span><span class="sxs-lookup"><span data-stu-id="15fe8-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Каталог COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="15fe8-161">Хранилище данных, в котором хранятся данные конфигурации COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="15fe8-162">Для повышения производительности задач администрирования COM+ требуется чтение и запись данных, хранящихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="15fe8-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="15fe8-163">Доступ к каталогу можно получить только с помощью средства администрирования "службы компонентов" или с помощью библиотеки Комадмин.</span><span class="sxs-lookup"><span data-stu-id="15fe8-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**События COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-165">События COM+ сопоставляют и соединяют издатели и подписчики через слабо связанную систему событий.</span><span class="sxs-lookup"><span data-stu-id="15fe8-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="15fe8-166">Издатель делает вызов метода для инициации события, а подписчик получает эти вызовы через систему событий, а не непосредственно от издателя.</span><span class="sxs-lookup"><span data-stu-id="15fe8-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="15fe8-167">Служба событий COM+ обслуживает список заинтересованных подписчиков, которые получают вызовы, и направляет эти вызовы, не требуя знания издателя.</span><span class="sxs-lookup"><span data-stu-id="15fe8-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Приложение библиотеки COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-169">Приложение COM+, которое выполняется в процессе клиента, который его создает.</span><span class="sxs-lookup"><span data-stu-id="15fe8-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="15fe8-170">Библиотечные приложения могут использовать безопасность на основе ролей, но не поддерживают удаленный доступ или компоненты, поставленные в очередь.</span><span class="sxs-lookup"><span data-stu-id="15fe8-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Группирование объектов COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-172">Автоматическая служба, предоставляемая COM+, которая позволяет настроить компонент для хранения активных экземпляров в пуле, готовых к использованию любым клиентом, запрашивающим этот компонент.</span><span class="sxs-lookup"><span data-stu-id="15fe8-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Разделы COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-174">Служба COM+, которая позволяет на одном компьютере создавать отдельные пространства выполнения для приложений.</span><span class="sxs-lookup"><span data-stu-id="15fe8-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Наборы разделов COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-176">Группа разделов COM+, сопоставленных с определенным ИДЕНТИФИКАТОРом пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15fe8-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Компоненты в очереди COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-178">Служба COM+, основанная на службе очередей сообщений Майкрософт, которая предоставляет простой способ асинхронного вызова и выполнения компонентов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="15fe8-179">Обработка сообщений может выполняться без учета доступности или доступности отправителя или получателя.</span><span class="sxs-lookup"><span data-stu-id="15fe8-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Серверное приложение COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-181">Приложение COM+, которое выполняется в собственном процессе.</span><span class="sxs-lookup"><span data-stu-id="15fe8-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="15fe8-182">Серверные приложения могут поддерживать все службы COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**</span><span class="sxs-lookup"><span data-stu-id="15fe8-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-184">Компонент служб компонентов, позволяющий предоставлять приложение COM+ в виде веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="15fe8-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="15fe8-185">COM+ SOAP также позволяет использовать веб-службу XML в качестве компонента COM.</span><span class="sxs-lookup"><span data-stu-id="15fe8-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM-компонент**</span><span class="sxs-lookup"><span data-stu-id="15fe8-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-187">Двоичная единица кода, которая включает код упаковки и регистрации и создает объекты COM.</span><span class="sxs-lookup"><span data-stu-id="15fe8-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="15fe8-188">Все приложения COM+ состоят из одного или нескольких компонентов COM.</span><span class="sxs-lookup"><span data-stu-id="15fe8-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**дерево фиксации**</span><span class="sxs-lookup"><span data-stu-id="15fe8-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-190">В системе распределенных транзакций концептуальное представление транзакции основано на иерархических связях между отдельными диспетчерами транзакций, участвующими в распределенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="15fe8-191">В эту иерархию входят диспетчеры ресурсов, связанные с диспетчерами транзакций.</span><span class="sxs-lookup"><span data-stu-id="15fe8-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM-объект**</span><span class="sxs-lookup"><span data-stu-id="15fe8-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-193">В модели программирования COM — это структура программирования, включающая как данные, так и функциональные возможности, которые определяются и выделяются как единое целое, и для которых предоставляется только общий доступ через интерфейсы структуры программирования.</span><span class="sxs-lookup"><span data-stu-id="15fe8-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="15fe8-194">COM-объект должен поддерживать, как минимум, интерфейс [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , который поддерживает существование объекта, пока он используется, и предоставляет доступ к другим интерфейсам объекта.</span><span class="sxs-lookup"><span data-stu-id="15fe8-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Компенсирующие диспетчер ресурсов (CRM)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-196">Функция COM+, которая позволяет нетранзакционным ресурсам участвовать в двухфазной фиксации транзакции с помощью Microsoft координатор распределенных транзакций (DTC).</span><span class="sxs-lookup"><span data-stu-id="15fe8-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="15fe8-197">Как правило, Крмс не предоставляют возможности изоляции полных диспетчеров ресурсов, но они обеспечивают атомарность и устойчивость транзакций путем записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="15fe8-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Средство администрирования служб компонентов**</span><span class="sxs-lookup"><span data-stu-id="15fe8-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-199">Оснастка пользовательского интерфейса, с помощью которой администраторы и разработчики могут создавать, настраивать и обслуживать приложения COM+, а также администрировать распределенные транзакции и базы данных, резидентные в памяти.</span><span class="sxs-lookup"><span data-stu-id="15fe8-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="15fe8-200">Средство администрирования служб компонентов также можно использовать для просмотра системных событий и управления локальными системными службами на компьютере, на котором установлено средство.</span><span class="sxs-lookup"><span data-stu-id="15fe8-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**Концептуальная модель**</span><span class="sxs-lookup"><span data-stu-id="15fe8-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-202">Первый шаг на этапе разработки приложения COM+, в котором разработчик определяет бизнес-задачи, которые необходимо решить, и решает, какие компоненты и службы требуются.</span><span class="sxs-lookup"><span data-stu-id="15fe8-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**параллелизма**</span><span class="sxs-lookup"><span data-stu-id="15fe8-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-204">Возможность одновременного доступа нескольких транзакций или процессов к одним и тем же данным.</span><span class="sxs-lookup"><span data-stu-id="15fe8-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="15fe8-205">COM+ обычно управляет параллелизмом с помощью синхронизации.</span><span class="sxs-lookup"><span data-stu-id="15fe8-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**настроенный компонент**</span><span class="sxs-lookup"><span data-stu-id="15fe8-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-207">COM-компонент, который был установлен в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="15fe8-208">После установки компонент настраивается в каталоге COM+ для использования доступных служб COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**локального**</span><span class="sxs-lookup"><span data-stu-id="15fe8-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-210">Набор свойств времени выполнения, связанных с одним или несколькими COM-объектами, которые используются для предоставления служб для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="15fe8-211">Каждый COM-объект выполняется в одном контексте от активации к деактивации (всегда в одном подразделении).</span><span class="sxs-lookup"><span data-stu-id="15fe8-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="15fe8-212">Инициализировано при активации объекта, свойства контекста, такие как свойства контекста безопасности, представляют потребности объекта во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**уровень данных**</span><span class="sxs-lookup"><span data-stu-id="15fe8-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-214">В модели трехуровневой архитектуры для бизнес-приложений уровень доступа СУБД, доступ к которому можно получить через средний уровень или уровень бизнес-служб, а иногда через уровень представления или пользовательский уровень служб.</span><span class="sxs-lookup"><span data-stu-id="15fe8-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="15fe8-215">Уровень данных состоит из компонентов доступа к данным (вместо необработанных соединений СУБД), чтобы обеспечить общий доступ к ресурсам и разрешить настройку клиентов без установки библиотек СУБД и драйверов ODBC на каждом клиенте.</span><span class="sxs-lookup"><span data-stu-id="15fe8-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="15fe8-216">Также называется *уровнем служб данных*.</span><span class="sxs-lookup"><span data-stu-id="15fe8-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**блокировку**</span><span class="sxs-lookup"><span data-stu-id="15fe8-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-218">В многопоточных приложениях — проблема потоковой обработки, возникающая, когда каждый член набора потоков ожидает другого члена набора.</span><span class="sxs-lookup"><span data-stu-id="15fe8-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**передачу**</span><span class="sxs-lookup"><span data-stu-id="15fe8-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-220">Форма олицетворения, которая разрешает серверу действовать от имени клиента, предоставляя серверу возможность олицетворять клиентов по сети.</span><span class="sxs-lookup"><span data-stu-id="15fe8-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**Распределенная транзакция**</span><span class="sxs-lookup"><span data-stu-id="15fe8-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-222">Транзакция, включающая несколько диспетчеров ресурсов, которые могут находиться на одном или разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="15fe8-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Координатор распределенных транзакций (DTC)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-224">Системная служба, которая управляет транзакциями и взаимодействиями, связанными с транзакциями, которые распределяются между двумя или более диспетчерами ресурсов в одной или нескольких системах для обеспечения правильности транзакций ACID.</span><span class="sxs-lookup"><span data-stu-id="15fe8-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Динамическая маскировка**</span><span class="sxs-lookup"><span data-stu-id="15fe8-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-226">Форма маскировки, при которой исходное удостоверение клиента обнаруживается как маркер доступа к серверному потоку при каждом вызове метода на подчиненный сервер.</span><span class="sxs-lookup"><span data-stu-id="15fe8-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="15fe8-227">Хотя представленное удостоверение можно определить динамически, накладные расходы, необходимые для этого, могут быть значительно более дорогими.</span><span class="sxs-lookup"><span data-stu-id="15fe8-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="15fe8-228">Для приложений COM+ конфигурация по умолчанию предназначена для динамической маскировки, так как она обеспечивает гибкость, которая обычно требуется в обстоятельствах, требующих использования олицетворения в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="15fe8-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Объект Enumerator**</span><span class="sxs-lookup"><span data-stu-id="15fe8-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-230">Обеспечивает перечисление элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**журнале**</span><span class="sxs-lookup"><span data-stu-id="15fe8-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-232">Действие, распознаваемое объектом, например щелчок мыши или нажатие клавиши, для которого можно написать код для ответа.</span><span class="sxs-lookup"><span data-stu-id="15fe8-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Объект класса событий**</span><span class="sxs-lookup"><span data-stu-id="15fe8-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-234">Настроенный компонент, предоставляющий постоянную запись в системе событий COM+ для описания издателей и интерфейсов обработки, связанных с этими издателями.</span><span class="sxs-lookup"><span data-stu-id="15fe8-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**метод события**</span><span class="sxs-lookup"><span data-stu-id="15fe8-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-236">Метод в интерфейсе COM+, определяющий событие COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="15fe8-237">Методы событий должны иметь уникальные имена и могут содержать только входные параметры.</span><span class="sxs-lookup"><span data-stu-id="15fe8-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="15fe8-238">Возвращаемое значение должно быть значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="15fe8-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**объект события**</span><span class="sxs-lookup"><span data-stu-id="15fe8-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-240">COM-объект, который может сигнализировать одному или нескольким потокам о произошедшем событии.</span><span class="sxs-lookup"><span data-stu-id="15fe8-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="15fe8-241">Любой поток в процессе может создать объект события.</span><span class="sxs-lookup"><span data-stu-id="15fe8-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**об**</span><span class="sxs-lookup"><span data-stu-id="15fe8-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-243">Аномальное условие или ошибка, возникающая во время выполнения программы и требующие выполнения программного обеспечения за пределами обычного потока управления.</span><span class="sxs-lookup"><span data-stu-id="15fe8-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Перемещение**</span><span class="sxs-lookup"><span data-stu-id="15fe8-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-245">В сетевой системе кластера — процесс перемещения перегруженного или неисправного ресурса, такого как сервер, диск или сеть, в компонент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="15fe8-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**процесс с произвольным потоком**</span><span class="sxs-lookup"><span data-stu-id="15fe8-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-247">Процесс с многопоточным апартаментом и без однопотоковых апартаментов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Координатор глобальной фиксации**</span><span class="sxs-lookup"><span data-stu-id="15fe8-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-249">В системе распределенных транзакций на базе Microsoft Windows — это корневой диспетчер транзакций дерева фиксации.</span><span class="sxs-lookup"><span data-stu-id="15fe8-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="15fe8-250">Этот координатор принимает решение либо зафиксировать или прервать заданную транзакцию, либо не имеет сомнений.</span><span class="sxs-lookup"><span data-stu-id="15fe8-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**олицетворения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-252">Способность потока выполняться в контексте безопасности, отличном от процесса, владеющего потоком.</span><span class="sxs-lookup"><span data-stu-id="15fe8-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="15fe8-253">Серверный поток использует маркер доступа, представляющий учетные данные клиента, и при этом он может получить доступ к ресурсам, к которым у клиента есть доступ.</span><span class="sxs-lookup"><span data-stu-id="15fe8-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**уровень олицетворения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-255">Параметр, используемый клиентом для предоставления серверу определенного уровня полномочий для выполнения действий от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="15fe8-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="15fe8-256">В COM+ это можно задать только для серверных приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**перехвата**</span><span class="sxs-lookup"><span data-stu-id="15fe8-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-258">Для объекта, активированного в заданном контексте, процесс обработки вызовов этого объекта из границы контекста.</span><span class="sxs-lookup"><span data-stu-id="15fe8-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="15fe8-259">Вызовы в контексте обрабатываются с помощью прокси-серверов упрощенных интерфейсов, которые будут обрабатывать любые решения, необходимые для корректировки среды выполнения из одной, которая допускает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="15fe8-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="15fe8-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-261">В программировании на основе COM — коллекция связанных открытых функций, предоставляющих доступ к COM-объекту.</span><span class="sxs-lookup"><span data-stu-id="15fe8-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="15fe8-262">Набор интерфейсов объекта COM создает контракт, указывающий, как программы и другие объекты могут взаимодействовать с COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="15fe8-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**прокси-сервер интерфейса**</span><span class="sxs-lookup"><span data-stu-id="15fe8-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-264">Объект, зависящий от интерфейса, который упаковывает (маршалирует) параметры для этого интерфейса при подготовке к удаленному вызову метода и распаковке (распаковка) возвращаемых значений из заглушки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="15fe8-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="15fe8-265">Прокси-сервер выполняется в адресном пространстве отправителя и взаимодействует с соответствующей заглушкой в адресном пространстве получателя.</span><span class="sxs-lookup"><span data-stu-id="15fe8-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**Заглушка интерфейса**</span><span class="sxs-lookup"><span data-stu-id="15fe8-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-267">Объект, зависящий от интерфейса, который разбирает Упакованные параметры, вызывает требуемый метод и упаковывает (маршалирует) возвращаемые значения из вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="15fe8-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="15fe8-268">Заглушка выполняется в адресном пространстве получателя и взаимодействует с соответствующим прокси интерфейса в адресном пространстве отправителя.</span><span class="sxs-lookup"><span data-stu-id="15fe8-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**внутренний объект**</span><span class="sxs-lookup"><span data-stu-id="15fe8-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-270">В иерархии транзакций — любой объект в корневом объекте.</span><span class="sxs-lookup"><span data-stu-id="15fe8-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**JIT-активация**</span><span class="sxs-lookup"><span data-stu-id="15fe8-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-272">Автоматическая служба, предоставляемая COM+, которая позволяет более продуктивно использовать неактивные ресурсы сервера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="15fe8-273">Если для компонента настроена для JIT-активация, службы COM+ могут деактивировать его экземпляр, и при этом клиент продолжает удерживать активную ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="15fe8-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="15fe8-274">В следующий раз, когда клиент вызывает метод для объекта, COM+ будет повторно активировать объект на клиенте по времени.</span><span class="sxs-lookup"><span data-stu-id="15fe8-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**Устаревший компонент**</span><span class="sxs-lookup"><span data-stu-id="15fe8-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-276">Ненастроенный компонент, установленный в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**прослушивателя**</span><span class="sxs-lookup"><span data-stu-id="15fe8-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-278">Элемент архитектуры службы очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="15fe8-279">Прослушиватель — это COM-объект, который открывает очередь сообщений, связанную с ведущим приложением, и ожидает прибытия сообщений.</span><span class="sxs-lookup"><span data-stu-id="15fe8-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="15fe8-280">По мере поступления сообщений прослушиватель отправляет потоки, обрабатывающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**логическая модель**</span><span class="sxs-lookup"><span data-stu-id="15fe8-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-282">Второй шаг в процессе разработки приложения COM+, при котором концептуальная модель разбивается на логические уровни трехуровневой архитектуры, как показано ниже: уровень представления или пользовательские службы. Средний уровень или бизнес-услуги; и уровень данных, или службы данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**слабо связанное событие**</span><span class="sxs-lookup"><span data-stu-id="15fe8-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-284">Событие, отправитель (издатель) и получатель (подписчик) не связаны тесно.</span><span class="sxs-lookup"><span data-stu-id="15fe8-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="15fe8-285">В слабо связанной системе событий, такой как события COM+, сведения о событиях от разных издателей сохраняются в хранилище событий.</span><span class="sxs-lookup"><span data-stu-id="15fe8-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="15fe8-286">Подписчики запрашивают это хранилище и выбирают события, которые они хотят получить.</span><span class="sxs-lookup"><span data-stu-id="15fe8-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="15fe8-287">При выборе сведений о событии из хранилища событий создается подписка.</span><span class="sxs-lookup"><span data-stu-id="15fe8-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="15fe8-288">При возникновении события система событий выполняет поиск в этой базе данных и находит заинтересованных подписчиков, создает новый объект каждого заинтересованного класса и вызывает метод для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="15fe8-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Маршалинг**</span><span class="sxs-lookup"><span data-stu-id="15fe8-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-290">Процесс упаковки и распаковки параметров метода интерфейса через границы потока или процесса, чтобы можно было выполнить удаленный вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="15fe8-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**перемещение сообщений**</span><span class="sxs-lookup"><span data-stu-id="15fe8-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-292">Элемент архитектуры службы очередей компонентов COM+, который перемещает сообщения с ошибками обратно во входную очередь, чтобы их можно было повторить.</span><span class="sxs-lookup"><span data-stu-id="15fe8-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**Мета-событие**</span><span class="sxs-lookup"><span data-stu-id="15fe8-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-294">Тип события, используемого системой событий COM+ для уведомления заинтересованных подписчиков при создании, изменении или удалении объектов класса событий или подписок.</span><span class="sxs-lookup"><span data-stu-id="15fe8-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Method**</span><span class="sxs-lookup"><span data-stu-id="15fe8-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-296">В программировании на основе COM — процесс, выполняемый COM-объектом при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**Средний уровень**</span><span class="sxs-lookup"><span data-stu-id="15fe8-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-298">В модели трехуровневой архитектуры для бизнес-приложений слой, состоящий из бизнес-логики и правил данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="15fe8-299">Компоненты, составляющие средний уровень, можно использовать для применения бизнес-правил, таких как бизнес-алгоритмы, юридические или правительственные нормы, и правила данных, которые предназначены для обеспечения единообразия структур данных в отдельных или нескольких базах данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="15fe8-300">Поскольку эти компоненты среднего уровня не привязаны к конкретному клиенту, они могут использоваться всеми приложениями и могут быть перемещены в разные расположения в качестве времени ответа и других правил.</span><span class="sxs-lookup"><span data-stu-id="15fe8-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="15fe8-301">Также называется уровнем *бизнес-служб* или *бизнес-логикой*.</span><span class="sxs-lookup"><span data-stu-id="15fe8-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**процесс смешанной модели**</span><span class="sxs-lookup"><span data-stu-id="15fe8-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-303">Процесс, который имеет многопоточный апартамент и один или несколько однопотоковых апартаментов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**помощи**</span><span class="sxs-lookup"><span data-stu-id="15fe8-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-305">Имя, уникально идентифицирующее COM-объект.</span><span class="sxs-lookup"><span data-stu-id="15fe8-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="15fe8-306">Точно так же, как путь определяет файл в файловой системе, моникер определяет COM-объект в пространстве имен каталога.</span><span class="sxs-lookup"><span data-stu-id="15fe8-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**MSI файл**</span><span class="sxs-lookup"><span data-stu-id="15fe8-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-308">Файл, созданный средством администрирования служб компонентов при экспорте приложения COM+ или прокси приложения для установки на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="15fe8-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="15fe8-309">MSI-файл может быть установлен на любой клиент под управлением Windows с помощью установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="15fe8-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**модель многопоточного подразделения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-311">Модель подразделений, в которой все потоки в процессе, инициализированные в виде свободных потоков, находятся в одном апартаменте.</span><span class="sxs-lookup"><span data-stu-id="15fe8-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="15fe8-312">Поэтому нет необходимости выполнять маршалирование между потоками.</span><span class="sxs-lookup"><span data-stu-id="15fe8-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="15fe8-313">Потокам не требуется получать и отправлять сообщения, так как COM не использует сообщения окна в этой модели.</span><span class="sxs-lookup"><span data-stu-id="15fe8-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**вложенная транзакция**</span><span class="sxs-lookup"><span data-stu-id="15fe8-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-315">Вторичная транзакция, инициированная из существующей границы первичной или родительской транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="15fe8-316">Первичная транзакция не фиксируется до фиксации всех ее подчиненных или вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="15fe8-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="15fe8-317">COM+ не поддерживает вложенные транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**модель нейтрального подразделения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-319">Потоковая модель, в которой объекты следуют рекомендациям по многопоточным подразделениям, но могут выполняться в потоках любого типа.</span><span class="sxs-lookup"><span data-stu-id="15fe8-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="15fe8-320">Модель с нейтральным апартаментом — это рекомендуемая модель потоков для COM-компонентов и приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**постоянный объект**</span><span class="sxs-lookup"><span data-stu-id="15fe8-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-322">COM-объект, который может сохранить свое внутреннее состояние при появлении запроса клиентом и соответствует стандартам, определяемым моделью COM, с помощью которых клиенты могут запрашивать инициализацию, загрузку и сохранение объектов в хранилище данных (например, неструктурированный файл, структурированное хранилище или память).</span><span class="sxs-lookup"><span data-stu-id="15fe8-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="15fe8-323">Ответственность за управление расположением, в котором хранятся сохраняемые данные объекта, является обязанностью клиента, но не формат данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**интерфейс постоянного объекта**</span><span class="sxs-lookup"><span data-stu-id="15fe8-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-325">COM-интерфейс, реализованный постоянным объектом.</span><span class="sxs-lookup"><span data-stu-id="15fe8-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="15fe8-326">Клиенты используют интерфейсы постоянных объектов, чтобы сообщить этим постоянным объектам о том, когда и где сохранять их состояние.</span><span class="sxs-lookup"><span data-stu-id="15fe8-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**интерфейс уведомления нулевого этапа**</span><span class="sxs-lookup"><span data-stu-id="15fe8-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-328">Интерфейс COM+, позволяющий приложениям обнаруживать, когда транзакция готова для продолжения работы с протоколом двухфазной фиксации, чтобы он мог выполнять необходимые операции уведомления и взаимодействовать с диспетчером транзакций по завершении операций.</span><span class="sxs-lookup"><span data-stu-id="15fe8-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**Физическая модель**</span><span class="sxs-lookup"><span data-stu-id="15fe8-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-330">Третий и последний шаг в процессе разработки приложений COM+, где разработчик определяет, где находятся компоненты физически и как они должны быть написаны.</span><span class="sxs-lookup"><span data-stu-id="15fe8-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**многопользовательские**</span><span class="sxs-lookup"><span data-stu-id="15fe8-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-332">Элемент архитектуры службы компонентов COM+ в очереди, который получает сообщение из очереди, а затем загружает объект сервера и стандартные заглушки интерфейса для распаковки данных и вызова методов сервера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="15fe8-333">Проигрыватель отменяет упаковку контекста безопасности клиента на стороне сервера, а затем вызывает серверный компонент и выполняет те же вызовы метода.</span><span class="sxs-lookup"><span data-stu-id="15fe8-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="15fe8-334">Вызовы методов воспроизводятся проигрывателем до тех пор, пока не завершится клиентский компонент и транзакция, которая записала вызовы метода, фиксируется.</span><span class="sxs-lookup"><span data-stu-id="15fe8-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**уровень представления**</span><span class="sxs-lookup"><span data-stu-id="15fe8-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-336">В модели трехуровневой архитектуры для бизнес-приложений — уровень, который представляет данные пользователю и при необходимости позволяет управлять данными и вводить данные.</span><span class="sxs-lookup"><span data-stu-id="15fe8-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="15fe8-337">Два основных типа пользовательского интерфейса для уровня представления — это традиционные приложения и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="15fe8-338">Также называется *слоем пользовательских служб*.</span><span class="sxs-lookup"><span data-stu-id="15fe8-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**основной маркер доступа**</span><span class="sxs-lookup"><span data-stu-id="15fe8-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-340">Описывает контекст безопасности учетной записи пользователя, связанной с процессом.</span><span class="sxs-lookup"><span data-stu-id="15fe8-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Диспетчер прокси-сервера**</span><span class="sxs-lookup"><span data-stu-id="15fe8-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-342">В стандартной упаковке — компонент, управляющий всеми прокси-интерфейсами для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="15fe8-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**псевдо-Object**</span><span class="sxs-lookup"><span data-stu-id="15fe8-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-344">Тип содержащегося объекта, например выбор пользователя в документе, диапазон ячеек в электронной таблице или диапазон символов в текстовом документе.</span><span class="sxs-lookup"><span data-stu-id="15fe8-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="15fe8-345">Этот тип объекта называется псевдо-объектом, так как он не обрабатывается как отдельный объект, пока пользователь не помечает выделение.</span><span class="sxs-lookup"><span data-stu-id="15fe8-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**издателя**</span><span class="sxs-lookup"><span data-stu-id="15fe8-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-347">Отправитель события.</span><span class="sxs-lookup"><span data-stu-id="15fe8-347">The sender of an event.</span></span> <span data-ttu-id="15fe8-348">В архитектуре событий COM+ издатель выполняет вызов метода для инициации события.</span><span class="sxs-lookup"><span data-stu-id="15fe8-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**Моникер очереди**</span><span class="sxs-lookup"><span data-stu-id="15fe8-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-350">Моникер, используемый для активации компонента в очереди.</span><span class="sxs-lookup"><span data-stu-id="15fe8-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**состояние гонки**</span><span class="sxs-lookup"><span data-stu-id="15fe8-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-352">В многопоточном приложении — условие, возникающее, когда несколько потоков обращаются к элементу данных без координации, что может привести к несогласованным результатам, в зависимости от того, какой поток достиг первого элемента данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="15fe8-353">COM предоставляет некоторые функции, специально разработанные для того, чтобы избежать конкуренции в необработанных серверах.</span><span class="sxs-lookup"><span data-stu-id="15fe8-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**средства записи**</span><span class="sxs-lookup"><span data-stu-id="15fe8-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-355">Элемент архитектуры службы очередей компонентов COM+, который маршалирует контекст безопасности клиента в сообщение и записывает все вызовы метода для объекта.</span><span class="sxs-lookup"><span data-stu-id="15fe8-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="15fe8-356">Средство записи — это предоставляемый системой Диспетчер прокси-серверов, который выбирает интерфейсы из интерфейсов куеуабле в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**распределитель ресурсов**</span><span class="sxs-lookup"><span data-stu-id="15fe8-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-358">В модели программирования COM+ — компонент, который управляет неустойчивым общим состоянием от имени компонентов приложения внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="15fe8-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="15fe8-359">Распределитель ресурсов аналогичен диспетчерам ресурсов, но без гарантии устойчивости.</span><span class="sxs-lookup"><span data-stu-id="15fe8-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Диспетчер ресурсов**</span><span class="sxs-lookup"><span data-stu-id="15fe8-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-361">Служба, которая управляет постоянными или устойчивыми данными в базах данных, устойчивых очередях сообщений или транзакционных файловых системах.</span><span class="sxs-lookup"><span data-stu-id="15fe8-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="15fe8-362">Это диспетчер ресурсов, который знает, как хранить данные и выполнять аварийное восстановление.</span><span class="sxs-lookup"><span data-stu-id="15fe8-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="15fe8-363">Серверные приложения COM+ используют диспетчеры ресурсов для поддержания устойчивого состояния приложения, например записи инвентаризации, ожидающих заказов и дебиторской задолженности.</span><span class="sxs-lookup"><span data-stu-id="15fe8-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="15fe8-364">Диспетчеры ресурсов работают совместно с Microsoft координатор распределенных транзакций (DTC) для обеспечения атомарности и изоляции приложения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**безопасность на основе ролей**</span><span class="sxs-lookup"><span data-stu-id="15fe8-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-366">Служба безопасности COM+, предоставляемая для приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="15fe8-367">Роль представляет категорию пользователей, определенных для приложения COM+, с целью определения разрешений на доступ к ресурсам приложения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="15fe8-368">Роли назначаются разработчиком компонентам, интерфейсам и методам.</span><span class="sxs-lookup"><span data-stu-id="15fe8-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="15fe8-369">Пользователи назначаются администратором для соответствующих ролей, что позволяет пользователю в рамках данной роли получить доступ к любым ресурсам, которым назначена эта роль.</span><span class="sxs-lookup"><span data-stu-id="15fe8-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**корневой объект**</span><span class="sxs-lookup"><span data-stu-id="15fe8-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-371">Первый объект транзакции, называемый корнем транзакции, и всегда помещается в новую транзакционную границу.</span><span class="sxs-lookup"><span data-stu-id="15fe8-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="15fe8-372">В транзакции может быть только один корневой объект.</span><span class="sxs-lookup"><span data-stu-id="15fe8-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="15fe8-373">Все остальные объекты в иерархии транзакций в корневом объекте называются внутренними объектами.</span><span class="sxs-lookup"><span data-stu-id="15fe8-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Диспетчер корневых транзакций**</span><span class="sxs-lookup"><span data-stu-id="15fe8-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-375">Диспетчер транзакций в системе, которая инициирует транзакцию.</span><span class="sxs-lookup"><span data-stu-id="15fe8-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="15fe8-376">Транзакция не завершается до тех пор, пока корневой диспетчер транзакций не определит состояние транзакции (либо зафиксировано, либо прервано).</span><span class="sxs-lookup"><span data-stu-id="15fe8-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**семафор**</span><span class="sxs-lookup"><span data-stu-id="15fe8-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-378">Объект ядра, используемый для арбитража доступа к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="15fe8-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Диспетчер управления службами (SCM)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-380">Процесс Microsoft Windows Server, который управляет всеми службами в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="15fe8-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Диспетчер общих свойств (SPM)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-382">В com+ это распределитель ресурсов, который можно использовать для совместного использования неустойчивого состояния между несколькими объектами в процессе сервера.</span><span class="sxs-lookup"><span data-stu-id="15fe8-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**однопотоковый процесс**</span><span class="sxs-lookup"><span data-stu-id="15fe8-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-384">Процесс, состоящий только из одного однопотокового подразделения, который, в свою очередь, состоит из ровно одного потока.</span><span class="sxs-lookup"><span data-stu-id="15fe8-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="15fe8-385">Все COM-объекты, которые находятся в однопотоковом подразделении, могут принимать вызовы методов только из одного потока, который принадлежит этому подразделению.</span><span class="sxs-lookup"><span data-stu-id="15fe8-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**ОТВЕТ**</span><span class="sxs-lookup"><span data-stu-id="15fe8-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-387">Простой, основанный на XML протокол для обмена структурированной и типизированной информацией в Интернете.</span><span class="sxs-lookup"><span data-stu-id="15fe8-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="15fe8-388">Протокол не содержит ни приложения, ни семантики транспорта, что делает его модульным и расширяемым.</span><span class="sxs-lookup"><span data-stu-id="15fe8-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**регистрация разбиения**</span><span class="sxs-lookup"><span data-stu-id="15fe8-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-390">Для компонентов, которые уже являются существующими COM-компонентами и используются в среде служб COM+, схема регистрации, в которой базовый COM-аспект регистрации хранится в реестре Windows, а новые службы и атрибуты COM+ (например, очереди компонентов) хранятся в базе данных регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="15fe8-391">Каждый атрибут компонента хранится либо в реестре Windows, либо в базе данных регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="15fe8-392">Новые COM-компоненты регистрируются исключительно в базе данных регистрации COM+, что приводит к дублированию в реестре Windows, чтобы существующие средства могли их использовать.</span><span class="sxs-lookup"><span data-stu-id="15fe8-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**с отслеживанием состояния**</span><span class="sxs-lookup"><span data-stu-id="15fe8-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-394">Или относятся к системе или процессу, который отслеживает все сведения о состоянии действия, в котором он участвует.</span><span class="sxs-lookup"><span data-stu-id="15fe8-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**без отслеживания состояния**</span><span class="sxs-lookup"><span data-stu-id="15fe8-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-396">Или относятся к системе или процессу, участвующим в действии, без мониторинга всех сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="15fe8-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**Статическая маскировка**</span><span class="sxs-lookup"><span data-stu-id="15fe8-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-398">Форма маскировки, где исходное удостоверение клиента может быть представлено один раз на подчиненный сервер, устанавливая на прокси-сервере исходное удостоверение клиента.</span><span class="sxs-lookup"><span data-stu-id="15fe8-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="15fe8-399">Это удостоверение клиента представляется как токен серверного потока, который будет использоваться при последующих вызовах метода.</span><span class="sxs-lookup"><span data-stu-id="15fe8-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**абонент**</span><span class="sxs-lookup"><span data-stu-id="15fe8-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-401">Получатель события.</span><span class="sxs-lookup"><span data-stu-id="15fe8-401">The receiver of an event.</span></span> <span data-ttu-id="15fe8-402">В архитектуре событий COM+ подписчик получает вызовы, совершенные издателем.</span><span class="sxs-lookup"><span data-stu-id="15fe8-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**Объект Subscription**</span><span class="sxs-lookup"><span data-stu-id="15fe8-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-404">В системе событий COM+ — объект, созданный подписчиком для запроса и управления доставкой событий.</span><span class="sxs-lookup"><span data-stu-id="15fe8-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**синхронизиру**</span><span class="sxs-lookup"><span data-stu-id="15fe8-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-406">В COM+ — служба, которая передается из компонента в компонент и запрещает более чем одному вызывающему объекту вводить компонент в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="15fe8-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="15fe8-407">Синхронизация определяет, когда именно потоки могут направлять вызовы объекту.</span><span class="sxs-lookup"><span data-stu-id="15fe8-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**трехуровневая модель архитектуры**</span><span class="sxs-lookup"><span data-stu-id="15fe8-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-409">Основная платформа для логической модели проектирования — сегменты компонентов приложения на три уровня служб следующим образом: уровень представления или пользовательские службы. Средний уровень или бизнес-услуги; и уровень данных, или службы данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="15fe8-410">Эти уровни не обязательно соответствуют физическим расположениям на различных компьютерах в сети, а не к логическим уровням приложения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**тесно связанное событие**</span><span class="sxs-lookup"><span data-stu-id="15fe8-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-412">Событие, отправитель (издатель) и получатель (подписчик) тесно связаны.</span><span class="sxs-lookup"><span data-stu-id="15fe8-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="15fe8-413">В тесно связанной системе событий издатель предоставляется с интерфейсом, на котором вызывается метод при возникновении изменения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="15fe8-414">Подписчик знает, какой издатель должен запрашивать уведомления, и предоставляемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="15fe8-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="15fe8-415">Тесно связанная система событий требует, чтобы издатель и подписчик выполнялись постоянно.</span><span class="sxs-lookup"><span data-stu-id="15fe8-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Журнал трассировки**</span><span class="sxs-lookup"><span data-stu-id="15fe8-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-417">Файл журнала, автоматически созданный координатор распределенных транзакцийом Microsoft, который показывает данные, связанные с одной или несколькими распределенными транзакциями.</span><span class="sxs-lookup"><span data-stu-id="15fe8-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="15fe8-418">Примерами данных в журнале трассировки являются идентификатор транзакции, время транзакции и сообщения, указывающие результат транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**операции**</span><span class="sxs-lookup"><span data-stu-id="15fe8-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-420">Единица работы, в которой последовательность связанных операций выполняется в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="15fe8-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="15fe8-421">Транзакция выполняется ровно один раз и является атомарной — либо вся работа выполняется, либо ни одна из них не имеет.</span><span class="sxs-lookup"><span data-stu-id="15fe8-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Протокол IP транзакций (TIP)**</span><span class="sxs-lookup"><span data-stu-id="15fe8-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-423">Протокол Интернета транзакций — это стандартный протокол двухфазной фиксации, который позволяет разнородным диспетчерам транзакций координировать распределенные транзакции, особенно через Интернет.</span><span class="sxs-lookup"><span data-stu-id="15fe8-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="15fe8-424">Протокол двухфазной фиксации TIP прост в реализации и не зависит от протокола связи "приложение — приложение", так что он может использоваться с любым протоколом приложения, но особенно HTTP.</span><span class="sxs-lookup"><span data-stu-id="15fe8-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Диспетчер транзакций**</span><span class="sxs-lookup"><span data-stu-id="15fe8-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-426">Часть Microsoft координатор распределенных транзакций (DTC), которая выполняется на каждом компьютере, участвующем в распределенной транзакции, и управляет действиями, связанными с фиксацией или препрерыванием этой части транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**приложение обработки транзакций**</span><span class="sxs-lookup"><span data-stu-id="15fe8-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-428">Коллекция операций транзакций, автоматизирующих данную бизнес-задачу.</span><span class="sxs-lookup"><span data-stu-id="15fe8-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**система обработки транзакций**</span><span class="sxs-lookup"><span data-stu-id="15fe8-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-430">Полная система, включающая оборудование и программное обеспечение компьютера, на котором размещается приложение обработки транзакций для выполнения повседневных транзакций, необходимых для ведения бизнеса.</span><span class="sxs-lookup"><span data-stu-id="15fe8-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**протокол двухфазной фиксации**</span><span class="sxs-lookup"><span data-stu-id="15fe8-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-432">Протокол, используемый только в распределенных транзакциях, гарантирует согласованность результата транзакции во всех диспетчерах транзакций, участвующих в транзакции.</span><span class="sxs-lookup"><span data-stu-id="15fe8-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="15fe8-433">Протокол работает на двух разных этапах, чтобы в конечном итоге зафиксировать или прервать транзакцию: этап 1 оценивает условие каждого диспетчера ресурсов, а второй этап завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="15fe8-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**ненастроенный компонент**</span><span class="sxs-lookup"><span data-stu-id="15fe8-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-435">COM-компонент, который не был настроен в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="15fe8-436">Ненастроенные компоненты не могут использовать службы COM+.</span><span class="sxs-lookup"><span data-stu-id="15fe8-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**информацией местонахождении**</span><span class="sxs-lookup"><span data-stu-id="15fe8-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-438">Для транзакций DTC — непрозрачная структура данных, представляющая адрес диспетчера транзакций диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15fe8-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Интерфейсы XA**</span><span class="sxs-lookup"><span data-stu-id="15fe8-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-440">Стандартный набор программных интерфейсов, позволяющих разработчикам приложений COM+ получать доступ к XA-совместимым базам данных и создавать диспетчеры ресурсов, которые работают с реляционными базами данных, очередью сообщений, транзакционными файлами и объектно-ориентированными базами данных.</span><span class="sxs-lookup"><span data-stu-id="15fe8-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="15fe8-441">Хотя корпорация Майкрософт не поддерживает протокол XA напрямую, корпорация Майкрософт поддерживает средства перевода между транзакциями OLE и XA.</span><span class="sxs-lookup"><span data-stu-id="15fe8-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="15fe8-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Веб-службы XML**</span><span class="sxs-lookup"><span data-stu-id="15fe8-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="15fe8-443">Блоки логики приложения, предоставляющие данные и службы другим приложениям.</span><span class="sxs-lookup"><span data-stu-id="15fe8-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="15fe8-444">Приложения обращаются к веб-службам XML через стандартные веб-протоколы, такие как SOAP.</span><span class="sxs-lookup"><span data-stu-id="15fe8-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
