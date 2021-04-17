---
description: Класс Ксистемклокк реализует часы, возвращающие системное время.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Класс Ксистемклокк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559212"
---
# <a name="csystemclock-class"></a>Класс Ксистемклокк

![Иерархия классов ксистемклокк](images/sclock01.png)

`CSystemClock`Класс реализует часы, возвращающие системное время.

Этот класс является производным от класса [**кбасереференцеклокк**](cbasereferenceclock.md) и добавляет поддержку интерфейсов **IPersist** и [**иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .



| Открытые методы                                        | Описание                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Создает экземпляр этого объекта.              |
| [**ксистемклокк**](csystemclock-csystemclock.md)     | Метод конструктора.                                 |
| Методы Иамклоккаджуст                                | Описание                                         |
| [**сетклоккделта**](csystemclock-setclockdelta.md)   | Корректирует время.                             |
| Методы IPersist                                      | Описание                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Возвращает идентификатор класса (CLSID) объекта. |



 

 

 



