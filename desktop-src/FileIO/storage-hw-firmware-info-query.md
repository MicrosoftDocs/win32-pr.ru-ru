---
description: Эта структура содержит сведения о встроенном по устройства.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Структура STORAGE_HW_FIRMWARE_INFO_QUERY (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683443"
---
# <a name="storage_hw_firmware_info_query-structure"></a>\_ \_ \_ Структура запроса сведений о встроенном по оборудования хранилища \_

Эта структура содержит сведения о встроенном по устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Версия этой структуры. Для этого параметра должно быть задано значение sizeof ( \_ \_ \_ запрос сведений о встроенном по аппаратного обеспечения хранилища \_ )

</dd> <dt>

**Размер**
</dt> <dd>

Размер этой структуры в виде буфера.

</dd> <dt>

**Флаги**
</dt> <dd>

Флаги, связанные с запросом. Ниже приведены флаги, которые можно задать в этом элементе.



| Flag                                             | Описание                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| \_ \_ \_ \_ контроллер флага запроса встроенного по аппаратного обеспечения хранилища \_ | Указывает, что целевой объект запроса отличается от самого устройства. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Виниоктл. h. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

[**\_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




