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
ms.openlocfilehash: 1ee106c42267397f8dae66b1ed431b5d6fa3c1047b7ace6fd9a44bd81960be2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056422"
---
# <a name="vmdrivebustype-enumeration"></a>Перечисление Вмдривебустипе

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



 

