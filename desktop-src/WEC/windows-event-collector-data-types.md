---
title: Типы данных сборщика событий Windows (Евколл. h)
description: Типы данных для сборщика событий Windows используются как типы переменных объектов подписки на события, типы параметров функций и типы возвращаемых функций.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691759"
---
# <a name="windows-event-collector-data-types"></a>Типы данных сборщика событий Windows

Типы данных для сборщика событий Windows используются как типы переменных объектов подписки на события, типы параметров функций и типы возвращаемых функций.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_маркер EC**
</dt> <dd>

Обработчик для объекта подписки. Используется для представления подписки сборщика событий.

</dd> <dt>

**\_ \_ \_ маркер свойства массива объектов \_ EC**
</dt> <dd>

Обработайте массив значений свойств для источников событий подписки. Этот маркер массива возвращается методом [**екжетсубскриптионпроперти**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) , когда значение **ексубскриптионевентсаурцес** передается в параметр *PropertyId* .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Евколл. h</dt> </dl> |



 

 





