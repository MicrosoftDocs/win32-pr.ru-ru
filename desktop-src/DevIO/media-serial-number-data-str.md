---
description: Содержит серийный номер USB-устройства. Он используется в качестве \_ \_ контрольного кода для хранилища ioctl Get \_ Media \_ серийный \_ номер.
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Структура MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647755"
---
# <a name="media_serial_number_data-structure"></a>\_ \_ Структура данных серийного номера носителя \_

Содержит серийный номер USB-устройства. Он используется в качестве контрольного кода для [**\_ хранилища ioctl \_ Get \_ Media \_ серийный \_ номер**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**сериалнумберленгс**
</dt> <dd>

Размер строки **сериалнумбердата** в байтах.

</dd> <dt>

**Результат**
</dt> <dd>

Состояние запроса.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**сериалнумбердата**
</dt> <dd>

Серийный номер устройства.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для структуры **\_ \_ \_ данных серийного номера носителя** не доступен файл заголовка. Включите определение структуры в верхнюю часть этой страницы в исходном коде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>          |
| Минимальная версия сервера<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IOCTL \_ хранилище \_ Получение \_ \_ серийного \_ номера носителя**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




