---
description: Эта Ассоциация указывает, что подкласс логического устройства (например, тома хранилища) подключен через конкретный контроллер протокола.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Класс Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086634"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>\_Класс мсвм протоколконтроллерфорунит

Эта Ассоциация указывает, что подкласс логического устройства (например, тома хранилища) подключен через конкретный контроллер протокола. Во многих ситуациях (например, Маскирование LUN хранилища) для связи с различными объектами могут использоваться многие из этих ассоциаций. Таким образом, подклассы определены для оптимизации перечисления ассоциаций.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ протоколконтроллерфорунит** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ протоколконтроллерфорунит** имеет следующие свойства.

<dl> <dt>

**акцессприорити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приоритет, предоставляемый для доступа к устройству через этот контроллер. Путь с наивысшим приоритетом будет иметь самое низкое значение для этого параметра. Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.

</dd> <dt>

**акцессстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли контроллер активной командой или доступом к устройству (2) или нет (3). Кроме того, можно определить значение 0 (неизвестно). Эти сведения необходимы в том случае, если логическое устройство может быть командо с помощью нескольких контроллеров протокола или доступно через несколько. Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Активно** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Неактивно** (3)
</dt> </dl>

</dd> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ протоколконтроллер**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Контроллер протокола. Этот класс наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Управляемое устройство. Этот класс наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**девицеакцесс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Права доступа, предоставленные устройству через этот контроллер. Этот класс наследуется от **CIM \_ протоколконтроллерфорунит**.



| Значение                                                                               | Значение                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Неизвестно<br/>         |
| <dl> <dt>2</dt> </dl>        | Чтение/запись<br/>      |
| <dl> <dt>3</dt> </dl>        | Только для чтения<br/>       |
| <dl> <dt>4</dt> </dl>        | Нет доступа.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | Зарезервировано DMTF<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Поставщик зарезервирован<br/> |



 

</dd> <dt>

**девиценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес связанного устройства в контексте предшествующего контроллера. Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ протоколконтроллерфорунит мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ПРОТОКОЛКОНТРОЛЛЕРФОРУНИТ CIM**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**\_ПРОТОКОЛКОНТРОЛЛЕРФОРУНИТ CIM**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[служба хранилища Класса](storage-classes.md)
</dt> </dl>

 

