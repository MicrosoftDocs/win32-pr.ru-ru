---
description: Фильтр сжатия AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Фильтр сжатия AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909472"
---
# <a name="avi-compressor-filter"></a>Фильтр сжатия AVI

Фильтр AVI Compression позволяет присоединить к графу фильтров кодеки (ВКМ). Каждый кодек отображается как отдельный экземпляр фильтра. Этот фильтр нельзя создать напрямую с помощью CoCreateInstance. Вместо этого необходимо использовать перечислитель системных устройств. Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).

Входной ПИН-код фильтра подключается к фильтрам, которые выводят несжатые видеоданные, такие как фильтры записи видео или [Фильтр AVI-разделителя](avi-splitter-filter.md). Закрепление вывода фильтра обычно подключается к фильтру МУЛЬТИПЛЕКСОРа, например [фильтру мультиплексора AVI](avi-mux-filter.md).

Если кодек поддерживает диалоговое окно настройки VFW старого стиля или диалоговое окно "о программе", приложение может отобразить его с помощью интерфейса [**иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> Программы сжатия MPEG никогда не реализуются как кодеки ВКМ, но только как собственные фильтры DirectShow.

 



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, испеЦифипропертипажес                                                                                                             |
| Типы носителей входных закрепления                    | \_Устройство MEDIATYPE, медиасубтипе \_ null                                                                                                                                                                                                               |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Типы носителей для выходного ПИН-кода                   | \_Устройство MEDIATYPE, медиасубтипе \_ null                                                                                                                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | Неприменимо                                                                                                                                                                                                                                     |
| CLSID страницы свойств                      | Нет страницы свойств.                                                                                                                                                                                                                                  |
| Исполняемый объект                               | qcap.dll                                                                                                                                                                                                                                           |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                                                                                                                |
| [Категория фильтра](filter-categories.md) | \_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



