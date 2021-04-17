---
description: Структура ПРОПЕРТИНСТЕКС определяет экземпляр расширенного свойства с полилинией.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Структура ПРОПЕРТИНСТЕКС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673235"
---
# <a name="propertyinstex-structure"></a>Структура ПРОПЕРТИНСТЕКС

Структура **пропертинстекс** определяет экземпляр расширенного свойства с полилинией.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Члены

<dl> <dt>

**Длина**
</dt> <dd>

Длина данных в байтах.

</dd> <dt>

**ленгсекс**
</dt> <dd>

Длина расширенных данных.

</dd> <dt>

**лпдата**
</dt> <dd>

Указатель на Расширенные данные.

</dd> <dt>

**Byte**
</dt> <dd>

Указатель на **байтовые** данные.

</dd> <dt>

**Word**
</dt> <dd>

Указатель на данные **слова** .

</dd> <dt>

**DWORD**
</dt> <dd>

Указатель на данные **DWORD** .

</dd> <dt>

**ларжеинт**
</dt> <dd>

Указатель на данные **ларжеинт** .

</dd> <dt>

**систиме**
</dt> <dd>

Указатель на данные **SYSTEMTIME** .

</dd> <dt>

**типедстринг**
</dt> <dd>

Типизированная строка, которая может иметь Расширенные данные.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




