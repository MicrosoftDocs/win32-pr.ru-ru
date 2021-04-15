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
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497805"
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

## <a name="remarks"></a>Комментарии

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

 

 




