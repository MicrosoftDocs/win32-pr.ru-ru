---
description: Фильтры драйвера класса WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Фильтры драйвера класса WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898162"
---
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="5390a-103">Фильтры драйвера класса WDM</span><span class="sxs-lookup"><span data-stu-id="5390a-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="5390a-104">Если устройство записи использует драйвер WDM (WDM), для диаграммы могут потребоваться определенные фильтры из фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="5390a-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="5390a-105">Эти фильтры называются фильтрами драйверов потокового класса или фильтрами WDM.</span><span class="sxs-lookup"><span data-stu-id="5390a-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="5390a-106">Они поддерживают дополнительные функции, предоставляемые оборудованием.</span><span class="sxs-lookup"><span data-stu-id="5390a-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="5390a-107">Например, плата ТВ-тюнера имеет функции для настройки канала.</span><span class="sxs-lookup"><span data-stu-id="5390a-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="5390a-108">Соответствующий фильтр — это фильтр [ТВ-тюнера](tv-tuner-filter.md) , который предоставляет интерфейс [**иамтвтунер**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="5390a-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="5390a-109">Чтобы сделать эту функцию доступной для приложения, необходимо подключить фильтр ТВ-тюнера к фильтру записи.</span><span class="sxs-lookup"><span data-stu-id="5390a-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="5390a-110">Интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) предоставляет самый простой способ добавления фильтров WDM в граф.</span><span class="sxs-lookup"><span data-stu-id="5390a-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="5390a-111">В некоторый момент при построении графа вызовите [**финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) или [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="5390a-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="5390a-112">Любой из этих методов автоматически обнаружит необходимые фильтры WDM и подключится к фильтру записи.</span><span class="sxs-lookup"><span data-stu-id="5390a-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="5390a-113">В оставшейся части этого раздела описано, как добавить фильтры WDM вручную.</span><span class="sxs-lookup"><span data-stu-id="5390a-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="5390a-114">Однако следует иметь в виду, что рекомендуемый подход просто вызывает один из этих методов **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="5390a-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="5390a-115">ПИН-коды в фильтре WDM поддерживают один или несколько средних.</span><span class="sxs-lookup"><span data-stu-id="5390a-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="5390a-116">Средний уровень определяет способ связи, например шину.</span><span class="sxs-lookup"><span data-stu-id="5390a-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="5390a-117">Необходимо подключить ПИН-коды, поддерживающие один и тот же носитель.</span><span class="sxs-lookup"><span data-stu-id="5390a-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="5390a-118">Структура [**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , эквивалентная **\_ средней структуре кспин** , используемой для драйверов потоковой передачи ядра, определяет носитель в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5390a-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="5390a-119">Элемент **клсмедиум** структуры **регпинмедиум** ЗАДАЕТ идентификатор класса (CLSID) для носителя.</span><span class="sxs-lookup"><span data-stu-id="5390a-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="5390a-120">Чтобы получить средний ПИН-код, вызовите метод [**икспин:: кскуеримедиумс**](ikspin-ksquerymediums.md) .</span><span class="sxs-lookup"><span data-stu-id="5390a-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="5390a-121">Этот метод возвращает указатель на блок памяти, содержащий структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) , за которой следует ноль или более структур **регпинмедиум** .</span><span class="sxs-lookup"><span data-stu-id="5390a-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="5390a-122">Каждая структура **регпинмедиум** определяет средний поддерживаемый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5390a-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="5390a-123">Не подключайте ПИН-код, если носитель имеет идентификатор CLSID \_ null или ксмедиумсетид \_ Standard.</span><span class="sxs-lookup"><span data-stu-id="5390a-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="5390a-124">Это значения по умолчанию, указывающие, что ПИН-код не поддерживает средние.</span><span class="sxs-lookup"><span data-stu-id="5390a-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="5390a-125">Кроме того, не подключайте ПИН-код, если только для фильтра не требуется ровно один подключенный экземпляр этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5390a-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="5390a-126">В противном случае приложение может попытаться подключить различные ПИН-коды, которые не должны иметь подключений, что может привести к зависанию программы.</span><span class="sxs-lookup"><span data-stu-id="5390a-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="5390a-127">Чтобы узнать количество требуемых экземпляров, извлеките значение свойства КСПРОПЕРТИ \_ PIN \_ нецессаринстанцес, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="5390a-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="5390a-128">(Для краткости в этом примере не выполняется проверка кодов возврата или освобождение интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="5390a-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="5390a-129">Конечно, приложение должно выполнять и то, и другое.)</span><span class="sxs-lookup"><span data-stu-id="5390a-129">Your application should do both, of course.)</span></span>


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



<span data-ttu-id="5390a-130">Следующий псевдокод является чрезвычайно кратким обзором, в котором показано, как найти и подключить фильтры WDM.</span><span class="sxs-lookup"><span data-stu-id="5390a-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="5390a-131">Он не содержит много сведений и предназначен только для того, чтобы продемонстрировать общие действия, которые необходимо выполнить приложению.</span><span class="sxs-lookup"><span data-stu-id="5390a-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a><span data-ttu-id="5390a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5390a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5390a-133">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="5390a-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



