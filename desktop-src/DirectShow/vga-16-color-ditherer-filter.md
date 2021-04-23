---
description: Фильтр VGA 16 с оттенокм
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Фильтр VGA 16 с оттенокм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908682"
---
# <a name="vga-16-color-ditherer-filter"></a>Фильтр VGA 16 с оттенокм

Фильтр VGA 16, отменяющий цвет, выполняет преобразование из типа цвета RGB в 4-разрядный цвет, чтобы видеопотоки AVI и MPEG могли отображаться на старых 16 цветных мониторах. Этот фильтр вставляется в граф между фильтром декомпрессора и фильтром модуля подготовки видео.



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Типы носителей входных закрепления                    | МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB8                                                                                                               |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Типы носителей для выходного ПИН-кода                   | МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB4                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | \_ДИЗЕРИНГ CLSID                                                                                                                                      |
| CLSID страницы свойств                      | Нет страницы свойств.                                                                                                                                  |
| Исполняемый объект                               | quartz.dll                                                                                                                                         |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                                                                    |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



