---
description: Связывает прозрачную службу моста с записью своей базы данных пересылки.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: Класс CIM_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662812"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a>\_Класс CIM транспарентбридгингдинамикфорвардинг

Связывает прозрачную службу моста с записью своей базы данных пересылки.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ транспарентбридгингдинамикфорвардинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ транспарентбридгингдинамикфорвардинг** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ транспарентбридгингсервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) на службу прозрачного моста.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ динамикфорвардинжентри**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка [**CIM \_ динамикфорвардинжентри**](cim-dynamicforwardingentry.md) на запись пересылки базы данных.

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

 

