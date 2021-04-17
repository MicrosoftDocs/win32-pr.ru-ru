---
description: Тип перечисления "типы скорости WPD" \_ \_ описывает тип сжатия звуковых файлов.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Перечисление WPD_BITRATE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718089"
---
# <a name="wpd_bitrate_types-enumeration"></a>\_ \_ Перечисление типов скорости WPD

Тип перечисления " **\_ \_ типы скорости WPD** " описывает тип сжатия звукового файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**тип скорости WPD не \_ \_ \_ используется**
</dt> <dd>

Это значение не было указано.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_ \_ дискретная скорость типа WPD \_**
</dt> <dd>

Сжатие постоянной скорости потока.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**\_переменная скорости \_ типа \_ WPD**
</dt> <dd>

Сжатие переменной скорости.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**тип скорости WPD — \_ \_ \_ бесплатный**
</dt> <dd>

Скорость для свободной версии формата. Это постоянная скорость, которая ниже максимально допустимой скорости.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




