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
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037124"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




