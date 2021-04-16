---
description: Свойство Property объекта Session является свойством для чтения и записи, представляющим строковое значение именованного свойства установщика, которое поддерживается объектом Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Свойство Session. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679940"
---
# <a name="sessionproperty-property"></a>Свойство Session. Property

Свойство **Property** объекта [**Session**](session-object.md) — это свойство, доступное для чтения и записи, которое представляет строковое значение именованного свойства установщика, которое поддерживается объектом **Session** в таблице свойств в памяти, или значение, если в качестве префикса используется знак процента (%), значением системной переменной среды для текущего процесса. Может быть указано либо строковое, либо целочисленное значение. Несуществующее свойство или переменная среды эквивалентны ее значению NULL.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Значение свойства

Обязательное имя свойства с учетом регистра или имя переменной среды без учета регистра с префиксом процента (%).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




