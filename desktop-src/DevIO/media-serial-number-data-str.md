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
ms.openlocfilehash: cbb007769238f0e6a4239366e8fe9956e61f892f7d3c98f2b638dc425dc9359f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053484"
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

## <a name="remarks"></a>Remarks

Для структуры **\_ \_ \_ данных серийного номера носителя** не доступен файл заголовка. Включите определение структуры в верхнюю часть этой страницы в исходном коде.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>          |
| Минимальная версия сервера<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IOCTL \_ хранилище \_ Получение \_ \_ серийного \_ номера носителя**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




