---
description: Структура АДДРЕССТАБЛЕ содержит таблицу пар адресов.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Структура АДДРЕССТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064284"
---
# <a name="addresstable-structure"></a>Структура АДДРЕССТАБЛЕ

Структура **аддресстабле** содержит таблицу пар адресов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**наддресспаирс**
</dt> <dd>

Число пар адресов в массиве **аддресспаир** .

</dd> <dt>

**ннонмакаддресспаирс**
</dt> <dd>

Число пар адресов, отличных от MAC.

</dd> <dt>

**аддресспаир**
</dt> <dd>

Массив пар адресов. Обратите внимание, что можно хранить не более восьми пар адресов на структуру АДДРЕССТАБЛЕ.

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте эту структуру как часть процесса создания фильтра записи. Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аддресспаир](addresspair.md)
</dt> <dt>

[каптурефилтер](capturefilter.md)
</dt> </dl>

 

 




