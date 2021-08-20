---
description: Эта структура содержит сведения о слоте на устройстве.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Структура STORAGE_HW_FIRMWARE_SLOT_INFO (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 6db9bc5341bf3efec18390d171c205cc57b933afe166af6df48657b668cc85ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996458"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>\_ \_ \_ Структура сведений о слоте встроенного по АППАРАТного обеспечения хранилища \_

Эта структура содержит сведения о слоте на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Версия этой структуры. Для этого параметра должно быть задано значение sizeof ( \_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_ ).

</dd> <dt>

**Размер**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Номер слота этого слота.

</dd> <dt>

**ReadOnly**
</dt> <dd>

Указывает, доступен ли этот слот только для чтения.

</dd> <dt>

**Reserved0**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**Reserved1**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**Редакции**
</dt> <dd>

Редакция встроенного по этого слота.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>виниоктл. h. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ \_ Активация встроенного по службы хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**\_ \_ Активация встроенного по оборудования хранилища \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**\_ \_ скачивание встроенного по для хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**\_ \_ Загрузка встроенного по оборудования хранилища \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_ \_ сведения о встроенном по оборудования хранилища \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_ \_ \_ запрос сведений о встроенном по оборудования хранилища \_**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




