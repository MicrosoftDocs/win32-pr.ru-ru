---
description: Фильтр средства синтаксического анализа MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Фильтр средства синтаксического анализа MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989920"
---
# <a name="midi-parser-filter"></a>Фильтр средства синтаксического анализа MIDI

Фильтр средства синтаксического анализа MIDI считывает данные MIDI, найденные в. MID и. Файлы RMI. Фильтр принимает поток из источника [Async File](file-source--async--filter.md) или [файла URL-адреса](file-source--url--filter.md) , фильтрует и выводит примеры MIDI в модуль [**подготовки MIDI**](midi-renderer-filter.md) для воспроизведения.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Типы носителей входных закрепления                    | \_Поток MEDIATYPE, медиасубтипе \_ MIDI                                                                    |
| Интерфейсы входных закрепления                     | [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Типы носителей для выходного ПИН-кода                   | MEDIATYPE \_ MIDI, медиасубтипе \_ null                                                                      |
| Интерфейсы выходного ПИН-кода                    | [**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Фильтровать CLSID                             | \_МИДИПАРСЕР CLSID                                                                                        |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                         |
| Исполняемый объект                               | quartz.dll                                                                                               |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                          |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                            |



 

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе Модуль [**подготовки MIDI**](midi-renderer-filter.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



