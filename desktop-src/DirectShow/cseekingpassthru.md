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
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685118"
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
| [**Ini**](cseekingpassthru-init.md)                           | Инициализирует объект.            |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Сикпт. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




