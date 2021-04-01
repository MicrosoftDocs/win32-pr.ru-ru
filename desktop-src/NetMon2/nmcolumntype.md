---
description: Задает элементы структуры НМКОЛУМНВАРИАНТ.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Перечисление НМКОЛУМНТИПЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818521"
---
# <a name="nmcolumntype-enumeration"></a>Перечисление НМКОЛУМНТИПЕ

Перечисление **нмколумнтипе** указывает элементы структуры [**нмколумнвариант**](nmcolumnvariant.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**НМКОЛУМНТИПЕ \_ UINT8**
</dt> <dd>

8-битовое целое число без знака.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**НМКОЛУМНТИПЕ \_ SINT8**
</dt> <dd>

8-разрядное целое число со знаком.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**НМКОЛУМНТИПЕ \_ UINT16**
</dt> <dd>

16-разрядное целое число без знака.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**НМКОЛУМНТИПЕ \_ SINT16**
</dt> <dd>

16-разрядное целое число со знаком.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**НМКОЛУМНТИПЕ \_ UINT32**
</dt> <dd>

32-битовое целое число без знака.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**НМКОЛУМНТИПЕ \_ SINT32**
</dt> <dd>

32-разрядное целое число со знаком.

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**НМКОЛУМНТИПЕ \_ FLOAT64**
</dt> <dd>

64-разрядное число с плавающей запятой.

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**НМКОЛУМНТИПЕ \_ рамка**
</dt> <dd>

Номер кадра.

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**НМКОЛУМНТИПЕ \_ Данет**
</dt> <dd>

"Yes" или "No".

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**НМКОЛУМНТИПЕ \_ онофф**
</dt> <dd>

"On" или "OFF"

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**НМКОЛУМНТИПЕ \_ труефалсе**
</dt> <dd>

"True" или "false".

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**НМКОЛУМНТИПЕ \_ макаддр**
</dt> <dd>

MAC-адрес.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**НМКОЛУМНТИПЕ \_ ипксаддр**
</dt> <dd>

IPX-адрес.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**НМКОЛУМНТИПЕ \_ reduce**
</dt> <dd>

IP-адрес.

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**НМКОЛУМНТИПЕ \_ вартиме**
</dt> <dd>

Вариант времени.

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_строка нмколумнтипе**
</dt> <dd>

Указатель на строку.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




