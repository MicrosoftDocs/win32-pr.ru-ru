---
description: Объект Call создается, когда происходит вызов. Связанные интерфейсы получают и задают сведения, касающиеся вызова.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Вызов интерфейсов объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998610"
---
# <a name="call-object-interfaces"></a>Вызов интерфейсов объектов

[Объект call](call-object.md) создается, когда происходит вызов. Связанные интерфейсы получают и задают сведения, касающиеся вызова.

Интерфейсы перечислителя и событий не предоставляются напрямую в объекте Call, но перечислены здесь для удобства.

Интерфейсы [**иткаллнотификатионевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**иткаллинфочанжеевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent), [**иткаллстативент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent), [**Иткаллмедиаевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)и [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) не предоставляются напрямую в объекте Call, но тесно связаны с ним и перечислены здесь для удобства.



| Интерфейс                                                      | Описание                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Предоставляет сведения об объекте вызова, например о состоянии вызова или терминалах, используемых.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Расширяет [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) , предоставляя методы для установки фильтрации событий для каждого вызова.                    |
| [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Используется для подключения, ответа и выполнения базовых операций телефонии для объекта вызова.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Расширяет [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) , предоставляя методы для выбора терминала на вызов.              |
| [**иткаллнотификатионевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Интерфейс уведомления для [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**иткаллинфочанжеевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Интерфейс уведомления об изменениях в сведениях о вызовах.                                                                      |
| [**иткаллстативент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Возвращает сведения о событии вызова.                                                                                    |
| [**иткаллмедиаевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Возвращает сведения о событии вызова мультимедиа.                                                                              |
| [**иткустомтоне**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Предоставляет методы для управления пользовательскими тонами, возможными для некоторых наборов телефонов.                                                  |
| [**итдетекттоне**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Предоставляет методы для задания характеристик тона и тона, создающих события тона.                                    |
| [**итлегацикаллмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Поддерживает устаревшие приложения, которые должны напрямую взаимодействовать с устройством.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Расширяет [**итлегацикаллмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) , предоставляя методы для обнаружения и создания тонов. |
| [**иенумкалл**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Перечисляет [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



