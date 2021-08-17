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
ms.openlocfilehash: 6243e86ec53213f959ea0b8f420543a9dca619de9d12593a73619aab2805091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646462"
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

### <a name="properties"></a>Элемент Property

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

 

 




