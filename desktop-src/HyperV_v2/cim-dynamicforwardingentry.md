---
description: Представляет запись в базе данных пересылки, связанную с \_ классом CIM транспарентбридгингсервице.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Класс CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682941"
---
# <a name="cim_dynamicforwardingentry-class"></a>\_Класс CIM динамикфорвардинжентри

Представляет запись в базе данных пересылки, связанную с классом [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ динамикфорвардинжентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ динамикфорвардинжентри** имеет следующие свойства.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя класса или подкласса, используемого для создания экземпляра. При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

</dd> <dt>

**динамикстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpFdbStatus ")
</dt> </dl>

Состояние записи.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

**Недопустимое** (2)


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

**Узнали** (3)


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

**Self** (4)


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

Управление **(5** )


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpFdbAddress ")
</dt> </dl>

MAC-адрес одноадресной рассылки, по которому служба моста фильтрует данные. MAC-адрес имеет формат двенадцати шестнадцатеричных цифр, например 010203040506, с каждой парой, представляющей один из шести октетов MAC-адреса в каноническом порядке в соответствии с RFC 2469.

</dd> <dt>

**сервицекреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Служба CIM**](cim-service.md)".**CreationClassName**")
</dt> </dl>

Значение **CreationClassName** объекта службы области.

</dd> <dt>

**Служба**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Служба CIM**](cim-service.md)".**Name**")
</dt> </dl>

Имя службы определения области.

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Значение **CreationClassName** объекта System области.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")
</dt> </dl>

Имя системы области.

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

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> </dl>

 

