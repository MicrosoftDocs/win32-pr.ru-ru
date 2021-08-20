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
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076162"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




