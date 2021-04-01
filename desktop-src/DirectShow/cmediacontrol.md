---
description: Класс Кмедиаконтрол обеспечивает обработку базового класса для методов IDispatch сдвоенного интерфейса Имедиаконтрол. Он оставляет чисто виртуальные свойства и методы интерфейса Имедиаконтрол.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Класс Кмедиаконтрол
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914212"
---
# <a name="cmediacontrol-class"></a>Класс Кмедиаконтрол

![Иерархия классов кмедиаконтрол](images/cutil02.png)

`CMediaControl`Класс обеспечивает обработку базового класса для методов [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) сдвоенного интерфейса [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol). Он оставляет чисто виртуальные свойства и методы интерфейса **имедиаконтрол** .

Как правило, диспетчер графа фильтров является единственным объектом, реализующим интерфейс [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) . (фильтры реализуют интерфейс [**имедиафилтер**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , наследуемый [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), для получения управляющих команд из диспетчера графа фильтров.) Поэтому эта библиотека классов ограничена использованием для фильтрации разработчиков.

Функции-члены [**кмедиаконтрол:: GetIdsOfNames**](cmediacontrol-getidsofnames.md), [**Кмедиаконтрол:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**Кмедиаконтрол:: Жеттипеинфокаунт**](cmediacontrol-gettypeinfocount.md)и [**кмедиаконтрол:: Invoke**](cmediacontrol-invoke.md) являются стандартными реализациями методов [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) с помощью класса [**кбаседиспатч**](cbasedispatch.md) (и библиотеки типов) для анализа команд и передачи их в чистые виртуальные методы интерфейса [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .

Методы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) , определенные в Control. ODL, остаются нечистыми виртуальными.



| Функции элементов                                           | Описание                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**кмедиаконтрол**](cmediacontrol-cmediacontrol.md)       | Конструирует объект **кмедиаконтрол** .                                                                                                                                                                                                  |
| Методы IDispatch                                          | Описание                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Сопоставляет один элемент и необязательный набор параметров с соответствующим набором целочисленных идентификаторов диспетчеризации (DISPID), которые могут использоваться при последующих вызовах метода [**кмедиаконтрол:: Invoke**](cmediacontrol-invoke.md) . |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Извлекает объект сведений о типе, который может получить сведения о типе для интерфейса.                                                                                                                                          |
| [**жеттипеинфокаунт**](cmediacontrol-gettypeinfocount.md) | Извлекает количество интерфейсов типа данных, предоставленных объектом.                                                                                                                                                              |
| [**Вызвать**](cmediacontrol-invoke.md)                     | Предоставляет доступ к открытым свойствам и методам объекта.                                                                                                                                                                         |



 

 

 
