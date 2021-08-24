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
ms.openlocfilehash: 8ccf3b6cd9ac1fcc97c8e409df792069c02652d5e0bf92ef8bbbec9f88e36cf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899534"
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

### <a name="properties"></a>Элемент Property

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

