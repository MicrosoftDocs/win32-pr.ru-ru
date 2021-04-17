---
title: Глоссарий COM
description: Страница глоссария
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700950"
---
# <a name="com-glossary"></a><span data-ttu-id="634ec-103">Глоссарий COM</span><span class="sxs-lookup"><span data-stu-id="634ec-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="634ec-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**продукта**</span><span class="sxs-lookup"><span data-stu-id="634ec-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-105">Процесс загрузки объекта в памяти, который преобразует его в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="634ec-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**активное состояние**</span><span class="sxs-lookup"><span data-stu-id="634ec-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-107">COM-объект, который находится в состоянии выполнения и имеет видимый пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="634ec-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**абсолютное специальное имя**</span><span class="sxs-lookup"><span data-stu-id="634ec-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-109">Моникер, указывающий абсолютное расположение объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="634ec-110">Абсолютный моникер аналогичен полному пути.</span><span class="sxs-lookup"><span data-stu-id="634ec-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**держатель рекомендаций**</span><span class="sxs-lookup"><span data-stu-id="634ec-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-112">COM-объект, который кэширует, управляет и отправляет уведомления об изменениях в приемники рекомендаций для приложений-контейнеров.</span><span class="sxs-lookup"><span data-stu-id="634ec-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**приемник рекомендаций**</span><span class="sxs-lookup"><span data-stu-id="634ec-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-114">COM-объект, который может получать уведомления об изменениях во внедренном объекте или связанном объекте, так как он реализует интерфейс [**иадвисесинк**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) или [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) .</span><span class="sxs-lookup"><span data-stu-id="634ec-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="634ec-115">Контейнеры, которые должны получать уведомления об изменениях в объектах, реализуют приемник рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="634ec-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="634ec-116">Уведомления создаются на сервере, который использует объект держателя рекомендаций для кэширования уведомлений и управления ими в контейнерах.</span><span class="sxs-lookup"><span data-stu-id="634ec-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**агрегатный объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-118">COM-объект, который состоит из одного или нескольких других COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="634ec-119">Один объект в статистическом выражении указывает на управляющий объект, который управляет тем, какие интерфейсы в агрегате предоставляются и являются частными.</span><span class="sxs-lookup"><span data-stu-id="634ec-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="634ec-120">Этот управляющий объект имеет специальную реализацию [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , называемую управляющим **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="634ec-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="634ec-121">Все объекты в статистическом выражении должны передавать вызовы методам **IUnknown** через управляющий **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="634ec-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**статистической обработки**</span><span class="sxs-lookup"><span data-stu-id="634ec-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-123">Метод компоновки для реализации COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="634ec-124">Он позволяет создать новый объект, повторно используя одну или несколько существующих реализаций интерфейса объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="634ec-125">Объект Aggregate выбирает, какие интерфейсы предоставлять клиентам, а интерфейсы предоставляются так, как если бы они были реализованы с помощью статистического объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="634ec-126">Клиенты статистического объекта обмениваются данными только с объектом Aggregate.</span><span class="sxs-lookup"><span data-stu-id="634ec-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**внешнее свойство**</span><span class="sxs-lookup"><span data-stu-id="634ec-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-128">Свойство времени выполнения, управляемое и предоставляемое контейнером.</span><span class="sxs-lookup"><span data-stu-id="634ec-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="634ec-129">Как правило, внешнее свойство представляет собой характеристику формы, например цвет фона, которую необходимо передать в элемент управления, чтобы элемент управления мог полагаться на внешний вид окружающей среды.</span><span class="sxs-lookup"><span data-stu-id="634ec-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**Защита моникера**</span><span class="sxs-lookup"><span data-stu-id="634ec-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-131">Обратная запись моникера файла, элемента или указателя.</span><span class="sxs-lookup"><span data-stu-id="634ec-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="634ec-132">Защита моникера добавляется в конец файла, элемента или моникера указателя, чтобы аннулируются его.</span><span class="sxs-lookup"><span data-stu-id="634ec-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="634ec-133">Защита от моникеров используется в создании относительных моникеров.</span><span class="sxs-lookup"><span data-stu-id="634ec-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**искусственный подсчет ссылок**</span><span class="sxs-lookup"><span data-stu-id="634ec-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-135">Метод, используемый для защиты объекта перед вызовом функции или метода, который может преждевременно уничтожить его.</span><span class="sxs-lookup"><span data-stu-id="634ec-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="634ec-136">Программа вызывает метод **IUnknown:: AddRef** для увеличения счетчика ссылок объекта перед вызовом, который может освободить объект.</span><span class="sxs-lookup"><span data-stu-id="634ec-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="634ec-137">После возврата функции программа вызывает метод **IUnknown:: Release** , чтобы уменьшить число.</span><span class="sxs-lookup"><span data-stu-id="634ec-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**Асинхронная привязка**</span><span class="sxs-lookup"><span data-stu-id="634ec-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-139">Тип привязки, в котором процесс должен выполняться асинхронно, чтобы избежать снижения производительности для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="634ec-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="634ec-140">Как правило, асинхронная привязка используется в распределенных средах, например в Интернете.</span><span class="sxs-lookup"><span data-stu-id="634ec-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="634ec-141">OLE поддерживает асинхронные классы моникера и механизмы обратного вызова, позволяющие выполнять поиск и инициализацию объекта в распределенной среде, пока выполняются другие операции.</span><span class="sxs-lookup"><span data-stu-id="634ec-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**асинхронный вызов**</span><span class="sxs-lookup"><span data-stu-id="634ec-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-143">Вызов функции, которая выполняется отдельно, чтобы вызывающий объект мог продолжить обработку инструкций, не дожидаясь возвращения функции.</span><span class="sxs-lookup"><span data-stu-id="634ec-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**Асинхронное моникер**</span><span class="sxs-lookup"><span data-stu-id="634ec-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-145">Моникер, поддерживающий асинхронную привязку.</span><span class="sxs-lookup"><span data-stu-id="634ec-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="634ec-146">Например, экземпляры класса моникера URL-адреса, предоставляемого системой, являются асинхронными моникерами.</span><span class="sxs-lookup"><span data-stu-id="634ec-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**средствами**</span><span class="sxs-lookup"><span data-stu-id="634ec-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-148">Способ управления объектами приложения извне приложения.</span><span class="sxs-lookup"><span data-stu-id="634ec-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="634ec-149">Автоматизация обычно используется для создания приложений, предоставляющих объекты для программных средств и языков макросов, создания объектов одного приложения из других приложений и управления ими, а также для создания средств для доступа к объектам и управления ими.</span><span class="sxs-lookup"><span data-stu-id="634ec-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**контекст привязки**</span><span class="sxs-lookup"><span data-stu-id="634ec-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-151">COM-объект, реализующий интерфейс [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="634ec-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="634ec-152">Контексты привязки используются в операциях моникера для хранения ссылок на объекты, активируемые при связывании моникера.</span><span class="sxs-lookup"><span data-stu-id="634ec-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="634ec-153">Контекст привязки содержит параметры, которые применяются ко всем операциям во время привязки универсального составного моникера и предоставляют реализацию моникера с доступом к сведениям о своей среде.</span><span class="sxs-lookup"><span data-stu-id="634ec-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**вязывания**</span><span class="sxs-lookup"><span data-stu-id="634ec-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-155">Связывание имени с его референт.</span><span class="sxs-lookup"><span data-stu-id="634ec-155">Associating a name with its referent.</span></span> <span data-ttu-id="634ec-156">В частности, Поиск объекта с именем с помощью моникера, перевод его в состояние выполнения, если он еще не существует, и возвращение к нему указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="634ec-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="634ec-157">Объекты могут быть привязаны во время выполнения (также называемое поздним связыванием или динамической привязкой) или во время компиляции (также называемое статической привязкой).</span><span class="sxs-lookup"><span data-stu-id="634ec-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**Мбайта**</span><span class="sxs-lookup"><span data-stu-id="634ec-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-159">(Обычно это временное) локальное хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="634ec-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="634ec-160">В OLE кэш содержит сведения, определяющие представление связанного или внедренного объекта при открытии контейнера.</span><span class="sxs-lookup"><span data-stu-id="634ec-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**Инициализация кэша**</span><span class="sxs-lookup"><span data-stu-id="634ec-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-162">Заполнение кэша связанного или внедренного объекта данными представления.</span><span class="sxs-lookup"><span data-stu-id="634ec-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="634ec-163">Интерфейс [**иолекаче**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) предоставляет методы, которые контейнер может вызывать для управления данными, которые кэшируются для связанных или внедренных объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**см**</span><span class="sxs-lookup"><span data-stu-id="634ec-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-165">Определение объекта в коде.</span><span class="sxs-lookup"><span data-stu-id="634ec-165">The definition of an object in code.</span></span> <span data-ttu-id="634ec-166">В C++ класс объекта определяется как тип данных, но в других языках это не так.</span><span class="sxs-lookup"><span data-stu-id="634ec-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="634ec-167">Поскольку кодировку OLE можно закодировать на любом языке, класс используется для ссылки на общее определение объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**фабрика класса**</span><span class="sxs-lookup"><span data-stu-id="634ec-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-169">COM-объект, реализующий интерфейс [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) и создающий один или несколько экземпляров объекта, идентифицируемого по заданному идентификатору класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="634ec-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**Идентификатор класса (CLSID)**</span><span class="sxs-lookup"><span data-stu-id="634ec-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-171">Глобальный уникальный идентификатор (GUID), связанный с объектом класса OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="634ec-172">Если объект класса будет использоваться для создания более чем одного экземпляра объекта, связанное серверное приложение должно зарегистрировать его CLSID в системном реестре, чтобы клиенты могли размещать и загружать исполняемый код, связанный с объектами.</span><span class="sxs-lookup"><span data-stu-id="634ec-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="634ec-173">Каждый сервер OLE или контейнер, который допускает связывание с внедренными объектами, должен зарегистрировать идентификатор CLSID для каждого поддерживаемого определения объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**Объект класса**</span><span class="sxs-lookup"><span data-stu-id="634ec-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-175">В объектно-ориентированном программировании — объект, состояние которого совместно используется всеми объектами в классе и поведение которого действует на эти данные состояния классвиде.</span><span class="sxs-lookup"><span data-stu-id="634ec-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="634ec-176">В COM объекты класса называются фабриками классов и обычно не имеют поведения, Кроме создания новых экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="634ec-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**компьютера**</span><span class="sxs-lookup"><span data-stu-id="634ec-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-178">COM-объект, запрашивающий службы из другого объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**клиентский сайт**</span><span class="sxs-lookup"><span data-stu-id="634ec-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-180">Отображаемый сайт для внедренного или связанного объекта в составном документе.</span><span class="sxs-lookup"><span data-stu-id="634ec-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="634ec-181">Клиентский сайт — это основное средство, с помощью которого объект запрашивает службы из своего контейнера.</span><span class="sxs-lookup"><span data-stu-id="634ec-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="634ec-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-183">Глобальный уникальный идентификатор (GUID), связанный с объектом класса OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="634ec-184">Если объект класса будет использоваться для создания более чем одного экземпляра объекта, связанное серверное приложение должно зарегистрировать его CLSID в системном реестре, чтобы клиенты могли размещать и загружать исполняемый код, связанный с объектами.</span><span class="sxs-lookup"><span data-stu-id="634ec-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="634ec-185">Каждый сервер OLE или контейнер, который допускает связывание с внедренными объектами, должен зарегистрировать идентификатор CLSID для каждого поддерживаемого определения объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="634ec-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-187">Для постоянного сохранения всех изменений, внесенных в объект хранилища или потока с момента открытия или последнего сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="634ec-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**см**</span><span class="sxs-lookup"><span data-stu-id="634ec-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-189">Объект, инкапсулирующий как данные, так и код, а также предоставляет хорошо указанный набор общедоступных служб.</span><span class="sxs-lookup"><span data-stu-id="634ec-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Объектная модель компонента (COM)**</span><span class="sxs-lookup"><span data-stu-id="634ec-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-191">Объектно-ориентированная модель программирования OLE, которая определяет, как объекты взаимодействуют внутри одного процесса или между процессами.</span><span class="sxs-lookup"><span data-stu-id="634ec-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="634ec-192">В COM клиенты получают доступ к объекту через интерфейсы, реализованные в объекте.</span><span class="sxs-lookup"><span data-stu-id="634ec-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**Составная строка меню**</span><span class="sxs-lookup"><span data-stu-id="634ec-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-194">Общая строка меню, состоящая из групп меню из приложения-контейнера и серверного приложения, активируемого на месте.</span><span class="sxs-lookup"><span data-stu-id="634ec-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**составной моникер**</span><span class="sxs-lookup"><span data-stu-id="634ec-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-196">Моникер, состоящий из двух или более моникеров, обрабатываемых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="634ec-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="634ec-197">Составной моникер может быть неуниверсальным, то есть его моникеры компонента имеют особые знания друг друга или универсальные, что означает, что его моникеры компонента ничего не интересует друг с другом, за исключением того, что они являются моникерами</span><span class="sxs-lookup"><span data-stu-id="634ec-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="634ec-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**составной документ**</span><span class="sxs-lookup"><span data-stu-id="634ec-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-199">Документ, содержащий связанные или внедренные объекты, а также собственные собственные данные.</span><span class="sxs-lookup"><span data-stu-id="634ec-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**составной файл**</span><span class="sxs-lookup"><span data-stu-id="634ec-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-201">Реализация структурированного хранилища, предоставляемая OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM-объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-203">Объект, который соответствует модели COM компонента OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="634ec-204">COM-объект — это экземпляр определения объекта, который указывает данные объекта и одну или несколько реализаций интерфейсов для объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="634ec-205">Клиенты взаимодействуют с COM-объектом только через его интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="634ec-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**Подключаемый объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-207">COM-объект, реализующий как минимум интерфейс [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) для управления объектами точек соединения.</span><span class="sxs-lookup"><span data-stu-id="634ec-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="634ec-208">Подключаемые объекты поддерживают обмен данными между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="634ec-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="634ec-209">Подключаемый объект создает и управляет одним или несколькими подобъектами точек подключения, которые получают события от интерфейсов, реализованных в других объектах, и отправляют их клиенту.</span><span class="sxs-lookup"><span data-stu-id="634ec-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**объект точки подключения**</span><span class="sxs-lookup"><span data-stu-id="634ec-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-211">COM-объект, управляемый подключаемым объектом и реализующий интерфейс [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="634ec-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="634ec-212">Можно создать один или несколько объектов точек подключения и управлять ими с помощью подключаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="634ec-213">Каждый объект точки подключения управляет входящими событиями из определенного интерфейса другого объекта и отправляет эти события клиенту.</span><span class="sxs-lookup"><span data-stu-id="634ec-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**приложение контейнера**</span><span class="sxs-lookup"><span data-stu-id="634ec-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-215">Приложение, которое поддерживает составные документы.</span><span class="sxs-lookup"><span data-stu-id="634ec-215">An application that supports compound documents.</span></span> <span data-ttu-id="634ec-216">Приложение-контейнер предоставляет хранилище для внедренного или связанного объекта, сайт для его дисплея, доступ к отображаемому сайту и приемник рекомендаций для получения уведомлений об изменениях в объекте.</span><span class="sxs-lookup"><span data-stu-id="634ec-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**вложения**</span><span class="sxs-lookup"><span data-stu-id="634ec-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-218">Метод компоновки для реализации COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="634ec-219">Он позволяет одному объекту повторно использовать некоторые или все реализации интерфейса одного или нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="634ec-220">Внешний объект выступает в качестве клиента для других объектов, делегируя реализацию, когда хочет использовать службы одного из содержащихся в нем объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**локального**</span><span class="sxs-lookup"><span data-stu-id="634ec-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-222">В COM+ это набор свойств времени выполнения, связанных с одним или несколькими COM-объектами, которые используются для предоставления служб для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**элемента**</span><span class="sxs-lookup"><span data-stu-id="634ec-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-224">Внедряемый, многократно используемый COM-объект, который поддерживает, как минимум, интерфейс [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) .</span><span class="sxs-lookup"><span data-stu-id="634ec-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="634ec-225">Элементы управления обычно связаны с пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="634ec-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="634ec-226">Они также поддерживают взаимодействие с контейнером и могут повторно использоваться несколькими клиентами в зависимости от критериев лицензирования.</span><span class="sxs-lookup"><span data-stu-id="634ec-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**контейнер элементов управления**</span><span class="sxs-lookup"><span data-stu-id="634ec-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-228">Приложение, которое поддерживает внедрение элементов управления путем реализации интерфейса [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .</span><span class="sxs-lookup"><span data-stu-id="634ec-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Control, свойство**</span><span class="sxs-lookup"><span data-stu-id="634ec-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-230">Свойство времени выполнения, которое предоставляется элементом управления и управляется им.</span><span class="sxs-lookup"><span data-stu-id="634ec-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="634ec-231">Например, шрифт и размер текста, используемые элементом управления, являются свойствами элементов управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**Управление объектом**</span><span class="sxs-lookup"><span data-stu-id="634ec-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-233">Объект в статистическом объекте, который управляет тем, какие интерфейсы в объекте агрегата предоставляются и являются частными.</span><span class="sxs-lookup"><span data-stu-id="634ec-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="634ec-234">Интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) управляемого объекта называется управляющим **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="634ec-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="634ec-235">Вызовы методов **IUnknown** других объектов в статистическом выражении должны передаваться в управляющий **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="634ec-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**сайт управления**</span><span class="sxs-lookup"><span data-stu-id="634ec-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-237">Структура, реализованная контейнером элементов управления для управления отображением и хранением элемента управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="634ec-238">В заданном контейнере каждый элемент управления имеет соответствующий узел элемента управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**объект для перемещения данных**</span><span class="sxs-lookup"><span data-stu-id="634ec-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-240">Объект, реализующий интерфейс [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) и содержащий данные, передаваемые из одного объекта в другой через буфер обмена или операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="634ec-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**обработчик объектов по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="634ec-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-242">Библиотека DLL, предоставляемая с OLE, которая выступает в качестве суррогата в области обработки приложения-контейнера для реального объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="634ec-243">С помощью обработчика объектов по умолчанию можно просматривать хранимые данные объекта, не выполняя фактическую активацию объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="634ec-244">Обработчик объектов по умолчанию выполняет другие задачи, такие как отрисовка объекта из его кэшированного состояния при загрузке объекта в память.</span><span class="sxs-lookup"><span data-stu-id="634ec-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**зависимый объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-246">COM-объект, который обычно инициализируется другим объектом (ведущим объектом).</span><span class="sxs-lookup"><span data-stu-id="634ec-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="634ec-247">Несмотря на то что время существования зависимого объекта может иметь смысл только в течение времени существования ведущего объекта, объект узла не работает как управляющий [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) для зависимого объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="634ec-248">В отличие от этого, объект является агрегированным объектом, когда его время существования (с помощью его счетчика ссылок) полностью контролируется управляющим объектом.</span><span class="sxs-lookup"><span data-stu-id="634ec-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**режим прямого доступа**</span><span class="sxs-lookup"><span data-stu-id="634ec-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-250">Один из двух режимов доступа, в которых можно открыть объект хранения.</span><span class="sxs-lookup"><span data-stu-id="634ec-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="634ec-251">В режиме прямого доступа все изменения немедленно фиксируются в объекте корневого хранилища.</span><span class="sxs-lookup"><span data-stu-id="634ec-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**объект Document**</span><span class="sxs-lookup"><span data-stu-id="634ec-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-253">Документ OLE, который может отображать одно или несколько активированных на месте представлений своих данных в собственном или внешнем фрейме, таком как браузер, сохраняя полный контроль над пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="634ec-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="634ec-254">Помимо реализации обычных интерфейсов OLE и интерфейса активации на месте, объект документа должен реализовывать [**иоледокумент**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), и каждое из его представлений (в виде объекта представления документа) должно реализовывать [**иоледокументвиев**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span><span class="sxs-lookup"><span data-stu-id="634ec-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**контейнер объектов Document**</span><span class="sxs-lookup"><span data-stu-id="634ec-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-256">Приложение-контейнер может отображать одно или несколько представлений одного или нескольких объектов документа и управлять всеми содержащимися в нем объектами документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="634ec-257">Каждый объект документа связан с сайтом документа, а каждый сайт документа содержит один или несколько сайтов представления документов, соответствующих представлениям, поддерживаемым объектом Document.</span><span class="sxs-lookup"><span data-stu-id="634ec-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="634ec-258">Контейнер объектов документов также включает фрейм контейнера, который обрабатывает согласование меню и панели инструментов, а также перечисление содержащихся объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**сервер объектов документов**</span><span class="sxs-lookup"><span data-stu-id="634ec-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-260">Серверное приложение, способное предоставлять объекты документов.</span><span class="sxs-lookup"><span data-stu-id="634ec-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**сайт документа**</span><span class="sxs-lookup"><span data-stu-id="634ec-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-262">Клиентский сайт, реализованный контейнером объектов документов для управления отображением и хранением объекта документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="634ec-263">Каждый объект документа в контейнере имеет соответствующий сайт документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**объект сайта документа**</span><span class="sxs-lookup"><span data-stu-id="634ec-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-265">COM-объект, реализующий интерфейс [**иоледокументсите**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , в дополнение к обычным интерфейсам клиентского сайта (например, [**иолеклиентсите**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span><span class="sxs-lookup"><span data-stu-id="634ec-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**представление документа**</span><span class="sxs-lookup"><span data-stu-id="634ec-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-267">Конкретная презентация данных документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="634ec-268">Один объект документа может иметь одно или несколько представлений, но одно представление документа может принадлежать одному и только одному объекту документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**Объект представления документов**</span><span class="sxs-lookup"><span data-stu-id="634ec-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-270">COM-объект, реализующий интерфейс [**иоледокументвиев**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) и соответствующий определенному представлению документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="634ec-271">Объект с несколькими представлениями документа объединяет отдельный объект представления документа для каждого представления.</span><span class="sxs-lookup"><span data-stu-id="634ec-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**сайт представления документов**</span><span class="sxs-lookup"><span data-stu-id="634ec-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-273">Объект, агрегированный объектом сайта документа для управления пространством отображения для конкретного представления объекта документа.</span><span class="sxs-lookup"><span data-stu-id="634ec-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="634ec-274">В пределах конкретного сайта документа каждое представление документа имеет соответствующий сайт представления документов.</span><span class="sxs-lookup"><span data-stu-id="634ec-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**объект сайта в представлении документов**</span><span class="sxs-lookup"><span data-stu-id="634ec-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-276">COM-объект, агрегированный в объекте сайта документа и реализующий интерфейс [**иолеинплацесите**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) и, при необходимости, интерфейс [**иконтинуекаллбакк**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .</span><span class="sxs-lookup"><span data-stu-id="634ec-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**Перетаскивание**</span><span class="sxs-lookup"><span data-stu-id="634ec-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-278">Операция, в которой конечный пользователь использует мышь или другое указывающее устройство для перемещения данных в другое место в том же или другом окне.</span><span class="sxs-lookup"><span data-stu-id="634ec-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Внедрить**</span><span class="sxs-lookup"><span data-stu-id="634ec-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-280">Для вставки объекта в составной документ таким образом, чтобы сохранить форматы данных, встроенные в этот объект, и разрешить его редактирование в контейнере с помощью средств, предоставляемых его сервером.</span><span class="sxs-lookup"><span data-stu-id="634ec-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**внедренный объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-282">Объект, данные которого хранятся в составном документе, но объект выполняется в пространстве процесса сервера.</span><span class="sxs-lookup"><span data-stu-id="634ec-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="634ec-283">Обработчик объекта по умолчанию предоставляет суррогат в области обработки приложения-контейнера для реального объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**Расширенное свойство**</span><span class="sxs-lookup"><span data-stu-id="634ec-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-285">Свойство времени выполнения, например положение и размер элемента управления, которое пользователь предполагает предоставить элементу управления, но он предоставляется и управляется контейнером.</span><span class="sxs-lookup"><span data-stu-id="634ec-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**моникер файла**</span><span class="sxs-lookup"><span data-stu-id="634ec-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-287">Моникер, основанный на пути в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="634ec-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="634ec-288">Моникеры файлов можно использовать для обнаружения объектов, сохраненных в собственных файлах.</span><span class="sxs-lookup"><span data-stu-id="634ec-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="634ec-289">Моникер файла — это COM-объект, который поддерживает предоставляемую системой реализацию интерфейса [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) для класса моникера файла.</span><span class="sxs-lookup"><span data-stu-id="634ec-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**Объект Font**</span><span class="sxs-lookup"><span data-stu-id="634ec-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-291">COM-объект, предоставляющий доступ к интерфейс графических устройствным шрифтам (GDI) с помощью реализации интерфейса [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .</span><span class="sxs-lookup"><span data-stu-id="634ec-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**идентификатор формата**</span><span class="sxs-lookup"><span data-stu-id="634ec-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-293">Идентификатор GUID, определяющий набор постоянных свойств.</span><span class="sxs-lookup"><span data-stu-id="634ec-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="634ec-294">Также называется FMTID.</span><span class="sxs-lookup"><span data-stu-id="634ec-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**NOFRAMES**</span><span class="sxs-lookup"><span data-stu-id="634ec-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-296">Часть приложения-контейнера, ответственная за согласованность меню, сочетаний клавиш, панелей инструментов и других общих элементов пользовательского интерфейса с внедренным объектом COM или объектом Document.</span><span class="sxs-lookup"><span data-stu-id="634ec-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**объект Frame**</span><span class="sxs-lookup"><span data-stu-id="634ec-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-298">COM-объект, реализующий интерфейс [**иолеинплацефраме**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) и (необязательно) интерфейс [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .</span><span class="sxs-lookup"><span data-stu-id="634ec-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**универсальный составной моникер**</span><span class="sxs-lookup"><span data-stu-id="634ec-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-300">Упорядоченная коллекция моникеров, начиная с моникера файла для предоставления пути на уровне документа и продолжая с одним или несколькими моникерами элементов, которые в целом уникально идентифицируют объект.</span><span class="sxs-lookup"><span data-stu-id="634ec-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**вспомогательная функция**</span><span class="sxs-lookup"><span data-stu-id="634ec-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-302">Функция, которая инкапсулирует вызовы других функций и методов интерфейса, общедоступных в пакете SDK для OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="634ec-303">Вспомогательные функции — это удобный способ вызова часто используемых последовательностей функций и вызовов методов, которые выполняют стандартные задачи.</span><span class="sxs-lookup"><span data-stu-id="634ec-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**объект узла**</span><span class="sxs-lookup"><span data-stu-id="634ec-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-305">COM-объект, который формирует иерархическую связь с одним или несколькими объектами COM, называемыми зависимыми объектами.</span><span class="sxs-lookup"><span data-stu-id="634ec-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="634ec-306">Как правило, объект узла создает экземпляры зависимых объектов, и их существование имеет смысл только в течение времени существования объекта узла.</span><span class="sxs-lookup"><span data-stu-id="634ec-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="634ec-307">Однако объект узла не выступает в качестве управляющего [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) для зависимых объектов и не выполняет непосредственное делегирование реализаций интерфейса этих объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**СОСТАВ**</span><span class="sxs-lookup"><span data-stu-id="634ec-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-309">Непрозрачный результирующий маркер, определенный как ноль, для успешного возврата из функции и ненулевое значение, если возвращается информация об ошибке или состоянии.</span><span class="sxs-lookup"><span data-stu-id="634ec-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**объект Hyperlink**</span><span class="sxs-lookup"><span data-stu-id="634ec-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-311">COM-объект, реализующий как минимум интерфейс [**ихлинк**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) и действующий как ссылка на объект в другом расположении (цель).</span><span class="sxs-lookup"><span data-stu-id="634ec-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="634ec-312">Гиперссылка состоит из четырех частей: моникера, определяющего расположение целевого объекта. Строка для расположения в целевом объекте; понятное или отображаемое имя для целевого объекта; и строка, которая может содержать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="634ec-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**контекст обзора гиперссылок**</span><span class="sxs-lookup"><span data-stu-id="634ec-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-314">COM-объект, реализующий интерфейс [**ихлинкбровсеконтекст**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) и поддерживающий стек навигации по гиперссылкам.</span><span class="sxs-lookup"><span data-stu-id="634ec-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="634ec-315">Объект контекста обзора управляет окном фрейма гиперссылки и окном целевого объекта гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="634ec-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**контейнер гиперссылок**</span><span class="sxs-lookup"><span data-stu-id="634ec-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-317">Приложение-контейнер, которое поддерживает гиперссылки путем реализации интерфейса [**ихлинксите**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) и, если объекты контейнера могут быть целевыми объектами других гиперссылок, интерфейс [**ихлинктаржет**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="634ec-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**Объект рамки гиперссылки**</span><span class="sxs-lookup"><span data-stu-id="634ec-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-319">COM-объект, реализующий интерфейс [**ихлинкфраме**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) и управляющий навигацией верхнего уровня и отображением гиперссылок для контейнера фрейма и сервера целевого объекта гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="634ec-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**объект гиперссылки**</span><span class="sxs-lookup"><span data-stu-id="634ec-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-321">COM-объект, реализующий интерфейс [**ихлинксите**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) и предоставляющий либо моникер, либо идентификатор интерфейса его контейнера гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="634ec-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="634ec-322">Один сайт гиперссылок может обслуживать несколько гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="634ec-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**Целевой объект гиперссылки**</span><span class="sxs-lookup"><span data-stu-id="634ec-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-324">COM-объект, реализующий интерфейс [**ихлинктаржет**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) и предоставляющий его моникер, понятное имя и другую информацию, которую будут использовать другие объекты-гиперссылки для перехода к нему.</span><span class="sxs-lookup"><span data-stu-id="634ec-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**в параметре**</span><span class="sxs-lookup"><span data-stu-id="634ec-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-326">Параметр, который выделяется, задается и освобождается вызывающим объектом функции или метода интерфейса.</span><span class="sxs-lookup"><span data-stu-id="634ec-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="634ec-327">Параметр in не изменяется вызванной функцией.</span><span class="sxs-lookup"><span data-stu-id="634ec-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**параметр in/out**</span><span class="sxs-lookup"><span data-stu-id="634ec-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-329">Параметр, изначально выделенный вызывающим объектом для функции или метода интерфейса, а также при необходимости устанавливается, освобождается и перераспределяется, если это необходимо, в процессе вызова.</span><span class="sxs-lookup"><span data-stu-id="634ec-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**Активация на месте**</span><span class="sxs-lookup"><span data-stu-id="634ec-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-331">Изменение внедренного объекта в окне своего контейнера с помощью средств, предоставляемых сервером.</span><span class="sxs-lookup"><span data-stu-id="634ec-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="634ec-332">Связанные объекты не поддерживают активацию на месте; они всегда редактируются в окне сервера.</span><span class="sxs-lookup"><span data-stu-id="634ec-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**внутрипроцессный сервер**</span><span class="sxs-lookup"><span data-stu-id="634ec-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-334">Сервер, реализованный как библиотека DLL, которая выполняется в пространстве процесса клиента.</span><span class="sxs-lookup"><span data-stu-id="634ec-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**вхождение**</span><span class="sxs-lookup"><span data-stu-id="634ec-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-336">Объект, для которого выделяется память или которая является постоянной.</span><span class="sxs-lookup"><span data-stu-id="634ec-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="634ec-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-338">Группа семантически связанных функций, предоставляющих доступ к COM-объекту.</span><span class="sxs-lookup"><span data-stu-id="634ec-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="634ec-339">Каждый интерфейс OLE определяет контракт, который позволяет объектам взаимодействовать в соответствии с объектной моделью компонента (COM).</span><span class="sxs-lookup"><span data-stu-id="634ec-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="634ec-340">Хотя OLE предоставляет множество реализаций интерфейсов, большинство интерфейсов также могут быть реализованы разработчиками, создающими приложения OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**Идентификатор интерфейса (IID)**</span><span class="sxs-lookup"><span data-stu-id="634ec-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-342">Глобальный уникальный идентификатор (GUID), связанный с интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="634ec-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="634ec-343">Некоторые функции принимают идентификаторов IID в качестве параметров, позволяя вызывающей стороне указать, какой указатель интерфейса должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="634ec-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**Моникер элемента**</span><span class="sxs-lookup"><span data-stu-id="634ec-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-345">Моникер на основе строки, определяющей объект в контейнере.</span><span class="sxs-lookup"><span data-stu-id="634ec-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="634ec-346">Моникеры элементов могут обозначать объекты меньше, чем файлы, включая внедренные объекты в составной документ или псевдо-объект (например, диапазон ячеек в электронной таблице).</span><span class="sxs-lookup"><span data-stu-id="634ec-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**интерфейс**</span><span class="sxs-lookup"><span data-stu-id="634ec-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-348">Функция COM, которая обеспечивает контроль над созданием объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="634ec-349">Лицензированные объекты могут создаваться только клиентами, которым разрешено их использовать.</span><span class="sxs-lookup"><span data-stu-id="634ec-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="634ec-350">Лицензирование реализуется в COM через интерфейс [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) и с помощью поддержки лицензионного ключа, который может быть передан во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="634ec-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**объект Link**</span><span class="sxs-lookup"><span data-stu-id="634ec-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-352">COM-объект, который создается при создании или загрузке связанного COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="634ec-353">Объект Link предоставляется OLE и реализует интерфейс [**иолелинк**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .</span><span class="sxs-lookup"><span data-stu-id="634ec-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**связанный объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-355">COM-объект, исходные данные которого физически расположены там, где они изначально были созданы.</span><span class="sxs-lookup"><span data-stu-id="634ec-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="634ec-356">Вместе с составным документом сохраняются только моникер, представляющий исходные данные и соответствующие данные представления.</span><span class="sxs-lookup"><span data-stu-id="634ec-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="634ec-357">Изменения, вносимые в источник ссылки, автоматически отражаются в связанном объекте.</span><span class="sxs-lookup"><span data-stu-id="634ec-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**Источник ссылки**</span><span class="sxs-lookup"><span data-stu-id="634ec-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-359">Данные, являющиеся источником связанного объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="634ec-360">Источником связи может быть файл или часть файла, например выделенный диапазон ячеек в файле (также называемый псевдо-объектом).</span><span class="sxs-lookup"><span data-stu-id="634ec-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**загруженное состояние**</span><span class="sxs-lookup"><span data-stu-id="634ec-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-362">Состояние объекта после того, как его структуры данных загружены в память и доступны для клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="634ec-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**локальный сервер**</span><span class="sxs-lookup"><span data-stu-id="634ec-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-364">Сервер вне процесса, реализованный как. Приложение EXE работает на том же компьютере, что и его клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="634ec-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**скрыть**</span><span class="sxs-lookup"><span data-stu-id="634ec-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-366">Указатель, который удерживается и, возможно, счетчик ссылок, увеличивающийся в выполняемом объекте.</span><span class="sxs-lookup"><span data-stu-id="634ec-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="634ec-367">OLE определяет два типа блокировок, которые могут храниться в объекте: strong и слабый.</span><span class="sxs-lookup"><span data-stu-id="634ec-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="634ec-368">Чтобы реализовать строгую блокировку, сервер должен поддерживать как указатель, так и счетчик ссылок, чтобы объект оставался заблокированным в памяти по крайней мере до тех пор, пока сервер не вызовет метод [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="634ec-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="634ec-369">Чтобы реализовать слабую блокировку, сервер хранит только указатель на объект, чтобы объект мог быть уничтожен другим процессом.</span><span class="sxs-lookup"><span data-stu-id="634ec-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**Маршалинг**</span><span class="sxs-lookup"><span data-stu-id="634ec-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-371">Упаковка и отправка вызовов методов интерфейса через границы потока или процесса.</span><span class="sxs-lookup"><span data-stu-id="634ec-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**Тип носителя**</span><span class="sxs-lookup"><span data-stu-id="634ec-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-373">Расширение MIME, которое позволяет согласовать формат данных между клиентом и объектом.</span><span class="sxs-lookup"><span data-stu-id="634ec-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Тип содержимого MIME**</span><span class="sxs-lookup"><span data-stu-id="634ec-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-375">Расширение MIME, которое позволяет согласовать формат данных между клиентом и объектом.</span><span class="sxs-lookup"><span data-stu-id="634ec-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Многоцелевое расширение электронной почты в Интернете (MIME)**</span><span class="sxs-lookup"><span data-stu-id="634ec-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-377">Изначально разработанный протокол Интернета, позволяющий обмениваться сообщениями электронной почты с богатым содержимым в разнородных сетях, компьютерах и средах электронной почты.</span><span class="sxs-lookup"><span data-stu-id="634ec-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="634ec-378">На практике MIME также был принят и расширен приложениями, не являющимися почтой.</span><span class="sxs-lookup"><span data-stu-id="634ec-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**помощи**</span><span class="sxs-lookup"><span data-stu-id="634ec-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-380">Объект, реализующий интерфейс [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="634ec-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="634ec-381">Моникер выступает в качестве имени, уникально идентифицирующего COM-объект.</span><span class="sxs-lookup"><span data-stu-id="634ec-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="634ec-382">Точно так же, как путь определяет файл в файловой системе, моникер определяет COM-объект в пространстве имен каталога.</span><span class="sxs-lookup"><span data-stu-id="634ec-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**класс моникера**</span><span class="sxs-lookup"><span data-stu-id="634ec-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-384">Реализация интерфейса [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="634ec-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="634ec-385">Предоставляемые системой классы моникера включают моникеры файлов, моникеры элементов, универсальные составные моникеры, средства защиты от моникеров, моникеры указателей и моникеры URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="634ec-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**моникер клиента**</span><span class="sxs-lookup"><span data-stu-id="634ec-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-387">Приложение, использующее моникеры для получения указателей интерфейсов на объекты, управляемые другим приложением.</span><span class="sxs-lookup"><span data-stu-id="634ec-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**Поставщик моникера**</span><span class="sxs-lookup"><span data-stu-id="634ec-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-389">Приложение, которое предоставляет доступные моникеры, которые определяют объекты, которыми он управляет, чтобы объекты были доступны другим приложениям.</span><span class="sxs-lookup"><span data-stu-id="634ec-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**расширение пространства имен**</span><span class="sxs-lookup"><span data-stu-id="634ec-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-391">Внутрипроцессный COM-объект, реализующий [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**иперсистфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)и [**ишеллвиев**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), которые иногда называют интерфейсами расширения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="634ec-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="634ec-392">Расширение пространства имен используется либо для расширения пространства имен оболочки, либо для создания отдельного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="634ec-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="634ec-393">Основные пользователи — это проводник Windows и общие диалоговые окна файлов.</span><span class="sxs-lookup"><span data-stu-id="634ec-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**собственные данные**</span><span class="sxs-lookup"><span data-stu-id="634ec-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-395">Данные, используемые приложением OLE Server при редактировании внедренного объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**объектами**</span><span class="sxs-lookup"><span data-stu-id="634ec-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-397">В OLE — структура программирования, включающая как данные, так и функциональные возможности, которые определены и выделены как единое целое и для которых предоставляется только общий доступ через интерфейсы структуры программирования.</span><span class="sxs-lookup"><span data-stu-id="634ec-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="634ec-398">COM-объект должен поддерживать, как минимум, интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , который поддерживает существование объекта, пока он используется, и предоставляет доступ к другим интерфейсам объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**состояние объекта**</span><span class="sxs-lookup"><span data-stu-id="634ec-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="634ec-400">Связь между объектом составного документа в его контейнере и приложением, ответственным за создание объекта: активный, пассивный, загруженный или выполняется.</span><span class="sxs-lookup"><span data-stu-id="634ec-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="634ec-401">Пассивные объекты хранятся на диске или в базе данных, а объект не выбран или активен.</span><span class="sxs-lookup"><span data-stu-id="634ec-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="634ec-402">В загруженном состоянии структуры данных объекта были загружены в память, но недоступны для таких операций, как редактирование.</span><span class="sxs-lookup"><span data-stu-id="634ec-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="634ec-403">Работающие объекты загружаются и доступны для всех операций.</span><span class="sxs-lookup"><span data-stu-id="634ec-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="634ec-404">Активные объекты — это объекты с видимым пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="634ec-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**имя типа объекта**</span><span class="sxs-lookup"><span data-stu-id="634ec-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-406">Уникальная строка идентификации, которая хранится как часть информации, доступной для объекта в базе данных регистрации.</span><span class="sxs-lookup"><span data-stu-id="634ec-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLEDB**</span><span class="sxs-lookup"><span data-stu-id="634ec-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-408">Технология Microsoft на основе объектов для совместного использования информации и служб через границы процессов и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="634ec-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**сервер вне процесса**</span><span class="sxs-lookup"><span data-stu-id="634ec-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-410">Сервер, реализованный как. EXE-приложение, выполняемое за пределами процесса клиента либо на том же или на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="634ec-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**выходной параметр**</span><span class="sxs-lookup"><span data-stu-id="634ec-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-412">Выходной параметр выделяется вызываемой функцией и освобождается вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="634ec-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**пассивное состояние**</span><span class="sxs-lookup"><span data-stu-id="634ec-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-414">Состояние COM-объекта при его хранении (на диске или в базе данных).</span><span class="sxs-lookup"><span data-stu-id="634ec-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="634ec-415">Объект не выбран или не активен.</span><span class="sxs-lookup"><span data-stu-id="634ec-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Постоянное свойство**</span><span class="sxs-lookup"><span data-stu-id="634ec-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-417">Сведения, которые могут храниться в постоянном виде в составе объекта хранилища, например файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="634ec-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="634ec-418">Постоянные свойства группируются в наборы свойств, которые могут быть отображены и изменены.</span><span class="sxs-lookup"><span data-stu-id="634ec-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="634ec-419">Свойство persistent отличается от свойств времени выполнения объектов, созданных с помощью элементов управления OLE и технологий автоматизации, которые можно использовать для воздействия на поведение системы.</span><span class="sxs-lookup"><span data-stu-id="634ec-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="634ec-420">Структура [**пропвариант**](/windows/win32/api/propidl/ns-propidl-propvariant) определяет все допустимые типы постоянных свойств, тогда как структура **Variant** определяет все допустимые типы свойств времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="634ec-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**постоянное хранилище**</span><span class="sxs-lookup"><span data-stu-id="634ec-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-422">Хранение файла или объекта на носителе, например в файловой системе или базе данных, чтобы объект и его данные сохранялись при закрытии файла, а затем повторно открыты позже.</span><span class="sxs-lookup"><span data-stu-id="634ec-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**Объект Picture**</span><span class="sxs-lookup"><span data-stu-id="634ec-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-424">COM-объект, предоставляющий доступ к изображениям GDI путем реализации интерфейса [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .</span><span class="sxs-lookup"><span data-stu-id="634ec-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**моникер указателя**</span><span class="sxs-lookup"><span data-stu-id="634ec-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-426">Моникер, который сопоставляет указатель интерфейса с объектом в памяти.</span><span class="sxs-lookup"><span data-stu-id="634ec-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="634ec-427">В то время как большинство моникеров обозначают объекты, которые могут храниться постоянно, моникеры указателей указывают объекты, которые не могут.</span><span class="sxs-lookup"><span data-stu-id="634ec-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="634ec-428">Они позволяют таким объектам участвовать в операции привязки моникера.</span><span class="sxs-lookup"><span data-stu-id="634ec-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**данные представления**</span><span class="sxs-lookup"><span data-stu-id="634ec-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-430">Данные, используемые контейнером для вывода внедренных или связанных объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**Первичная команда**</span><span class="sxs-lookup"><span data-stu-id="634ec-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-432">Действие, связанное с наиболее распространенной или предпочтительной операцией, выполняемой пользователями для объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="634ec-433">Первичная команда всегда определяется как команда Zero в системной базе данных регистрации.</span><span class="sxs-lookup"><span data-stu-id="634ec-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="634ec-434">Основная команда объекта выполняется двойным щелчком объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**свойства**</span><span class="sxs-lookup"><span data-stu-id="634ec-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-436">Сведения, связанные с объектом.</span><span class="sxs-lookup"><span data-stu-id="634ec-436">Information that is associated with an object.</span></span> <span data-ttu-id="634ec-437">В OLE свойства делятся на две категории: свойства времени выполнения и постоянные свойства.</span><span class="sxs-lookup"><span data-stu-id="634ec-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="634ec-438">Свойства времени выполнения обычно связаны с объектами управления или их контейнерами.</span><span class="sxs-lookup"><span data-stu-id="634ec-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="634ec-439">Например, цвет фона — это свойство времени выполнения, заданное контейнером элемента управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="634ec-440">Постоянные свойства связаны с хранимыми объектами.</span><span class="sxs-lookup"><span data-stu-id="634ec-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**рамка свойства**</span><span class="sxs-lookup"><span data-stu-id="634ec-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-442">Механизм пользовательского интерфейса, отображающий одну или несколько страниц свойств для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="634ec-443">Система выполнения элементов управления OLE предоставляет стандартную реализацию рамки свойства, доступ к которой можно получить с помощью вспомогательной функции [**олекреатепропертифраме**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="634ec-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**Идентификатор свойства**</span><span class="sxs-lookup"><span data-stu-id="634ec-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-445">4-байтовое целое число со знаком, определяющее постоянное свойство в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="634ec-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**Страница свойств**</span><span class="sxs-lookup"><span data-stu-id="634ec-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-447">COM-объект с собственным идентификатором CLSID, который является частью пользовательского интерфейса, реализованного элементом управления, и позволяет просматривать и задавать свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="634ec-448">Объекты страницы свойств реализуют интерфейс [**ипропертипаже**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .</span><span class="sxs-lookup"><span data-stu-id="634ec-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**сайт страницы свойств**</span><span class="sxs-lookup"><span data-stu-id="634ec-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-450">Расположение в рамке свойства, где отображается страница свойств.</span><span class="sxs-lookup"><span data-stu-id="634ec-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="634ec-451">Рамка свойства реализует интерфейс [**ипропертипажесите**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , который содержит методы для управления узлами каждой страницы свойств, предоставляемой элементом управления.</span><span class="sxs-lookup"><span data-stu-id="634ec-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**набор свойств**</span><span class="sxs-lookup"><span data-stu-id="634ec-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-453">Логически связанная группа свойств, связанная с сохраненным объектом.</span><span class="sxs-lookup"><span data-stu-id="634ec-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="634ec-454">Чтобы создать, открыть, удалить или перечислить один или несколько наборов свойств, реализуйте интерфейс [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="634ec-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="634ec-455">При использовании составных файлов можно использовать реализацию этого интерфейса OLE, а не реализовывать собственный.</span><span class="sxs-lookup"><span data-stu-id="634ec-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**хранилище набора свойств**</span><span class="sxs-lookup"><span data-stu-id="634ec-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-457">Объект хранилища COM, содержащий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="634ec-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="634ec-458">Хранилище набора свойств — это зависимый объект, связанный с объектом хранилища и управляемый им.</span><span class="sxs-lookup"><span data-stu-id="634ec-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**Страница свойств**</span><span class="sxs-lookup"><span data-stu-id="634ec-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-460">Набор страниц свойств для одного или нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="634ec-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**-**</span><span class="sxs-lookup"><span data-stu-id="634ec-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-462">Объект, зависящий от интерфейса, который упаковывает параметры для этого интерфейса в процессе подготовки к удаленному вызову метода.</span><span class="sxs-lookup"><span data-stu-id="634ec-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="634ec-463">Прокси-сервер выполняется в адресном пространстве отправителя и взаимодействует с соответствующей заглушкой в адресном пространстве получателя.</span><span class="sxs-lookup"><span data-stu-id="634ec-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Диспетчер прокси-сервера**</span><span class="sxs-lookup"><span data-stu-id="634ec-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-465">При стандартном маршалировании — это прокси-сервер, который управляет всеми прокси интерфейсами для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**псевдо**</span><span class="sxs-lookup"><span data-stu-id="634ec-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-467">Часть документа или внедренного объекта, например диапазон ячеек в электронной таблице, которая может быть источником для COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**подсчет ссылок**</span><span class="sxs-lookup"><span data-stu-id="634ec-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-469">Поддержание счетчика каждого указателя интерфейса, хранящегося на объекте, чтобы гарантировать, что объект не будет уничтожен до освобождения всех ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="634ec-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**относительный моникер**</span><span class="sxs-lookup"><span data-stu-id="634ec-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-471">Моникер, указывающий расположение объекта относительно расположения другого объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="634ec-472">Относительный моникер аналогичен относительному пути, например. \\ Резервное копирование \\ отчета. old.</span><span class="sxs-lookup"><span data-stu-id="634ec-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**удаленный сервер**</span><span class="sxs-lookup"><span data-stu-id="634ec-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-474">Серверное приложение, реализованное как EXE-файл, выполняющееся на другом компьютере из клиентского приложения, использующего его.</span><span class="sxs-lookup"><span data-stu-id="634ec-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**Верните**</span><span class="sxs-lookup"><span data-stu-id="634ec-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-476">Значение, чтобы отменить все изменения, внесенные в объект с момента последнего фиксации изменений или открытия хранилища объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**объект корневого хранилища**</span><span class="sxs-lookup"><span data-stu-id="634ec-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-478">Внешний объект хранилища в документе.</span><span class="sxs-lookup"><span data-stu-id="634ec-478">The outermost storage object in a document.</span></span> <span data-ttu-id="634ec-479">Объект корневого хранилища может содержать другие вложенные объекты хранилища и потоки.</span><span class="sxs-lookup"><span data-stu-id="634ec-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="634ec-480">Например, составной документ сохраняется на диске в виде последовательности объектов хранилища и потоков в корневом объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="634ec-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**состояние выполнения**</span><span class="sxs-lookup"><span data-stu-id="634ec-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-482">Состояние COM-объекта при выполнении серверного приложения, а также доступ к его интерфейсам и получение уведомлений об изменениях.</span><span class="sxs-lookup"><span data-stu-id="634ec-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**работающая таблица объектов (ROT)**</span><span class="sxs-lookup"><span data-stu-id="634ec-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-484">Глобально доступная таблица на каждом компьютере, которая отслеживает все COM-объекты в состоянии выполнения, которые могут быть идентифицированы моникером.</span><span class="sxs-lookup"><span data-stu-id="634ec-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="634ec-485">Поставщики моникеров регистрируют объект в таблице, что увеличивает число ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="634ec-486">Прежде чем объект можно будет уничтожить, его моникер должен быть освобожден из таблицы.</span><span class="sxs-lookup"><span data-stu-id="634ec-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Свойство времени выполнения**</span><span class="sxs-lookup"><span data-stu-id="634ec-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-488">Сведения о дискретном состоянии, связанные с объектом элемента управления или его контейнером.</span><span class="sxs-lookup"><span data-stu-id="634ec-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="634ec-489">Существует три типа свойств времени выполнения: внешние свойства, свойства элементов управления и расширенные свойства.</span><span class="sxs-lookup"><span data-stu-id="634ec-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**Самостоятельная регистрация**</span><span class="sxs-lookup"><span data-stu-id="634ec-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-491">Процесс, с помощью которого сервер может выполнять свои собственные операции с реестром.</span><span class="sxs-lookup"><span data-stu-id="634ec-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**серверное приложение**</span><span class="sxs-lookup"><span data-stu-id="634ec-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-493">Приложение, которое может создавать COM-объекты.</span><span class="sxs-lookup"><span data-stu-id="634ec-493">An application that can create COM objects.</span></span> <span data-ttu-id="634ec-494">Затем приложения контейнера могут внедрять эти объекты или связываться с ними.</span><span class="sxs-lookup"><span data-stu-id="634ec-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**статический объект**</span><span class="sxs-lookup"><span data-stu-id="634ec-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-496">Объект, содержащий только презентацию без собственных данных.</span><span class="sxs-lookup"><span data-stu-id="634ec-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="634ec-497">Контейнер может обрабатывать статический объект так, будто он был связанным или внедренным объектом, за исключением того, что невозможно изменить статический объект.</span><span class="sxs-lookup"><span data-stu-id="634ec-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="634ec-498">Статический объект может быть результатом, например, от разрыва связи на связанном объекте, т. е. серверное приложение недоступно, или пользователь не хочет больше обновлять связанный объект.</span><span class="sxs-lookup"><span data-stu-id="634ec-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**Объект Storage**</span><span class="sxs-lookup"><span data-stu-id="634ec-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-500">COM-объект, реализующий интерфейс [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="634ec-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="634ec-501">Объект хранилища содержит вложенные объекты хранилища или объекты потока, что приводит к эквиваленту структуры каталога или файла в одном файле.</span><span class="sxs-lookup"><span data-stu-id="634ec-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**Объект Stream**</span><span class="sxs-lookup"><span data-stu-id="634ec-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-503">COM-объект, реализующий интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="634ec-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="634ec-504">Объект потока аналогичен файлу в каталоге или файловой системе.</span><span class="sxs-lookup"><span data-stu-id="634ec-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Структурированное хранилище**</span><span class="sxs-lookup"><span data-stu-id="634ec-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-506">Технология OLE для хранения составных файлов в собственных файловых системах.</span><span class="sxs-lookup"><span data-stu-id="634ec-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**ловушек**</span><span class="sxs-lookup"><span data-stu-id="634ec-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-508">Когда параметры метода функции или интерфейса передаются через границу процесса, заглушка представляет собой объект определенного интерфейса, который разбивает Упакованные параметры и вызывает требуемый метод.</span><span class="sxs-lookup"><span data-stu-id="634ec-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="634ec-509">Заглушка выполняется в адресном пространстве получателя и взаимодействует с соответствующим прокси-сервером в адресном пространстве отправителя.</span><span class="sxs-lookup"><span data-stu-id="634ec-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Диспетчер заглушек**</span><span class="sxs-lookup"><span data-stu-id="634ec-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-511">Управляет всеми заглушками интерфейсов для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="634ec-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**синхронный вызов**</span><span class="sxs-lookup"><span data-stu-id="634ec-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-513">Вызов функции, который не позволяет выполнять дальнейшие инструкции в вызывающем процессе, пока функция не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="634ec-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**системный реестр**</span><span class="sxs-lookup"><span data-stu-id="634ec-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-515">Системный репозиторий данных, поддерживаемых Windows, который содержит сведения о системе и ее приложениях, включая клиенты и серверы OLE.</span><span class="sxs-lookup"><span data-stu-id="634ec-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**режим транзакционного доступа**</span><span class="sxs-lookup"><span data-stu-id="634ec-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-517">Один из двух режимов доступа, в которых можно открыть объект хранения.</span><span class="sxs-lookup"><span data-stu-id="634ec-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="634ec-518">При открытии в режиме транзакций изменения сохраняются в буферах до тех пор, пока объект корневого хранилища не зафиксирует свои изменения.</span><span class="sxs-lookup"><span data-stu-id="634ec-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**сведения о типе**</span><span class="sxs-lookup"><span data-stu-id="634ec-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-520">Сведения о классе объекта, предоставляемом библиотекой типов.</span><span class="sxs-lookup"><span data-stu-id="634ec-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="634ec-521">Для предоставления сведений о типах COM-объект реализует интерфейс [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="634ec-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**Единая для обмена данными**</span><span class="sxs-lookup"><span data-stu-id="634ec-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-523">Модель для передачи данных через буфер обмена, перетаскивание или автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="634ec-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="634ec-524">Объекты, согласованные с этой моделью, реализуют интерфейс [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="634ec-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="634ec-525">Эта модель заменяет DDE (динамический обмен данными).</span><span class="sxs-lookup"><span data-stu-id="634ec-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="634ec-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**демаршалинга**</span><span class="sxs-lookup"><span data-stu-id="634ec-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-527">Распаковка параметров, отправленных на прокси-сервер через границы процесса.</span><span class="sxs-lookup"><span data-stu-id="634ec-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**Указатель универсального ресурса (URL-адрес)**</span><span class="sxs-lookup"><span data-stu-id="634ec-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-529">Идентификатор, используемый в Интернете для имен и расположений объектов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="634ec-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="634ec-530">OLE предоставляет класс моникера, моникер URL, реализацию которого можно использовать для привязки клиента к объектам, идентифицируемым по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="634ec-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="634ec-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Моникер URL**</span><span class="sxs-lookup"><span data-stu-id="634ec-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="634ec-532">Моникер, основанный на указателе универсального ресурса (URL).</span><span class="sxs-lookup"><span data-stu-id="634ec-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="634ec-533">Клиент может использовать моникеры URL-адресов для привязки к объектам, размещенным в Интернете.</span><span class="sxs-lookup"><span data-stu-id="634ec-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="634ec-534">Предоставляемый системой класс моникера поддерживает как синхронную, так и асинхронную привязку.</span><span class="sxs-lookup"><span data-stu-id="634ec-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 