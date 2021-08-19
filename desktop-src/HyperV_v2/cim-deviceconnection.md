---
description: Связь, указывающая, что два или несколько устройств соединяются друг с другом.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Класс CIM_DeviceConnection (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81ec2826339e27d956750360b280fcafd7b55e6264a6bcab83ebc1cb41a1ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812848"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>Класс CIM_DeviceConnection (Управление Hyper-V)

Связь, указывающая, что два или несколько устройств соединяются друг с другом.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ девицеконнектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ девицеконнектион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

устройству;

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Второе устройство, подключенное к другому устройству.

</dd> <dt>

**неготиатеддатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Связь портов шины DMTF \| 001,3 "), **Пунит** (" bit ")
</dt> </dl>

Если возможны несколько значений ширины данных шины и соединения, свойство Неготиатеддатавидс определяет ту, которая используется между устройствами. Ширина данных указывается в битах. Если ширина данных не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0.

</dd> <dt>

**неготиатедспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Связь портов шины DMTF \| 001,2 "), **Пунит** (" бит/сек ")
</dt> </dl>

Если возможны несколько скоростей шины и соединения, это свойство определяет скорость, используемую между устройствами, в битах в секунду. Если скорость подключения или шины не согласована, или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение "0".

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

 

