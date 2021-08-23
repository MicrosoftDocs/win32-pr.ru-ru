---
description: Атрибуты событий
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Атрибуты событий (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600514"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Атрибуты событий (Microsoft Media Foundation)

Следующие атрибуты применяются к событиям.



| attribute                                                                                                        | Описание                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_событие MF \_ — \_ сужение**](mf-event-do-thinning-attribute.md)                                                | Когда источник мультимедиа запрашивает новый уровень воспроизведения, указывает, запрашивается ли нетонкое воспроизведение источника.                |
| [**\_ \_ узел вывода событий \_ MF**](mf-event-output-node-attribute.md)                                                | Определяет узел топологии для приемника потока.                                                                       |
| [**\_ \_ \_ смещение времени презентации событий \_ MF**](mf-event-presentation-time-offset-attribute.md)                     | Смещение между временем презентации и штампами времени источника мультимедиа.                                              |
| [**\_ \_ время СКРУБСАМПЛЕ события \_ MF**](mf-event-scrubsample-time-attribute.md)                                      | Время презентации для примера, отображаемого во время очистки.                                                     |
| [**\_сессионкапс событий \_ MF**](mf-event-sessioncaps-attribute.md)                                                 | Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.                  |
| [**\_Дельта событий MF \_ сессионкапс \_**](mf-event-sessioncaps-delta-attribute.md)                                    | Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации. |
| [**\_ \_ \_ Фактическое начало источника события MF \_**](mf-event-source-actual-start-attribute.md)                               | Содержит время начала, когда источник мультимедиа перезапускается с текущей позицией.                                       |
| [**\_ \_ характеристики источника события \_ MF**](mf-event-source-characteristics-attribute.md)                          | Задает текущие характеристики источника мультимедиа.                                                            |
| [**\_ \_ \_ старые характеристики источника события \_ MF**](mf-event-source-characteristics-old-attribute.md)                 | Задает предыдущие характеристики источника мультимедиа.                                                           |
| [**\_ \_ \_ поддельный \_ Запуск источника события MF**](mf-event-source-fake-start-attribute.md)                                   | Указывает, пуста ли текущая топология сегмента.                                                              |
| [**\_ \_ прожектстарт источник события \_ MF**](mf-event-source-projectstart-attribute.md)                                | Указывает время начала для топологии сегмента.                                                                      |
| [**\_ \_ топология источника событий MF \_ \_ отменена**](mf-event-source-topology-canceled-attribute.md)                     | Указывает, отменила ли источник Sequencer топологию.                                                           |
| [**\_ \_ \_ время начала презентации \_ для события MF**](mf-event-start-presentation-time-attribute.md)                       | Время начала презентации в единицах измерения 100-наносекундных, измеряемое часами представления.               |
| [**\_событие MF \_ Запуск \_ \_ во время презентации \_ на \_ выходе**](mf-event-start-presentation-time-at-output-attribute.md) | Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.                      |
| [**\_ \_ состояние ТОПОЛОГИИ событий \_ MF**](mf-event-topology-status-attribute.md)                                        | Указывает состояние топологии во время воспроизведения.                                                                   |
| [**\_время сеанса MF, \_ около \_ \_ времени возникновения события \_**](mf-session-approx-event-occurrence-time-attribute.md)        | Приблизительное время, когда сеанс мультимедиа вызвал событие.                                                          |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



