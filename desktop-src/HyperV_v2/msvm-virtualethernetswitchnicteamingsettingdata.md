---
description: Представляет параметры объединения сетевых карт.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Класс Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c1c6294ecca73448c58b48d54c7f23504921e5ef520a53092649d0be362b27f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050694"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a>\_Класс мсвм виртуалесернетсвитчниктеамингсеттингдата

Представляет параметры объединения сетевых карт.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалесернетсвитчниктеамингсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ виртуалесернетсвитчниктеамингсеттингдата** имеет следующие свойства.

<dl> <dt>

**лоадбаланЦингалгорисм**
</dt> <dd> <dl> <dt>

Тип данных: **UINT32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Алгоритм балансировки нагрузки.

</dd> <dt>

**теамингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UINT32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Режим объединения.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




