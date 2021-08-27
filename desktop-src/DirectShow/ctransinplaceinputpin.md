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
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076203"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




