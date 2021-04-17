---
description: Структура АДДРЕССПАИР конструирует фильтр записи.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Структура АДДРЕССПАИР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663650"
---
# <a name="addresspair-structure"></a>Структура АДДРЕССПАИР

Структура **аддресспаир** конструирует фильтр записи.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Члены

<dl> <dt>

**аддрессфлагс**
</dt> <dd>

Флаги, описывающие адреса, используемые фильтром записи. Дополнительные сведения см. в разделе "Примечания".



| Значение                                                                                                                                                                                                         | Значение                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**\_Флаги адреса \_ соответствуют \_ летнему времени**</dt> </dl>                 | Соответствует адресу назначения.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**\_Флаги адреса \_ совпадают с \_ src**</dt> </dl>                 | Соответствует исходному адресу.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**\_исключаемые флаги адреса \_**</dt> </dl>                     | Исключает рамку, если этот адрес найден.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**\_флаг адреса \_ адрес \_ группы \_ DST**</dt> </dl> | Соответствует только биту группы. Используйте этот параметр для сообщений типа Broadcast.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**\_Флаги адреса \_ совпадают \_**</dt> </dl>              | Совпадает с адресами назначения и источника.<br/>                     |



 

</dd> <dt>

**налресервед**
</dt> <dd>

Это зарезервировано.

</dd> <dt>

**дстаддресс**
</dt> <dd>

Адрес назначения элемента пары адресов.

</dd> <dt>

**сркаддресс**
</dt> <dd>

Исходный адрес элемента пары адресов.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Флаги элемента **аддрессфлагс** можно объединить. Например, следующий параметр исключает кадр при обнаружении указанного исходного адреса.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[каптурефилтер](capturefilter.md)
</dt> </dl>

 

 




