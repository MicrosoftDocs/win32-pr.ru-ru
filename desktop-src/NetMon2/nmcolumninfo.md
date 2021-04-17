---
description: Структура НМКОЛУМНИНФО определяет один столбец в верхней области Просмотр событий.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Структура НМКОЛУМНИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684540"
---
# <a name="nmcolumninfo-structure"></a>Структура НМКОЛУМНИНФО

Структура **нмколумнинфо** определяет один столбец в верхней области Просмотр событий.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**сзколумннаме**
</dt> <dd>

Отображаемое имя определенного столбца. Если имя слишком длинное, оно не будет полностью видимо в конфигурации Просмотр событий по умолчанию.

</dd> <dt>

**вариантдата**
</dt> <dd>

Данные, вставленные в столбец.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




