---
description: Структура STORAGE_HW_FIRMWARE_INFO — эта структура содержит сведения о встроенном по устройства.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Структура STORAGE_HW_FIRMWARE_INFO (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 1b9aa008e108f1282f8f61aaeacdce11eba7016632fa9643ae3db5550efb1e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047914"
---
# <a name="storage_hw_firmware_info-structure"></a>\_ \_ \_ Структура сведений о встроенном по оборудования хранилища

Эта структура содержит сведения о встроенном по устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Версия этой структуры. Для этого параметра должно быть задано значение sizeof ( \_ \_ сведения о встроенном по оборудования хранилища \_ ).

</dd> <dt>

**Размер**
</dt> <dd>

Размер этой структуры в виде буфера, включая слот.

</dd> <dt>

**суппортупграде**
</dt> <dd>

Указывает, что это встроенное по поддерживает обновление.

</dd> <dt>

**Reserved0**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**слоткаунт**
</dt> <dd>

Число слотов встроенного по на устройстве. Это измерение массива слотов.

> [!Note]  
> Некоторые устройства могут хранить более 1 образа встроенного по, если они имеют более одного слота встроенного по.

 

</dd> <dt>

**активеслот**
</dt> <dd>

Слот встроенного по, содержащий активный или выполняемый в данный момент образ встроенного по.

</dd> <dt>

**пендингактиватеслот**
</dt> <dd>

Слот встроенного по, ожидающий активации.

</dd> <dt>

**фирмварешаред**
</dt> <dd>

Указывает, что встроенное по относится как к устройству, так и к контроллеру или адаптеру, например SSD NVMe.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**имажепайлоадалигнмент**
</dt> <dd>

Выравнивание полезных данных изображения в байтах. Максимальное значение — \_ Размер страницы. Размер перемещения — это множественные этого размера. Для некоторых протоколов требуется по крайней мере размер сектора. Если это значение равно 0, это означает, что это значение является недопустимым.

</dd> <dt>

**имажепайлоадмакссизе**
</dt> <dd>

Максимальный размер полезных данных образа используется для одной команды.

</dd> <dt>

**Слот**
</dt> <dd>

Содержит сведения о слотах для каждого слота на устройстве, тип [**данных \_ \_ \_ слот \_ встроенного по аппаратного обеспечения хранилища**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



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

[**\_ \_ \_ запрос сведений о встроенном по оборудования хранилища \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**\_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




