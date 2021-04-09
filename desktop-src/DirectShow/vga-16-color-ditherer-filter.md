---
description: Фильтр VGA 16 с оттенокм
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Фильтр VGA 16 с оттенокм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081083"
---
# <a name="vga-16-color-ditherer-filter"></a>Фильтр VGA 16 с оттенокм

Фильтр VGA 16, отменяющий цвет, выполняет преобразование из типа цвета RGB в 4-разрядный цвет, чтобы видеопотоки AVI и MPEG могли отображаться на старых 16 цветных мониторах. Этот фильтр вставляется в граф между фильтром декомпрессора и фильтром модуля подготовки видео.



|                                          |                                                                                                                                                    |
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



