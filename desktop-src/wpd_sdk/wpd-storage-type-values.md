---
description: тип перечисления "WPD-типы \_ хранилища" \_ \_ описывает различные Windows типы хранилищ переносимых устройств.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Перечисление WPD_STORAGE_TYPE_VALUES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842080"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_ \_ Перечисление значений типа хранилища WPD \_

тип перечисления "WPD-типы **\_ хранилища \_ \_** " описывает различные Windows типы хранилищ переносимых устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_тип хранилища WPD не \_ \_ определен**
</dt> <dd>

Хранилище имеет неопределенный тип.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_тип хранилища WPD — \_ \_ фиксированное \_ ПЗУ**
</dt> <dd>

Хранилище не является съемным и доступно только для чтения.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_тип хранилища WPD — \_ \_ съемные \_ диски**
</dt> <dd>

Хранилище является съемным и доступно только для чтения.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_тип хранилища \_ WPD \_ фиксированный \_ объем ОЗУ**
</dt> <dd>

Хранилище не является съемным и доступно для чтения и записи.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_тип хранилища WPD — \_ \_ съемная \_ оперативная память**
</dt> <dd>

Хранилище является съемным и доступно для чтения и записи.

</dd> </dl>

## <a name="remarks"></a>Remarks

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




