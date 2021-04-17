---
description: Представляет данные параметра изоляции.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Класс Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663589"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a>\_Класс мсвм есернетсвитчпортисолатионсеттингдата

Представляет данные параметра изоляции.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортисолатионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчпортисолатионсеттингдата** имеет следующие свойства.

<dl> <dt>

**алловунтагжедтраффик**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Разрешено ли порту отправлять и получать трафик без тегов.

</dd> <dt>

**дефаултисолатионид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Значение по умолчанию VirtualSubnetId или VLAN, которое будет задано для всего трафика отправки и получения, если **алловедунтагжедтраффик** имеет **значение true**.

</dd> <dt>

**енаблемултитенантстакк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Если **значение — true**, сетевой стек на виртуальной машине сможет получить доступ к конфигурации изоляции. Значение по умолчанию — **false**.

</dd> <dt>

**IsolationMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Использует ли порт **виртуальную ЛС** или **VirtualSubnetId** для изоляции. **Нативевиртуалсубнетид** используется для сетей на основе WNV VirtualSubnetId.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

**Нативевиртуалсубнетид** (1)


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

**Екстерналвиртуалсубнетид** (2)


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

**Виртуальная ЛС** (3)


</dt> <dd></dd> </dl>

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

 

