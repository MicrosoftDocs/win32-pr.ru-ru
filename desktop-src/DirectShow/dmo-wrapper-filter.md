---
description: DMO Фильтр оболочки
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO Фильтр оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13383e7539f478327f1a904d60fcd069692180239e76bcfd48bcc090a068e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653044"
---
# <a name="dmo-wrapper-filter"></a>DMO Фильтр оболочки

фильтр оболочки DMO позволяет приложению DirectShow использовать [объект мультимедиа DirectX](directx-media-objects.md) (DMO) в графе фильтра. фильтр создает оболочку для DMO и обрабатывает все сведения об использовании DMO, например передачу данных в DMO и обратно. кроме того, фильтр объединяет DMO, поэтому приложение может запрашивать фильтр для любых COM-интерфейсов, предоставляемых DMO.



| Метка | Значение |
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



 

## <a name="remarks"></a>Remarks

### <a name="limitations"></a>Ограничения

оболочка DMO имеет следующие ограничения.

-   Он не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами. (Он поддерживает дмос с одним входом и несколькими выходами.)
-   Он не поддерживает пользовательские транспорты. Все данные транспортного уровня выполняются через интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Он не использует интерфейс **имедиаобжектинплаце** ; все операции обработки выполняются с помощью методов [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Маркеры

для каждого входного потока на DMO фильтр создает соответствующий входной пин-код. Для каждого выходного потока создается соответствующий выходной ПИН-код. Типы носителей, поддерживаемые каждым ПИН-кодом, зависят от DMO

### <a name="encoder-interfaces"></a>Интерфейсы кодировщика

если DMO является видеокодировщиком или звуковым кодировщиком, закрепление вывода предоставляет интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . если DMO является видеокодировщиком, закрепление вывода также предоставляет интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . в обоих случаях, если DMO поддерживает интерфейс, пин-код делегирует DMO. В противном случае ПИН-код предоставляет собственную реализацию.

### <a name="streaming"></a>Потоковая передача

Фильтр использует интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) для управления всей потоковой передачей. Он не поддерживает подключения [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . фильтр вызывает [**имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) в DMO только при получении данных из вышестоящего источника (включая уведомления в конце потока). Поэтому он не поддерживает дмос с нулевым числом входных потоков.

### <a name="seeking"></a>Нужна

все запросы поиска передаются в вышестоящий фильтр через первый входной пин-код в оболочке DMO. Для дмос нескольких выходных данных это означает, что вышестоящий фильтр может получить несколько запросов поиска при поиске приложением графа.

### <a name="merit"></a>Заслуживают

DirectShow присваивает всем дмос значение по умолчанию «неполный **» + « \_** 0x800». Это значение находится между **\_ нормальным** и **\_ невысоким приоритетом**. Фильтры декодера обычно имеют значение " **\_ нормально**". таким образом, диспетчер графов фильтров обычно выбирает DMO декодера для фильтра декодера. чтобы переопределить значение по умолчанию, добавьте запись реестра в раздел реестра DMO в \_ \_ корневой CLSID классов HKEY \\ . Включите значение **DWORD** с именем «заслуживает», значение которого указывает на неуспешный выбор.

### <a name="category"></a>Категория

фильтр оболочки DMO не отображается ни в одной категории. когда она создает оболочку для DMO, она отображается в категории DirectShow, соответствующей категории DMO, под именем DMO.

### <a name="buffers"></a>Буферы

фильтр оболочки DMO передает буферы мультимедиа в DMO, которые предоставляют интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

в Windows Vista и более поздних версиях буферы мультимедиа также предоставляют интерфейс IServiceProvider. DMO может использовать этот интерфейс для получения указателя на пример носителя, связанного с буфером. Используйте идентификатор службы **IID \_ имедиасампле**. видео-DMO может использовать интерфейс [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) примера мультимедиа для установки флагов чересстрочную развертки в образце. В следующем коде показано, как получить указатель на пример мультимедиа:


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

если DMO предоставляет интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , фильтр преобразует вызовы [**икуалитиконтрол:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) для его выходного пин-кода в вызовы [**идмокуалитиконтрол:: сетнов**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) в DMO. Параметр *ртнов* объекта **сетнов** вычисляется как сумма **метки времени** и **последних** элементов структуры [**качества**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Использование фильтровать в Графедит

в графедит фильтр оболочки DMO не отображается под собственным именем. вместо этого все зарегистрированные DMO перечислены под соответствующей категорией фильтра. при добавлении DMO с помощью диалогового окна " **вставить фильтры** " графедит создает фильтр оболочки DMO и настраивает его для использования DMO.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Объекты мультимедиа DirectX](directx-media-objects.md)
</dt> </dl>

 

 
