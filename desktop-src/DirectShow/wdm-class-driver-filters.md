---
description: Фильтры драйвера класса WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Фильтры драйвера класса WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd93db09c638ed7a8a217bec28a565086dcbfcae2b5702c9e1d07778c338646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071898"
---
# <a name="wdm-class-driver-filters"></a>Фильтры драйвера класса WDM

если устройство записи использует драйвер WDM (WDM), для диаграммы могут потребоваться определенные фильтры из фильтра записи. Эти фильтры называются фильтрами драйверов потокового класса или фильтрами WDM. Они поддерживают дополнительные функции, предоставляемые оборудованием. Например, плата ТВ-тюнера имеет функции для настройки канала. Соответствующий фильтр — это фильтр [ТВ-тюнера](tv-tuner-filter.md) , который предоставляет интерфейс [**иамтвтунер**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . Чтобы сделать эту функцию доступной для приложения, необходимо подключить фильтр ТВ-тюнера к фильтру записи.

Интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) предоставляет самый простой способ добавления фильтров WDM в граф. В некоторый момент при построении графа вызовите [**финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) или [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Любой из этих методов автоматически обнаружит необходимые фильтры WDM и подключится к фильтру записи. В оставшейся части этого раздела описано, как добавить фильтры WDM вручную. Однако следует иметь в виду, что рекомендуемый подход просто вызывает один из этих методов **ICaptureGraphBuilder2** .

ПИН-коды в фильтре WDM поддерживают один или несколько средних. Средний уровень определяет способ связи, например шину. Необходимо подключить ПИН-коды, поддерживающие один и тот же носитель. Структура [**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , эквивалентная **\_ средней структуре кспин** , используемой для драйверов потоковой передачи ядра, определяет носитель в DirectShow. Элемент **клсмедиум** структуры **регпинмедиум** ЗАДАЕТ идентификатор класса (CLSID) для носителя. Чтобы получить средний ПИН-код, вызовите метод [**икспин:: кскуеримедиумс**](ikspin-ksquerymediums.md) . Этот метод возвращает указатель на блок памяти, содержащий структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) , за которой следует ноль или более структур **регпинмедиум** . Каждая структура **регпинмедиум** определяет средний поддерживаемый ПИН-код.

Не подключайте ПИН-код, если носитель имеет идентификатор CLSID \_ null или ксмедиумсетид \_ Standard. Это значения по умолчанию, указывающие, что ПИН-код не поддерживает средние.

Кроме того, не подключайте ПИН-код, если только для фильтра не требуется ровно один подключенный экземпляр этого ПИН-кода. В противном случае приложение может попытаться подключить различные ПИН-коды, которые не должны иметь подключений, что может привести к зависанию программы. Чтобы узнать количество требуемых экземпляров, извлеките значение свойства КСПРОПЕРТИ \_ PIN \_ нецессаринстанцес, как показано в следующем примере кода. (Для краткости в этом примере не выполняется проверка кодов возврата или освобождение интерфейсов. Конечно, приложение должно выполнять и то, и другое.)


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



Следующий псевдокод является чрезвычайно кратким обзором, в котором показано, как найти и подключить фильтры WDM. Он не содержит много сведений и предназначен только для того, чтобы продемонстрировать общие действия, которые необходимо выполнить приложению.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> </dl>

 

 



