---
description: Существует три класса, предоставляемых библиотекой Комадмин (comadmin.dll), каждая из которых реализует сдвоенный интерфейс COM.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Сводное описание классов Комадмин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662086"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="4c8d4-103">Сводное описание классов Комадмин</span><span class="sxs-lookup"><span data-stu-id="4c8d4-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="4c8d4-104">Существует три класса, предоставляемых библиотекой Комадмин (comadmin.dll), каждая из которых реализует сдвоенный интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="4c8d4-105">Объекты, созданные из этих классов, используются для получения доступа к каталогу, для представления коллекций в каталоге и для представления элементов, содержащихся в коллекциях.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="4c8d4-106">комадминкаталог</span><span class="sxs-lookup"><span data-stu-id="4c8d4-106">COMAdminCatalog</span></span>

<span data-ttu-id="4c8d4-107">Класс [**комадминкаталог**](comadmincatalog.md) представляет сам каталог.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="4c8d4-108">Объект, созданный из **комадминкаталог** , является основным объектом, который используется в программном администрировании.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="4c8d4-109">Помимо установки базового соединения с сервером каталога при его создании, **комадминкаталог** предоставляет методы, позволяющие выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4c8d4-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="4c8d4-110">Получение коллекций в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="4c8d4-111">Подключитесь к серверу каталога на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="4c8d4-112">Установка, экспорт, запуск, завершение работы и получение сведений о приложениях COM+.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="4c8d4-113">Установка компонентов в приложения COM+ и получение сведений о компонентах.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="4c8d4-114">Запуск, завершение или обновление служб, запущенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="4c8d4-115">Обновление, восстановление или резервное копирование данных каталога.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="4c8d4-116">В COM+ 1,0 класс [**комадминкаталог**](comadmincatalog.md) реализует интерфейс [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="4c8d4-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="4c8d4-117">В COM+ 1,5 класс **комадминкаталог** реализует [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) в качестве интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="4c8d4-118">комадминкаталогколлектион</span><span class="sxs-lookup"><span data-stu-id="4c8d4-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="4c8d4-119">Класс [**комадминкаталогколлектион**](comadmincatalogcollection.md) представляет любую коллекцию в каталоге, предоставляя строковое имя определенной коллекции во время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="4c8d4-120">(Доступные коллекции каталогов именуются в таблице в [коллекции администрирования com+](com--administration-collections.md).) Объекты создаются из этого класса при получении коллекции верхнего уровня путем вызова метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="4c8d4-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="4c8d4-121">Эти объекты также создаются при извлечении дочерней коллекции путем вызова метода **IsCollection** своего родительского объекта Collection.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="4c8d4-122">Объекты **комадминкаталогколлектион** позволяют выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="4c8d4-123">Перечисление элементов, содержащихся в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="4c8d4-124">Получение элемента из коллекции.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="4c8d4-125">Добавление или удаление элементов в коллекции или из нее.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="4c8d4-126">Сохранение или Отмена всех ожидающих изменений, внесенных в коллекцию, или элементов, которые она содержит.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="4c8d4-127">Получение другой коллекции в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="4c8d4-128">Класс [**комадминкаталогобжект**](comadmincatalogobject.md) реализует интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .</span><span class="sxs-lookup"><span data-stu-id="4c8d4-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="4c8d4-129">комадминкаталогобжект</span><span class="sxs-lookup"><span data-stu-id="4c8d4-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="4c8d4-130">Класс [**комадминкаталогобжект**](comadmincatalogobject.md) представляет любой элемент, содержащийся в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="4c8d4-131">Объекты создаются из этого класса при получении элемента через свойство [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) объекта коллекции каталога.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="4c8d4-132">Объекты, созданные из класса **комадминкаталогобжект** , позволяют выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="4c8d4-133">Возвращает или задает свойства, поддерживаемые элементом, который используется объектом для представления.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="4c8d4-134">Получение сведений об элементе и его свойствах.</span><span class="sxs-lookup"><span data-stu-id="4c8d4-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="4c8d4-135">Класс [**комадминкаталогобжект**](comadmincatalogobject.md) реализует интерфейс [**икаталогобжект**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="4c8d4-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c8d4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="4c8d4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c8d4-137">Доступ к каталогу COM+</span><span class="sxs-lookup"><span data-stu-id="4c8d4-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="4c8d4-138">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="4c8d4-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



