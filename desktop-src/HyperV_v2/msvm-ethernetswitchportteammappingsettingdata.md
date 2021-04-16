---
description: Представляет данные настройки функции сопоставления команды порта.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Класс Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664763"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a>\_Класс мсвм есернетсвитчпорттеаммаппингсеттингдата

Представляет данные настройки функции сопоставления команды порта.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпорттеаммаппингсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчпорттеаммаппингсеттингдата** имеет следующие свойства.

<dl> <dt>

**нетадаптердевицеид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (2), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

ИДЕНТИФИКАТОР устройства предпочтительного сопоставленного физического адаптера.

</dd> <dt>

**нетадаптернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Имя предпочитаемого сопоставленного физического адаптера.

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

[**Мсвм \_ есернетсвитчпортфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

