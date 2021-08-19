---
title: Свойства (IInertiaProcessor)
description: Этот раздел содержит свойства интерфейса IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Сенсорный ввод, интерфейс IInertiaProcessor
- Windows Сенсорный ввод, свойства интерфейса
- инерция, интерфейс IInertiaProcessor
- Интерфейс IInertiaProcessor, свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7825a97545c897f402144ce5113b79650b9eba31e19da7ceef1459ae6cdc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030128"
---
# <a name="properties-iinertiaprocessor"></a>Свойства (IInertiaProcessor)

Этот раздел содержит свойства интерфейса [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Свойство                                                                               | Описание                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**инитиалоригинкс**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Задает начальное расположение целевого объекта с помощью интертиа.                                   |
| [**инитиалоригини**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Задает начальное вертикальное расположение для целевого объекта с помощью интертиа.                                     |
| [**инитиалвелоЦитикс**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Задает начальное перемещение целевого объекта по горизонтальной оси.                              |
| [**инитиалвелоЦитии**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Задает начальное перемещение целевого объекта по вертикальной оси.                                |
| [**инитиалангуларвелоЦити**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Задает скорость вращения целевого объекта при начале перемещения.                                    |
| [**инитиалекспансионвелоЦити**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Указывает частоту расширения RADIUS для целевого объекта при начале перемещения.                               |
| [**инитиалрадиус**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Задает расстояние от края целевого объекта до его центра перед изменением объекта.          |
| [**баундарилефт**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Ограничивает расстояние до левого края экрана, в котором может перемещаться целевой объект.                                 |
| [**баундаритоп**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Ограничивает расстояние в верхней части экрана, на которое может перемещаться целевой объект.                                  |
| [**баундариригхт**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Ограничивает расстояние в правой части экрана, на которое может перемещаться целевой объект.                           |
| [**баундариботтом**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Ограничивает расстояние в нижней части экрана, на которое может перемещаться целевой объект.                               |
| [**еластикмаргинлефт**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Задает крайний левый регион для возврата целевого объекта.                                            |
| [**еластикмаргинтоп**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Задает верхний регион для возврата целевого объекта.                                             |
| [**еластикмаргинригхт**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Задает крайний правый регион для возврата целевого объекта.                                           |
| [**еластикмаргинботтом**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Задает нижнюю область для возврата целевого объекта.                                              |
| [**десиредангулардецелератион**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Указывает желаемую скорость, с которой целевой объект будет останавливаться в радианах на МС.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Указывает нужное расстояние (в радианах), которое объект будет манипулировать обработчиком инерции. |
| [**десиредекспансион**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Указывает требуемое изменение среднего радиуса объекта.                                        |
| [**десиредекспансиондецелератион**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Указывает скорость, с которой объект будет останавливаться.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Указывает желаемую скорость, с которой операции преобразования будут замедлены.                              |
| [**десиреддисплацемент**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Указывает нужное расстояние, которое объект будет перемещать.                                              |
| [**инитиалтиместамп**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Задает начальную метку времени для целевого объекта, который имеет инерцию.                                  |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




