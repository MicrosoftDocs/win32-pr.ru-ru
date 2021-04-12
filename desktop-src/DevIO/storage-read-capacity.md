---
description: Содержит сведения о размере устройства. Это возвращается с помощью \_ \_ управляющего кода для считывания емкости хранилища ioctl \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Структура STORAGE_READ_CAPACITY (Нтддстор. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423258"
---
# <a name="storage_read_capacity-structure"></a>\_Структура емкости для чтения хранилища \_

Содержит сведения о размере устройства. Это возвращается с помощью управляющего кода для [**\_ \_ считывания \_ емкости хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Версия этой структуры. Вызывающий объект должен присвоить этому элементу значение `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Размер**
</dt> <dd>

Размер возвращаемых данных.

</dd> <dt>

**блоккленгс**
</dt> <dd>

Число байтов на блок.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Общее число блоков на диске.

</dd> <dt>

**дискленгс**
</dt> <dd>

Размер диска в байтах.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Файл заголовка Нтддстор. h доступен в комплекте драйверов Windows (WDK).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008, Windows Server 2003 с пакетом обновления 1<br/>                          |
| Header<br/>                   | <dl> <dt>Нтддстор. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Чтение данных \_ о \_ емкости хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




