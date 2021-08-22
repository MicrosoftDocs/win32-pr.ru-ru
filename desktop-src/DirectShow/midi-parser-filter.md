---
description: Фильтр средства синтаксического анализа MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Фильтр средства синтаксического анализа MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256514"
---
# <a name="midi-parser-filter"></a>Фильтр средства синтаксического анализа MIDI

Фильтр средства синтаксического анализа MIDI считывает данные MIDI, найденные в. MID и. Файлы RMI. Фильтр принимает поток из источника [Async File](file-source--async--filter.md) или [файла URL-адреса](file-source--url--filter.md) , фильтрует и выводит примеры MIDI в модуль [**подготовки MIDI**](midi-renderer-filter.md) для воспроизведения.



| Метка | Значение |
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



 

## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе Модуль [**подготовки MIDI**](midi-renderer-filter.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



