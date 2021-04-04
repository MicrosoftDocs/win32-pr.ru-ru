---
title: Перечисление Вмфлоппидривеаттачменттипе (Впккоминтерфацес. h)
description: Указывает, что подключено к дисководу гибких дисков.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Перечисление Вмфлоппидривеаттачменттипе Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988845"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a>Перечисление Вмфлоппидривеаттачменттипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает, что подключено к дисководу гибких дисков.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**Вмфлоппидриве \_ None**
</dt> <dd>

Нет присоединенных.

</dd> <dt>

<span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**\_изображение вмфлоппидриве**
</dt> <dd>

Файл образа гибкого диска подключен.

</dd> <dt>

<span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**Вмфлоппидриве \_ HostDrive**
</dt> <dd>

Подключен дисковод гибких дисков узла.

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

[**Ивмфлоппидриве:: вложение**](ivmfloppydrive-attachment.md)
</dt> </dl>

 

