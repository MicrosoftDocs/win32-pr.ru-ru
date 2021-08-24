---
title: Перечисление Вмдриветипе (Впккоминтерфацес. h)
description: Указывает тип диска, подключенного к расположению шины.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Перечисление Вмдриветипе Virtual PC
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5288988ff481bb785c4478bbd0ab8d5bf96e14d06ed016bdc9f9e593a677fc12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394324"
---
# <a name="vmdrivetype-enumeration"></a>Перечисление Вмдриветипе

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает тип диска, подключенного к расположению шины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**Вмдриветипе \_ null**
</dt> <dd>

Нет подключенного диска.

</dd> <dt>

<span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**Вмдриветипе \_ жесткого диска**
</dt> <dd>

Жесткий диск подключен.

</dd> <dt>

<span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**Вмдриветипе \_ DVD**
</dt> <dd>

Подключен компакт-диск или DVD-дисковод.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмвиртуалмачине:: Аттачеддриветипес**](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

