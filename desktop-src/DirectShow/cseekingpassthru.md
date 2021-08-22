---
description: Класс Ксикингпасссру — это вспомогательный объект, создающий объекты Кпоспасссру и Крендерерпоспасссру.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Класс Ксикингпасссру (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ffb8436623cb5ba5f415ceb8bbdafe00e22487da2bbfaba5d02ee4c8f189c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953773"
---
# <a name="cseekingpassthru-class"></a>Класс Ксикингпасссру

`CSeekingPassThru`Класс является вспомогательным объектом, который создает объекты [**Кпоспасссру**](cpospassthru.md) и [**крендерерпоспасссру**](crendererpospassthru.md) .

Классы **кпоспасссру** и **крендерерпоспасссру** являются вспомогательными объектами, которые передают команды поиска в виде вышестоящего, поэтому `CSeekingPassThru` класс является вспомогательным объектом для создания вспомогательных объектов.

Необязательно использовать этот класс напрямую. Вместо этого используйте функцию [**креатепоспасссру**](createpospassthru.md) , которая обрабатывает все сведения об использовании этого класса. Он имеет больше преимуществ при загрузке объекта из Quartz.dll, что немного сокращает размер кода фильтра. Дополнительные сведения см. в разделе [**кпоспасссру**](cpospassthru.md).

`CSeekingPassThru`Класс предоставляет интерфейс [**исикингпасссру**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) . Метод [**исикингпасссру:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Инициализирует объект. После инициализации объекта фильтр может запросить его для интерфейсов [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) и [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) .



| Открытые методы                                                  | Описание                        |
|-----------------------------------------------------------------|------------------------------------|
| [**ксикингпасссру**](cseekingpassthru-cseekingpassthru.md)   | Метод конструктора.                |
| [**~ Ксикингпасссру**](cseekingpassthru--cseekingpassthru.md) | Метод деструктора.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Создает экземпляр объекта. |
| Методы Исикингпасссру                                        | Описание                        |
| [**Init**](cseekingpassthru-init.md)                           | Инициализирует объект.            |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>сикпт. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




