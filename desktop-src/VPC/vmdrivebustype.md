---
title: Перечисление Вмдривебустипе (Впккоминтерфацес. h)
description: Указывает тип шины.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- Перечисление Вмдривебустипе Virtual PC
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136290"
---
# <a name="vmdrivebustype-enumeration"></a>Перечисление Вмдривебустипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает тип шины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**Вмдривебустипе является \_ недопустимым**
</dt> <dd>

Нет типа шины.

</dd> <dt>

<span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**\_Интегрированная среда разработки вмдривебустипе**
</dt> <dd>

Тип шины IDE.

</dd> <dt>

<span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**Вмдривебустипе \_ SCSI**
</dt> <dd>

Тип шины SCSI.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



 

