---
description: Класс Ктрансинплацеаутпутпин реализует выходной ПИН-код, который используется классом Ктрансинплацефилтер.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Класс Ктрансинплацеаутпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675144"
---
# <a name="ctransinplaceoutputpin-class"></a>Класс Ктрансинплацеаутпутпин

![Иерархия классов ктрансинплацеаутпутпин](images/tsip02.png)

`CTransInPlaceOutputPin`Класс реализует выходной ПИН-код, используемый классом [**ктрансинплацефилтер**](ctransinplacefilter.md) .

Как правило, наследование от этого класса не требуется. В этом случае необходимо переопределить метод [**ктрансинплацефилтер:: жетпин**](ctransinplacefilter-getpin.md) фильтра, чтобы создать экземпляры производного класса.



| Защищенные переменные членов                                                      | Описание                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ птипфилтер**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Указатель на фильтр, создавший этот ПИН-код.         |
| Открытые методы                                                                  | Описание                                          |
| [**ктрансинплацеаутпутпин**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Метод конструктора.                                  |
| [**чеккмедиатипе**](ctransinplaceoutputpin-checkmediatype.md)                 | Определяет, принимает ли ПИН-код конкретный тип носителя. |
| [**сеталлокатор**](ctransinplaceoutputpin-setallocator.md)                     | Указывает распределитель для соединения.           |
| [**коннектедимеминпутпин**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Получает указатель на нисходящий входной ПИН-код.     |
| [**пикаллокатор**](ctransinplaceoutputpin-peekallocator.md)                   | Получает указатель на распределитель контакта.          |
| Методы Ипин                                                                    | Описание                                          |
| [**енуммедиатипес**](ctransinplaceoutputpin-enummediatypes.md)                 | Перечисляет предпочтительные типы носителей для ПИН-кода.          |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




