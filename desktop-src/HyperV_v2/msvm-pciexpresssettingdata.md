---
description: Представляет настроенное состояние порта PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Класс Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684461"
---
# <a name="msvm_pciexpresssettingdata-class"></a>\_Класс мсвм пЦиекспресссеттингдата

Представляет настроенное состояние порта PCI Express.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ пЦиекспресссеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ пЦиекспресссеттингдата** имеет следующие свойства.

<dl> <dt>

**виртуалфунктионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Номер виртуальной функции, которую необходимо назначить виртуальной машине.

</dd> <dt>

**виртуалсистемидентифиерс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Строковый массив идентификаторов этого ресурса в свободной форме, представленный операционной системе виртуальной системы. Индексы и значения для каждого индекса определяются для каждого ресурса (то есть для каждого перечислимого **значения типа ресурса)** . Для этого свойства задано значение "GUID".

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) класса SD.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

