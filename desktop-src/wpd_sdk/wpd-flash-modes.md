---
description: '\_ \_ Тип перечисления WPD Flash Modes описывает режим Flash, используемый при записи изображений с устройства.'
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Перечисление WPD_FLASH_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668683"
---
# <a name="wpd_flash_modes-enumeration"></a>\_Перечисление Flash- \_ режимов WPD

Тип **перечисления \_ WPD \_ Flash** Modes описывает режим Flash, используемый при записи изображений с устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_режим Flash-памяти WPD не \_ \_ определен**
</dt> <dd>

Не указан режим вспышки.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_Автоматическое вспышка в \_ режиме Flash \_**
</dt> <dd>

Указывает, что Flash следует использовать в автоматическом режиме, как указано устройством.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_Вспышка Flash- \_ режима \_ отключен**
</dt> <dd>

Указывает, что Flash не следует использовать.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_ \_ Заливка флеш-режима WPD \_**
</dt> <dd>

Задает тип заливки Flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_ \_ \_ \_ Автоматический глаз флеш-режима WPD Flash \_**
</dt> <dd>

Указывает, что следует использовать Flash-память для сокращения красных глаз.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_Заливка флэш-памяти WPD с \_ \_ красным \_ глазом \_**
</dt> <dd>

Указывает, что следует использовать вспышку с заливкой красных глаз.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ \_ Внешняя синхронизация флеш-режима WPD \_**
</dt> <dd>

Указывает, что Flash должен быть синхронизирован с другими внешними устройствами Flash.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется в свойстве [ \_ \_ \_ \_ режима вспышки для изображения WPD](still-image-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




