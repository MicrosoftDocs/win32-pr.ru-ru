---
description: Класс Ктрансинплацеинпутпин реализует входной ПИН-код, используемый классом Ктрансинплацефилтер.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Класс Ктрансинплацеинпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675156"
---
# <a name="ctransinplaceinputpin-class"></a>Класс Ктрансинплацеинпутпин

![Иерархия классов ктрансинплацеинпутпин](images/tsip01.png)

`CTransInPlaceInputPin`Класс реализует входной ПИН-код, используемый классом [**ктрансинплацефилтер**](ctransinplacefilter.md) .

Как правило, наследование от этого класса не требуется. В этом случае необходимо переопределить метод [**ктрансинплацефилтер:: жетпин**](ctransinplacefilter-getpin.md) фильтра, чтобы создать экземпляры производного класса.



| Защищенные переменные членов                                                          | Описание                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ бреадонли**](ctransinplaceinputpin-m-breadonly.md)                           | Флаг, указывающий, доступен ли входной поток только для чтения. |
| [**m \_ птипфилтер**](ctransinplaceinputpin-m-ptipfilter.md)                         | Указатель на фильтр, создавший этот ПИН-код.               |
| Открытые методы                                                                      | Описание                                                |
| [**ктрансинплацеинпутпин**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Метод конструктора.                                        |
| [**чеккмедиатипе**](ctransinplaceinputpin-checkmediatype.md)                      | Определяет, принимает ли ПИН-код конкретный тип носителя.       |
| [**пикаллокатор**](ctransinplaceinputpin-peekallocator.md)                        | Получает указатель на распределитель контакта.                |
| [**Доступно**](ctransinplaceinputpin-readonly.md)                                  | Указывает, доступен ли входной поток только для чтения.           |
| Методы Ипин                                                                        | Описание                                                |
| [**енуммедиатипес**](ctransinplaceinputpin-enummediatypes.md)                      | Перечисляет предпочтительные типы носителей для ПИН-кода.                |
| Методы Имеминпутпин                                                                | Описание                                                |
| [**Распределителя**](ctransinplaceinputpin-getallocator.md)                          | Извлекает распределитель памяти, предложенный этим ПИН-кодом.       |
| [**нотифяллокатор**](ctransinplaceinputpin-notifyallocator.md)                    | Указывает распределитель для соединения.                 |
| [**жеталлокаторрекуирементс**](ctransinplaceinputpin--getallocatorrequirements.md) | Извлекает свойства распределителя, запрошенные ПИН-кодом.   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




