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
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704054"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




