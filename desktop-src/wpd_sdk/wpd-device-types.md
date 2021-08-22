---
description: '\_тип перечисления типов устройств типа "wpd" \_ описывает различные типы Windowsных портативных устройств (WPD), обычно используемые для определения базовой классификации и внешнего вида портативного устройства.'
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Перечисление WPD_DEVICE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657464"
---
# <a name="wpd_device_types-enumeration"></a>\_ \_ Перечисление типов устройств WPD

тип **перечисления \_ \_ типов устройств** типа "wpd" описывает различные типы Windowsных портативных устройств (WPD), обычно используемые для определения базовой классификации и внешнего вида портативного устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_ \_ универсальный тип устройства типа WPD \_**
</dt> <dd>

Универсальный WPD, включающий в себя Многофункциональные устройства, которые не входят в одно из значений перечисления других [**\_ \_ типов устройств типа WPD**](wpd-device-types.md) .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_тип устройства \_ WPD \_ Camera**
</dt> <dd>

Устройство камеры, например цифровая камера.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_тип устройства \_ WPD \_ \_ проигрыватель мультимедиа**
</dt> <dd>

Устройство проигрывателя мультимедиа, которое поддерживает воспроизведение аудио, видео или просмотр изображений, например портативный музыкальный проигрыватель или портативный Media Center. Не все эти функции классифицируются как \_ устройства типа "устройство WPD \_ " \_ \_ проигрывателя мультимедиа. Например, устройства с портативным музыкальным проигрывателем классифицируются как \_ устройства \_ типа WPD \_ Media \_ Player.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**устройство типа "WPD" \_ \_ \_ Телефон**
</dt> <dd>

Телефонное устройство, например мобильный телефон.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_ \_ видео типа устройства \_ WPD**
</dt> <dd>

Видеоустройство.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_тип устройства \_ WPD \_ \_ Диспетчер персональных данных \_**
</dt> <dd>

Устройство диспетчера персональных данных.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_устройство типа "устройства WPD" \_ \_ Audio \_ Record**
</dt> <dd>

Устройство записи звука.

</dd> </dl>

## <a name="remarks"></a>Remarks

**WPD \_ Чтение \_ типов устройств** осуществляется с помощью интерфейса [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) . Приложения WPD могут использовать эти значения для определения универсального внешнего вида устройства. Это значит, что для устройств, подобных камере, отображается изображение камеры, изображение мобильного телефона отображается для устройств, подобных телефонам, и т. д.

> [!Note]  
> Приложения WPD должны использовать возможности портативного устройства для определения функций, а не для **\_ \_ типов устройств типа WPD** .

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




