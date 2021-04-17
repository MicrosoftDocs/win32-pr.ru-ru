---
description: Связывает имя группы и ее маркер.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Структура GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662178"
---
# <a name="groupinfo-structure"></a>Структура GROUPINFO

Структура **GROUPINFO** связывает имя группы и ее маркер.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**сзграупнаме**
</dt> <dd>

Увеличенное значение массива в структуре **GROUPNAME** .

</dd> <dt>

**hGroup**
</dt> <dd>

Обработчик для группы.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




