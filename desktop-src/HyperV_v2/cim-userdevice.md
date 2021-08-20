---
description: Представляет логическое устройство, позволяющее пользователю вводить, просматривать или слышать данные в компьютерной системе.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Класс CIM_UserDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbd5e96c7d00574848c43fe57695ba84e39dd2c0591483a65a1f56af94cca8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068664"
---
# <a name="cim_userdevice-class-hyper-v-management"></a>Класс CIM_UserDevice (Управление Hyper-V)

Представляет логическое устройство, позволяющее пользователю вводить, просматривать или слышать данные в компьютерной системе.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ усердевице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ усердевице** имеет следующие свойства.

<dl> <dt>

**IsLocked**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если устройство заблокировано, что препятствует вводу или выходу пользователя. в противном случае — **значение false**.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




