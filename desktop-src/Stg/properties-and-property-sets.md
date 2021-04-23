---
title: Свойства и наборы свойств
description: Хотя типы свойств времени выполнения, предлагаемые автоматизацией и элементами управления Microsoft ActiveX, являются важными, они не требуют непосредственного хранения информации с объектами, сохраняемыми в файловой системе.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Структурированное хранилище Стрктд STG, основы, свойства и наборы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411442"
---
# <a name="properties-and-property-sets"></a><span data-ttu-id="24114-104">Свойства и наборы свойств</span><span class="sxs-lookup"><span data-stu-id="24114-104">Properties and Property Sets</span></span>

<span data-ttu-id="24114-105">Хотя типы свойств времени выполнения, предлагаемые автоматизацией и элементами управления Microsoft ActiveX, являются важными, они не требуют непосредственного хранения информации с объектами, сохраняемыми в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="24114-105">While the kinds of run-time properties that Automation and Microsoft ActiveX Controls offer are important, they do not directly address the need to store information with objects persistently stored in the file system.</span></span> <span data-ttu-id="24114-106">Эти сущности могут включать файлы (структурированные, составные и т. д.), каталоги и Сводные каталоги.</span><span class="sxs-lookup"><span data-stu-id="24114-106">These entities could include files (structured, compound, and so forth), directories, and summary catalogs.</span></span> <span data-ttu-id="24114-107">COM предоставляет как стандартный сериализованный формат для этих постоянных свойств, так и набор интерфейсов и функций, которые позволяют создавать наборы свойств и их свойства, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="24114-107">COM provides both a standard serialized format for these persistent properties, and a set of interfaces and functions that allow you to create and manipulate the property sets and their properties.</span></span>

<span data-ttu-id="24114-108">Постоянные свойства хранятся в виде наборов, а один или несколько наборов могут быть связаны с сущностью файловой системы.</span><span class="sxs-lookup"><span data-stu-id="24114-108">Persistent properties are stored as sets, and one or more sets may be associated with a file system entity.</span></span> <span data-ttu-id="24114-109">Эти постоянные наборы свойств предназначены для хранения данных, которые предназначены для представления в виде коллекции детализированных значений.</span><span class="sxs-lookup"><span data-stu-id="24114-109">These persistent property sets are intended to be used to store data that is suited to being represented as a collection of fine-grained values.</span></span> <span data-ttu-id="24114-110">Они не предназначены для использования в качестве базы данных большого размера.</span><span class="sxs-lookup"><span data-stu-id="24114-110">They are not intended to be used as a large data base.</span></span> <span data-ttu-id="24114-111">Они могут использоваться для хранения сводных данных об объекте в системе, к которым затем можно получить доступ любым другим объектом, который понимает, как интерпретировать этот набор свойств.</span><span class="sxs-lookup"><span data-stu-id="24114-111">They can be used to store summary information about an object on the system, which can then be accessed by any other object that understands how to interpret that property set.</span></span>

