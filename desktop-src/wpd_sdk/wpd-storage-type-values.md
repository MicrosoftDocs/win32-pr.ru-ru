---
description: Тип перечисления "WPD- \_ тип хранилища" \_ \_ описывает различные типы хранилищ переносных устройств Windows.
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
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648781"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_ \_ Перечисление значений типа хранилища WPD \_

Тип перечисления " **WPD- \_ \_ тип \_ хранилища** " описывает различные типы хранилищ переносных устройств Windows.

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

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




