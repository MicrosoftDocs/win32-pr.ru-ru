---
description: Описание параметров данных для виртуального коммутатора Ethernet.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Класс CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662805"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>\_Класс CIM виртуалесернетсвитчсеттингдата

Описание параметров данных для виртуального коммутатора Ethernet.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалесернетсвитчсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ виртуалесернетсвитчсеттингдата** имеет следующие свойства.

<dl> <dt>

**ассоЦиатедресаурцепул**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий пулы ресурсов узла, которые в настоящее время связаны или связываются с коммутатором Ethernet для распределения Ethernet-подключений между коммутатором Ethernet и виртуальной машиной. Каждое значение этого свойства, отличное от NULL, должно соответствовать **\_ коду URI WBEM \_ унтипединстанцепас** , как определено в спецификации DMTF "DSP0207".

</dd> <dt>

**макснуммакаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число уникальных MAC-адресов, которые коммутатор может изучить для обучения MAC-адресов, как определено в стандарте IEEE 802,1.

</dd> <dt>

**вланконнектион**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий идентификаторы виртуальных ЛС, к которым может получить доступ коммутатор.

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

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




