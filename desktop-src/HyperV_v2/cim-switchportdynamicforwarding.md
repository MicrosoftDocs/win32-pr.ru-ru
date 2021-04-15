---
description: Представляет ассоциацию, в которой запись пересылаемой базы данных применяется к порту коммутатора.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: Класс CIM_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662819"
---
# <a name="cim_switchportdynamicforwarding-class"></a>\_Класс CIM свитчпортдинамикфорвардинг

Представляет ассоциацию, в которой запись пересылаемой базы данных применяется к порту коммутатора.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ свитчпортдинамикфорвардинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ свитчпортдинамикфорвардинг** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ свитчпорт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка [**на \_ свитчпорт CIM**](cim-switchport.md) для порта коммутатора.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ динамикфорвардинжентри**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка [**CIM \_ динамикфорвардинжентри**](cim-dynamicforwardingentry.md) на запись базы данных пересылки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

