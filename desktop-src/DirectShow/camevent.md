---
description: Класс Камевент является оболочкой для событий ручного сброса и автоматического сброса.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Класс Камевент (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665432"
---
# <a name="camevent-class"></a>Класс Камевент

![Иерархия классов камевент](images/util06.png)

Класс **камевент** является оболочкой для событий ручного сброса и автоматического сброса.

Этот класс предоставляет удобный способ управления событиями вместо вызова таких функций, как [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)и [**ресетевент**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Защищенные переменные членов                          | Описание                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ Хевент**](camevent-m-hevent.md)              | Обработчик событий.                                                   |
| Открытые методы                                      | Описание                                                     |
| [**камевент**](camevent-camevent.md)               | Метод конструктора.                                             |
| [**~ Камевент**](camevent--camevent.md)             | Метод деструктора.                                              |
| [**службы "Функции Azure"**](camevent-check.md)                     | Проверяет, задано ли событие, без блокировки.              |
| [**Перезапуск**](camevent-reset.md)                     | Задает несигнальное состояние события.                     |
| [**Параметр**](camevent-set.md)                         | Сигнализирует о событии.                                              |
| [**Ожидание**](camevent-wait.md)                       | Блокируется до получения сигнала о событии или до истечения времени ожидания. |
| Операторы                                           | Описание:                                                     |
| [**МАРКЕР оператора**](camevent-operator-handle.md) | Получает маркер события.                                     |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

