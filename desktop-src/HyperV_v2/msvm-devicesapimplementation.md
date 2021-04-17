---
description: Связь между точкой доступа к службе (SAP) и ее реализацией.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Класс Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663727"
---
# <a name="msvm_devicesapimplementation-class"></a>\_Класс мсвм девицесапимплементатион

Связь между точкой доступа к службе (SAP) и ее реализацией. Кратность этой ассоциации — «многие ко многим». SAP может предоставляться более чем одним логическим устройством, работающим совместно. Любое устройство может предоставлять более одного SAP. Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа. При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP. Эти отдельные экземпляры будут иметь связи с уникальными реализациями.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ девицесапимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ девицесапимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Логическое устройство. Это свойство наследуется от [**CIM \_ девицесапимплементатион**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Точка доступа к службе, реализованная с помощью логического устройства. Это свойство наследуется от [**CIM \_ девицесапимплементатион**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ девицесапимплементатион мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

См. раздел [запросы к сетевым объектам](querying-networking-objects.md).

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

[**\_ДЕВИЦЕСАПИМПЛЕМЕНТАТИОН CIM**](cim-devicesapimplementation.md)
</dt> <dt>

[**\_ДЕВИЦЕСАПИМПЛЕМЕНТАТИОН CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

