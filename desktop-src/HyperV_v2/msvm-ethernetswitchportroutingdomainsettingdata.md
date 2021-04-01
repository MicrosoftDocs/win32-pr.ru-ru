---
description: Представляет данные о параметрах домена маршрутизации.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Класс Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913888"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>\_Класс мсвм есернетсвитчпортраутингдомаинсеттингдата

Представляет данные о параметрах домена маршрутизации.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортраутингдомаинсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчпортраутингдомаинсеттингдата** имеет следующие свойства.

<dl> <dt>

**исолатионидлист**
</dt> <dd> <dl> <dt>

Тип данных: массив **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Идентификаторы VirtualSubnetId или VLAN для доменов маршрутизации.

</dd> <dt>

**исолатиониднамелист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Массив понятных имен VirtualSubnetId или VLAN.

</dd> <dt>

**раутингдомаингуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (1), [**версия**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

GUID домена маршрутизации.

</dd> <dt>

**раутингдомаиннаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (2), [**версия**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Понятное имя домена маршрутизации.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ есернетсвитчпортфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

