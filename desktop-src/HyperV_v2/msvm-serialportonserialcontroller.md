---
description: Связывает последовательный порт с последовательным контроллером.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Класс Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897818"
---
# <a name="msvm_serialportonserialcontroller-class"></a>\_Класс мсвм сериалпортонсериалконтроллер

Связывает последовательный порт с последовательным контроллером.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сериалпортонсериалконтроллер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сериалпортонсериалконтроллер** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последовательный контроллер, к которому подключен порт. Это свойство наследуется от [**CIM \_ портондевице**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Порт последовательного контроллера. Это свойство наследуется от [**CIM \_ портондевице**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ сериалпортонсериалконтроллер мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ПОРТОНДЕВИЦЕ CIM**](cim-portondevice.md)
</dt> <dt>

[**\_ПОРТОНДЕВИЦЕ CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Классы последовательных устройств](serial-devices-classes.md)
</dt> </dl>

 

