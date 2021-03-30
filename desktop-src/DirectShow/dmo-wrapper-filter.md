---
description: Фильтр оболочки DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Фильтр оболочки DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b01ee006203e2e1fd328bacc13c01de4a3b25f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495579"
---
# <a name="dmo-wrapper-filter"></a>Фильтр оболочки DMO

Фильтр оболочки DMO позволяет приложению DirectShow использовать [объект мультимедиа DirectX](directx-media-objects.md) (DMO) в графе фильтра. Фильтр создает оболочку DMO и обрабатывает все детали использования DMO, например передачу данных в DMO и обратно. Кроме того, фильтр объединяет DMO, поэтому приложение может запросить фильтр для любых COM-интерфейсов, предоставляемых DMO.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Типы носителей входных закрепления                    | См. примечания                                                                                                                                                                                                                                        |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Типы носителей для выходного ПИН-кода                   | См. примечания                                                                                                                                                                                                                                        |
| Интерфейсы выходного ПИН-кода                    | [**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | \_ДМОВРАППЕРФИЛТЕР CLSID                                                                                                                                                                                                                            |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                                                                                                                                   |
| Исполняемый объект                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Заслуживают](merit.md)                       | См. примечания                                                                                                                                                                                                                                        |
| [Категория фильтра](filter-categories.md) | См. примечания                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Комментарии

### <a name="limitations"></a>Ограничения

Оболочка DMO имеет следующие ограничения.

-   Он не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами. (Он поддерживает дмос с одним входом и несколькими выходами.)
-   Он не поддерживает пользовательские транспорты. Все данные транспортного уровня выполняются через интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Он не использует интерфейс **имедиаобжектинплаце** ; все операции обработки выполняются с помощью методов [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Маркеры

Для каждого входного потока в DMO фильтр создает соответствующий входной ПИН-код. Для каждого выходного потока создается соответствующий выходной ПИН-код. Типы носителей, поддерживаемые каждым ПИН-кодом, зависят от DMO

### <a name="encoder-interfaces"></a>Интерфейсы кодировщика

Если DMO является видеокодировщиком или звуковым кодировщиком, закрепление вывода предоставляет интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . Если DMO является видеокодировщиком, закрепление вывода также предоставляет интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . В обоих случаях, если DMO поддерживает интерфейс, ПИН-код делегирует объект DMO. В противном случае ПИН-код предоставляет собственную реализацию.

### <a name="streaming"></a>Потоковая передача

Фильтр использует интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) для управления всей потоковой передачей. Он не поддерживает подключения [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Фильтр вызывает [**имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) на DMO только при получении данных из вышестоящего (включая уведомления в виде конца потока). Поэтому он не поддерживает дмос с нулевым числом входных потоков.

### <a name="seeking"></a>Нужна

Все запросы поиска передаются в вышестоящий фильтр через первый входной ПИН-код в оболочке DMO. Для дмос нескольких выходных данных это означает, что вышестоящий фильтр может получить несколько запросов поиска при поиске приложением графа.

### <a name="merit"></a>Заслуживают

DirectShow назначает всем дмос значение по умолчанию «неполный **» + « \_** 0x800». Это значение находится между **\_ нормальным** и **\_ невысоким приоритетом**. Фильтры декодера обычно имеют значение " **\_ нормально**". Таким образом, диспетчер графов фильтров обычно выбирает декодер DMO для фильтра декодера. Чтобы переопределить значение по умолчанию, добавьте запись реестра в раздел реестра DMO в \_ \_ корневом CLSID классов hKey \\ . Включите значение **DWORD** с именем «заслуживает», значение которого указывает на неуспешный выбор.

### <a name="category"></a>Категория

Фильтр оболочки DMO не отображается ни в одной категории. При создании оболочки DMO она отображается в категории DirectShow, соответствующей категории DMO, под именем DMO.

### <a name="buffers"></a>Буферы

Фильтр оболочки DMO передает буферы мультимедиа в DMO, которые предоставляют интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

В Windows Vista и более поздних версиях буферы мультимедиа также предоставляют интерфейс IServiceProvider. DMO может использовать этот интерфейс для получения указателя на пример носителя, связанного с буфером. Используйте идентификатор службы **IID \_ имедиасампле**. Видео DMO может использовать интерфейс [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) примера мультимедиа для установки флагов чересстрочную развертки в образце. В следующем коде показано, как получить указатель на пример мультимедиа:


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Дополнительные сведения о параметрах чересстрочную развертки для каждого образца см. в разделе [**\_ SAMPLE2 \_ Properties Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Контроль качества

Если объекты DMO предоставляют интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , то фильтр преобразует вызовы [**Икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) для своего выходного контакта в [**идмокуалитиконтрол:: сетнов**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) вызовы в DMO. Параметр *ртнов* объекта **сетнов** вычисляется как сумма **метки времени** и **последних** элементов структуры [**качества**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Использование фильтровать в Графедит

В Графедит фильтр оболочки DMO не отображается под собственным именем. Вместо этого каждый зарегистрированный объект DMO отображается под соответствующей категорией фильтра. При добавлении DMO с помощью диалогового окна " **Вставить фильтры** " графедит создает фильтр оболочки DMO и настраивает его для использования этого DMO.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Объекты мультимедиа DirectX](directx-media-objects.md)
</dt> </dl>

 

 
