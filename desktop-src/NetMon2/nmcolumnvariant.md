---
description: Предоставляет линию в верхней области Просмотр событий, которая служит контейнером для всех возможных данных, вставленных в столбец.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Структура НМКОЛУМНВАРИАНТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 814b419909591e45c07b3ed499072ec4871cdeb1f4c5a355277a03d0623d264c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890028"
---
# <a name="nmcolumnvariant-structure"></a>Структура НМКОЛУМНВАРИАНТ

Структура **нмколумнвариант** предоставляет линию в верхней области Просмотр событий, которая служит контейнером для всех возможных данных, вставленных в столбец.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Значение из типа перечисления [**нмколумнтипе**](nmcolumntype.md) .

</dd> <dt>

**Значение**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

8-битовое целочисленное значение без знака.

</dd> <dt>

**Sint8Val**
</dt> <dd>

8-битовое целочисленное значение со знаком.

</dd> <dt>

**Uint16Val**
</dt> <dd>

16-битовое целочисленное значение без знака.

</dd> <dt>

**Sint16Val**
</dt> <dd>

16-разрядное целое число со знаком.

</dd> <dt>

**Uint32Val**
</dt> <dd>

32-битовое целочисленное значение без знака.

</dd> <dt>

**Sint32Val**
</dt> <dd>

32-битовое целочисленное значение со знаком.

</dd> <dt>

**Float64Val**
</dt> <dd>

64-разрядное значение с плавающей запятой.

</dd> <dt>

**фрамевал**
</dt> <dd>

Номер кадра.

</dd> <dt>

**есновал**
</dt> <dd>

Отображается значение Да или нет.

</dd> <dt>

**оноффвал**
</dt> <dd>

Отображение или отключение.

</dd> <dt>

**труефалсевал**
</dt> <dd>

Отображает значение true или false.

</dd> <dt>

**макаддрвал**
</dt> <dd>

MAC-адрес.

</dd> <dt>

**ипксаддрвал**
</dt> <dd>

IPX-адрес.

</dd> <dt>

**ипаддрвал**
</dt> <dd>

IP-адрес.

</dd> <dt>

**вартимевал**
</dt> <dd>

Вариант времени. Используйте **варианттиметосистемтиме** для преобразования в системное время.

</dd> <dt>

**пстрингвал**
</dt> <dd>

Указатель на строку.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**нмколумнтипе**](nmcolumntype.md)
</dt> </dl>

 

 




