---
description: Введение в разработку фильтров DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Введение в разработку фильтров DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682238"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="31eba-103">Введение в разработку фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="31eba-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="31eba-104">В этом разделе приводится краткий обзор задач, связанных с разработкой пользовательского фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="31eba-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="31eba-105">Здесь также приводятся ссылки на разделы, в которых более подробно рассматриваются эти задачи.</span><span class="sxs-lookup"><span data-stu-id="31eba-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="31eba-106">Перед чтением этого раздела ознакомьтесь с подразделами [о DirectShow](about-directshow.md), в которых описывается общая архитектура DirectShow.</span><span class="sxs-lookup"><span data-stu-id="31eba-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="31eba-107">**Библиотека базовых классов DirectShow**</span><span class="sxs-lookup"><span data-stu-id="31eba-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="31eba-108">Пакет SDK для DirectShow включает набор классов C++ для записи фильтров.</span><span class="sxs-lookup"><span data-stu-id="31eba-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="31eba-109">Хотя это и не является обязательным, эти классы являются рекомендуемым способом записи нового фильтра.</span><span class="sxs-lookup"><span data-stu-id="31eba-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="31eba-110">Чтобы использовать базовые классы, скомпилируйте их в статическую библиотеку и свяжите LIB-файл с проектом, как описано в разделе [Создание фильтров DirectShow](building-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="31eba-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="31eba-111">Базовая библиотека классов определяет корневой класс для фильтров, класс [**кбасефилтер**](cbasefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="31eba-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="31eba-112">Несколько других классов являются производными от **кбасефилтер** и являются специализированными для определенных типов фильтров.</span><span class="sxs-lookup"><span data-stu-id="31eba-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="31eba-113">Например, класс [**ктрансформфилтер**](ctransformfilter.md) предназначен для фильтров преобразований.</span><span class="sxs-lookup"><span data-stu-id="31eba-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="31eba-114">Чтобы создать новый фильтр, Реализуйте класс, наследующий от одного из классов фильтров.</span><span class="sxs-lookup"><span data-stu-id="31eba-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="31eba-115">Например, объявление класса может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="31eba-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="31eba-116">Дополнительные сведения о базовых классах DirectShow см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="31eba-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="31eba-117">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="31eba-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="31eba-118">Создание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="31eba-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="31eba-119">**Создание ПИН-кодов**</span><span class="sxs-lookup"><span data-stu-id="31eba-119">**Creating Pins**</span></span>

<span data-ttu-id="31eba-120">Фильтр должен создать один или несколько ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="31eba-120">A filter must create one or more pins.</span></span> <span data-ttu-id="31eba-121">Количество ПИН-кодов можно исправить во время разработки, или фильтр может создавать новые ПИН-коды по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="31eba-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="31eba-122">ПИН-коды обычно являются производными от класса [**кбасепин**](cbasepin.md) или от класса, который наследует **Кбасепин**, например [**кбасеинпутпин**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="31eba-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="31eba-123">ПИН-коды фильтра должны объявляться как переменные-члены в классе Filter.</span><span class="sxs-lookup"><span data-stu-id="31eba-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="31eba-124">Некоторые из классов фильтров уже определяют ПИН-коды, но если фильтр наследует непосредственно от **кбасефилтер**, необходимо объявить эти ПИН-коды в производном классе.</span><span class="sxs-lookup"><span data-stu-id="31eba-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="31eba-125">**Согласование соединений с ПИН-кодом**</span><span class="sxs-lookup"><span data-stu-id="31eba-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="31eba-126">Когда диспетчер графов фильтров пытается подключить два фильтра, ПИН-коды должны согласовать различные вещи.</span><span class="sxs-lookup"><span data-stu-id="31eba-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="31eba-127">В противном случае попытка подключения завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="31eba-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="31eba-128">Обычно ПИН-коды согласовывают следующее:</span><span class="sxs-lookup"><span data-stu-id="31eba-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="31eba-129">Transport.</span><span class="sxs-lookup"><span data-stu-id="31eba-129">Transport.</span></span> <span data-ttu-id="31eba-130">Транспорт — это механизм, который используется фильтрами для перемещения образцов мультимедиа из выходного крепления на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="31eba-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="31eba-131">Например, они могут использовать интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("Push Model") или интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("модель извлечения").</span><span class="sxs-lookup"><span data-stu-id="31eba-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="31eba-132">Тип носителя.</span><span class="sxs-lookup"><span data-stu-id="31eba-132">Media type.</span></span> <span data-ttu-id="31eba-133">Почти все контакты используют типы носителей для описания формата данных, которые они будут доставлять.</span><span class="sxs-lookup"><span data-stu-id="31eba-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="31eba-134">Выделен.</span><span class="sxs-lookup"><span data-stu-id="31eba-134">Allocator.</span></span> <span data-ttu-id="31eba-135">Распределитель — это объект, который создает буферы, в которых хранятся данные.</span><span class="sxs-lookup"><span data-stu-id="31eba-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="31eba-136">ПИН-код должен согласиться с тем, какой PIN будет предоставлять распределитель.</span><span class="sxs-lookup"><span data-stu-id="31eba-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="31eba-137">Они также должны согласовать размер буферов, число создаваемых буферов и другие свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="31eba-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="31eba-138">Базовые классы реализуют платформу для этих согласований.</span><span class="sxs-lookup"><span data-stu-id="31eba-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="31eba-139">Эти сведения необходимо выполнить путем переопределения различных методов в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="31eba-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="31eba-140">Набор методов, которые необходимо переопределить, зависит от класса и от функциональности фильтра.</span><span class="sxs-lookup"><span data-stu-id="31eba-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="31eba-141">Дополнительные сведения см. в разделе [Подключение фильтров](how-filters-connect.md).</span><span class="sxs-lookup"><span data-stu-id="31eba-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="31eba-142">**Обработка и доставка данных**</span><span class="sxs-lookup"><span data-stu-id="31eba-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="31eba-143">Основная функция большинства фильтров — обработка и доставка данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31eba-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="31eba-144">Как это происходит, зависит от типа фильтра:</span><span class="sxs-lookup"><span data-stu-id="31eba-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="31eba-145">Источник push-уведомлений содержит рабочий поток, который непрерывно заполняет образцы данными и доставляет их в нисходящий.</span><span class="sxs-lookup"><span data-stu-id="31eba-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="31eba-146">Источник извлечения ожидает, что его подчиненный сосед запрашивает пример.</span><span class="sxs-lookup"><span data-stu-id="31eba-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="31eba-147">Он отвечает, записывая данные в пример и доставляя пример подчиненному фильтру.</span><span class="sxs-lookup"><span data-stu-id="31eba-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="31eba-148">Нисходящий фильтр создает поток, который управляет потоком данных.</span><span class="sxs-lookup"><span data-stu-id="31eba-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="31eba-149">Фильтр преобразования содержит образцы, доставленные ему из вышестоящего соседнего узла.</span><span class="sxs-lookup"><span data-stu-id="31eba-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="31eba-150">При получении образца он обрабатывает данные и доставляет их нисходящим.</span><span class="sxs-lookup"><span data-stu-id="31eba-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="31eba-151">Фильтр модуля подготовки отчетов получает образцы из вышестоящего представления и планирует их отрисовку на основе меток времени.</span><span class="sxs-lookup"><span data-stu-id="31eba-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="31eba-152">Другие задачи, связанные с потоковой передачей, включают запись данных из графа, обработку конца потока и реагирование на запросы поиска.</span><span class="sxs-lookup"><span data-stu-id="31eba-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="31eba-153">Дополнительные сведения об этих проблемах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="31eba-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="31eba-154">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="31eba-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="31eba-155">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="31eba-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="31eba-156">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="31eba-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="31eba-157">**Поддержка COM**</span><span class="sxs-lookup"><span data-stu-id="31eba-157">**Supporting COM**</span></span>

<span data-ttu-id="31eba-158">Фильтры DirectShow — это COM-объекты, обычно Упакованные в библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="31eba-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="31eba-159">Базовая библиотека классов реализует платформу для поддержки COM.</span><span class="sxs-lookup"><span data-stu-id="31eba-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="31eba-160">Он описан в разделе [DirectShow и com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="31eba-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31eba-161">См. также</span><span class="sxs-lookup"><span data-stu-id="31eba-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31eba-162">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="31eba-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



