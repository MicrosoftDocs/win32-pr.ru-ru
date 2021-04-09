---
title: Составные документы
description: Составные документы OLE позволяют пользователям, работающим в одном приложении, работать с данными, написанными в различных форматах и производными от нескольких источников.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134682"
---
# <a name="compound-documents"></a><span data-ttu-id="82571-103">Составные документы</span><span class="sxs-lookup"><span data-stu-id="82571-103">Compound Documents</span></span>

<span data-ttu-id="82571-104">Составные документы OLE позволяют пользователям, работающим в одном приложении, работать с данными, написанными в различных форматах и производными от нескольких источников.</span><span class="sxs-lookup"><span data-stu-id="82571-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="82571-105">Например, пользователь может вставить в документ обработки текста граф, созданный во втором приложении, и объект Sound, созданный в третьем приложении.</span><span class="sxs-lookup"><span data-stu-id="82571-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="82571-106">Активация графа приводит к тому, что второе приложение загружает пользовательский интерфейс или по крайней мере ту часть, которая содержит инструменты, необходимые для редактирования объекта.</span><span class="sxs-lookup"><span data-stu-id="82571-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="82571-107">Активация объекта Sound приводит к тому, что третье приложение воспроизводит его.</span><span class="sxs-lookup"><span data-stu-id="82571-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="82571-108">В обоих случаях пользователь может манипулировать данными из внешних источников в контексте одного документа.</span><span class="sxs-lookup"><span data-stu-id="82571-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="82571-109">Технологии составных документов OLE — это основы, состоящие из модели COM, структурированного хранилища и равномерной пересылки данных.</span><span class="sxs-lookup"><span data-stu-id="82571-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="82571-110">Как показано ниже, каждая из этих основных технологий играет важную роль в составных документах OLE:</span><span class="sxs-lookup"><span data-stu-id="82571-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="82571-111"><span id="COM"></span><span id="com"></span>-</span><span class="sxs-lookup"><span data-stu-id="82571-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="82571-112">Объект составного документа — это, по сути, объект COM, который можно внедрить в существующий документ или связать с ним.</span><span class="sxs-lookup"><span data-stu-id="82571-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="82571-113">В качестве объекта COM объект составного документа предоставляет интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , через который клиенты могут получать указатели на другие интерфейсы, в том числе несколько, например [**иолеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**иолелинк**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)и [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), которые предоставляют специальные функции, уникальные для объектов составного документа.</span><span class="sxs-lookup"><span data-stu-id="82571-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="82571-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="82571-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="82571-115">Объект составного документа должен реализовывать [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) или, при необходимости, интерфейсы [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) для управления собственным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="82571-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="82571-116">Контейнер, используемый для создания составных документов, должен предоставлять интерфейс [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , через который объекты хранят и извлекают данные.</span><span class="sxs-lookup"><span data-stu-id="82571-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="82571-117">Контейнеры практически всегда предоставляют экземпляры **IStorage** , полученные из реализации составных файлов OLE.</span><span class="sxs-lookup"><span data-stu-id="82571-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="82571-118">Контейнеры также должны использовать интерфейсы **иперсистстораже** и/или **IPersistStream** объекта.</span><span class="sxs-lookup"><span data-stu-id="82571-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="82571-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Однородное Передача данных</span><span class="sxs-lookup"><span data-stu-id="82571-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="82571-120">Приложения, поддерживающие составные документы, должны реализовать интерфейс [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , так как внедренные объекты и связанные объекты начинаются как данные, перенесенные с помощью специальных форматов буфера обмена OLE, а не стандартные форматы буфера обмена Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="82571-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="82571-121">Другими словами, форматирование данных как внедренного или связанного объекта — это еще один вариант, предоставляемый унифицированной моделью обмена данными OLE.</span><span class="sxs-lookup"><span data-stu-id="82571-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="82571-122">Технология составных документов OLE дает преимущества как разработчикам программного обеспечения, так и пользователям.</span><span class="sxs-lookup"><span data-stu-id="82571-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="82571-123">Вместо того, чтобы прикрам каждую представить функцию в единое приложение, разработчики программного обеспечения теперь могут свободно работать, если они предназначены для разработки небольших, более специализированных приложений, которые используют другие приложения для предоставления дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="82571-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="82571-124">В случаях, когда разработчик программного обеспечения решает предоставить приложение с возможностями, которые выходят за пределы основных функций, разработчик может реализовать эти дополнительные службы в виде отдельных библиотек DLL, которые загружаются в память только при необходимости их служб.</span><span class="sxs-lookup"><span data-stu-id="82571-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="82571-125">Пользователи получают преимущества от меньшего, более быстрого, более производительного программного обеспечения, которое они могут комбинировать и сопоставлять по мере необходимости, управляя всеми необходимыми компонентами в рамках одного главного документа.</span><span class="sxs-lookup"><span data-stu-id="82571-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="82571-126">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="82571-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="82571-127">Контейнеры и серверы</span><span class="sxs-lookup"><span data-stu-id="82571-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="82571-128">Связывание и внедрение</span><span class="sxs-lookup"><span data-stu-id="82571-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="82571-129">Обработчики объектов</span><span class="sxs-lookup"><span data-stu-id="82571-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="82571-130">Внутрипроцессный сервер</span><span class="sxs-lookup"><span data-stu-id="82571-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="82571-131">Связанные объекты и моникеры</span><span class="sxs-lookup"><span data-stu-id="82571-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="82571-132">Уведомления</span><span class="sxs-lookup"><span data-stu-id="82571-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="82571-133">Интерфейсы составных документов</span><span class="sxs-lookup"><span data-stu-id="82571-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="82571-134">Состояния объектов</span><span class="sxs-lookup"><span data-stu-id="82571-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="82571-135">Реализация активации In-Place</span><span class="sxs-lookup"><span data-stu-id="82571-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="82571-136">Создание связанных и внедренных объектов из существующих данных</span><span class="sxs-lookup"><span data-stu-id="82571-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="82571-137">Просмотр кэширования</span><span class="sxs-lookup"><span data-stu-id="82571-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="82571-138">См. также</span><span class="sxs-lookup"><span data-stu-id="82571-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82571-139">Передача данных</span><span class="sxs-lookup"><span data-stu-id="82571-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="82571-140">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="82571-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 