<span data-ttu-id="24114-112">Предыдущие версии COM задаются очень мало по отношению к свойствам и их использованию, но определили сериализованный формат, который позволял разработчикам хранить свойства и наборы свойств в экземпляре [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="24114-112">Previous versions of COM specified very little with respect to properties and their usage, but did define a serialized format that allowed developers to store properties and property sets in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance.</span></span> <span data-ttu-id="24114-113">Были также определены идентификаторы и семантику одного набора свойств, используемого для сводных сведений о документе.</span><span class="sxs-lookup"><span data-stu-id="24114-113">The property identifiers and semantics of a single property set, used for summary information about a document, were also defined.</span></span> <span data-ttu-id="24114-114">В этот момент требовалось создавать структуру и манипулировать ею непосредственно в виде потока данных.</span><span class="sxs-lookup"><span data-stu-id="24114-114">At that time, it was necessary to create and manipulate that structure directly as a data stream.</span></span> <span data-ttu-id="24114-115">См. раздел [структурированное хранилище. формат набора свойств сериализованный](structured-storage-serialized-property-set-format.md).</span><span class="sxs-lookup"><span data-stu-id="24114-115">See [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).</span></span>

<span data-ttu-id="24114-116">Однако теперь COM определяет два основных интерфейса для управления наборами свойств:</span><span class="sxs-lookup"><span data-stu-id="24114-116">Now, however, COM defines two primary interfaces to manage property sets:</span></span>

-   [<span data-ttu-id="24114-117">**ипропертистораже**</span><span class="sxs-lookup"><span data-stu-id="24114-117">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [<span data-ttu-id="24114-118">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="24114-118">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

<span data-ttu-id="24114-119">Больше не нужно напрямую работать с сериализованным форматом, когда эти интерфейсы реализуются на объекте, поддерживающем интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (например, составные файлы).</span><span class="sxs-lookup"><span data-stu-id="24114-119">It is no longer necessary to deal with the serialized format directly when these interfaces are implemented on an object that supports the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface (such as compound files).</span></span> <span data-ttu-id="24114-120">При записи свойств с помощью [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) создаются данные, которые точно соответствуют формату набора свойств COM, как они просматриваются с помощью методов **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="24114-120">Writing properties through [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates data that exactly conforms to the COM property set format, as viewed through **IStorage** methods.</span></span> <span data-ttu-id="24114-121">Обратное также верно. свойства, записываемые в формат набора свойств COM с помощью **IStorage** , видимы через **IPropertySetStorage** и **ипропертистораже** (хотя вы не можете выполнять запись в [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) и иметь свойства через **ипропертистораже** немедленно, или наоборот).</span><span class="sxs-lookup"><span data-stu-id="24114-121">The converse is also true — properties written to the COM property set format using **IStorage** are visible through **IPropertySetStorage** and **IPropertyStorage** (although you cannot expect to write to [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) and have the properties through **IPropertyStorage** immediately available, or vice versa).</span></span>

<span data-ttu-id="24114-122">Интерфейс [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) определяет методы, которые создают наборы свойств и управляют ими.</span><span class="sxs-lookup"><span data-stu-id="24114-122">The [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface defines methods that create and manage property sets.</span></span> <span data-ttu-id="24114-123">Интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) напрямую управляет свойствами в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="24114-123">The [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface directly manipulates the properties within a property set.</span></span> <span data-ttu-id="24114-124">Вызывая методы этих интерфейсов, разработчик приложения может управлять тем, какие наборы свойств подходят для данной сущности файловой системы.</span><span class="sxs-lookup"><span data-stu-id="24114-124">By calling the methods of these interfaces, an application developer can manage whatever property sets are appropriate for a given file system entity.</span></span> <span data-ttu-id="24114-125">Использование этих интерфейсов предоставляет одну настроенную для чтения и записи реализацию свойств, а не реализацию в каждом приложении, где может быть узким местом производительности, например инцессант поиска.</span><span class="sxs-lookup"><span data-stu-id="24114-125">Use of these interfaces provides one tuned reading and writing implementation for properties, rather than having an implementation in each application, where there could be performance bottlenecks such as incessant seeking.</span></span> <span data-ttu-id="24114-126">Вы можете реализовать интерфейсы для повышения производительности, чтобы свойства могли быть прочитаны и записаны быстрее, например, более эффективным кэшированием.</span><span class="sxs-lookup"><span data-stu-id="24114-126">You can implement the interfaces to enhance performance, so properties can be read and written more quickly by, for example, more efficient caching.</span></span> <span data-ttu-id="24114-127">Более того, **ипропертистораже** и **IPropertySetStorage** позволяют управлять свойствами сущностей, которые не поддерживают [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), хотя в целом большинство приложений этого не делает.</span><span class="sxs-lookup"><span data-stu-id="24114-127">Furthermore, **IPropertyStorage** and **IPropertySetStorage** make it possible to manipulate properties on entities that do not support [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), although in general, most applications will not do so.</span></span>

<span data-ttu-id="24114-128">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="24114-128">This section contains the following topics:</span></span>

-   [<span data-ttu-id="24114-129">Набор свойств сводных данных</span><span class="sxs-lookup"><span data-stu-id="24114-129">The Summary Information Property Set</span></span>](the-summary-information-property-set.md)
-   [<span data-ttu-id="24114-130">Стандартные идентификаторы формата набора свойств</span><span class="sxs-lookup"><span data-stu-id="24114-130">Predefined Property Set Format Identifiers</span></span>](predefined-property-set-format-identifiers.md)
-   [<span data-ttu-id="24114-131">Свойства Документсуммаринформатион и Пользователяопределенные задают</span><span class="sxs-lookup"><span data-stu-id="24114-131">The DocumentSummaryInformation and UserDefined Property Sets</span></span>](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a><span data-ttu-id="24114-132">См. также</span><span class="sxs-lookup"><span data-stu-id="24114-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24114-133">Реализация наборов свойств в COM</span><span class="sxs-lookup"><span data-stu-id="24114-133">Property Set Implementations in COM</span></span>](property-set-implementations-in-com.md)
</dt> <dt>

[<span data-ttu-id="24114-134">Рекомендации по установке свойств</span><span class="sxs-lookup"><span data-stu-id="24114-134">Property Set Considerations</span></span>](property-set-considerations.md)
</dt> <dt>

[<span data-ttu-id="24114-135">Управление свойствами</span><span class="sxs-lookup"><span data-stu-id="24114-135">Managing Properties</span></span>](managing-properties.md)
</dt> <dt>

[<span data-ttu-id="24114-136">Управление наборами свойств</span><span class="sxs-lookup"><span data-stu-id="24114-136">Managing Property Sets</span></span>](managing-property-sets.md)
</dt> <dt>

[<span data-ttu-id="24114-137">Хранение наборов свойств</span><span class="sxs-lookup"><span data-stu-id="24114-137">Storing Property Sets</span></span>](storing-property-sets.md)
</dt> <dt>

[<span data-ttu-id="24114-138">Характеристики производительности</span><span class="sxs-lookup"><span data-stu-id="24114-138">Performance Characteristics</span></span>](performance-characteristics.md)
</dt> </dl>

 

 




