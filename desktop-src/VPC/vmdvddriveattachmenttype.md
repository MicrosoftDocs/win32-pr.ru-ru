---
title: Перечисление Вмдвддривеаттачменттипе (Впккоминтерфацес. h)
description: Указывает, что подключено к DVD-дисководу.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Перечисление Вмдвддривеаттачменттипе Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491286"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a>Перечисление Вмдвддривеаттачменттипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает, что подключено к DVD-дисководу.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**Вмдвддриве \_ None**
</dt> <dd>

Нет присоединенных.

</dd> <dt>

<span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**\_изображение вмдвддриве**
</dt> <dd>

Имеется прикрепленный файл ISO-образа.

</dd> <dt>

<span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**Вмдвддриве \_ HostDrive**
</dt> <dd>

Подключенный компакт-диск или DVD-дисковод.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмдвддриве:: вложение**](ivmdvddrive-attachment.md)
</dt> </dl>

 

