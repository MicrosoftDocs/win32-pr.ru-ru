---
description: Представляет ассоциацию между управляемыми элементами и их возможностями.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Класс Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683751"
---
# <a name="msvm_elementcapabilities-class"></a>\_Класс мсвм елементкапабилитиес

Представляет ассоциацию между управляемыми элементами и их возможностями.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ елементкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ елементкапабилитиес** имеет следующие свойства.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ возможности CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Объект capabilities, связанный с элементом. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Характеристики**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержит описательные сведения о возможностях. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Значение                                                                                                                                                                                                                       | Значение                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**По умолчанию**</dt> <dt>2</dt> </dl> | Связанные возможности представляют возможности управляемого элемента по умолчанию.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Текущие**</dt> <dt>3</dt> </dl> | Связанные возможности представляют текущие возможности управляемого элемента.<br/> |



 

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **min** (1)
</dt> </dl>

Управляемый элемент. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ елементкапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ЕЛЕМЕНТКАПАБИЛИТИЕС CIM**](cim-elementcapabilities.md)
</dt> <dt>

[**\_ЕЛЕМЕНТКАПАБИЛИТИЕС CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**Мсвм \_ елементкапабилитиес (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

