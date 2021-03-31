---
description: Фильтр записи звука
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Фильтр записи звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806593"
---
# <a name="audio-capture-filter"></a>Фильтр записи звука

Фильтр записи звука представляет устройство аудиозаписи. Он имеет один закрепление вывода и несколько входных ПИН-кодов (по одному для каждого типа входных данных на карточке, например строка в, микрофон, компакт-диск и MIDI).

Этот фильтр может работать с более чем одним аппаратным устройством, поэтому вызов CoCreateInstance для создания фильтра не работает. Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md). Перечислитель системных устройств Возвращает уникальный моникер для каждого устройства. Понятное имя моникера соответствует имени устройства. (Это имя отображается в Графедит.) Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**иамфилтермискфлагс**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**иамресаурцеконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, испеЦифипропертипажес                                                               |
| Типы носителей входных закрепления                    | MEDIATYPE \_ аналогаудио, медиасубтипе \_ null                                                                                                                                                                                                                                                         |
| Интерфейсы входных закрепления                     | [**Иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Типы носителей для выходного ПИН-кода                   | MEDIATYPE \_ Audio, медиасубтипе \_ null                                                                                                                                                                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**Иамбуффернеготиатион**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**иампушсаурце**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**икспропертисет**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | Неприменимо                                                                                                                                                                                                                                                                                     |
| CLSID страницы свойств                      | \_АУДИОИНПУТМИКСЕРПРОПЕРТИЕС CLSID                                                                                                                                                                                                                                                                   |
| Исполняемый объект                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                                                                                                                                                                |
| [Категория фильтра](filter-categories.md) | \_АУДИОИНПУТДЕВИЦЕКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Комментарии

Входные сигналы представляют собой физические подключения оборудования и никогда не подключаются к другим фильтрам в DirectShow.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Запись звука](audio-capture.md)
</dt> </dl>

 

 



