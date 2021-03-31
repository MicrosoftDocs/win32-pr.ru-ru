---
description: Установите связь между экземпляром \_ класса мсвм емулатедесернетпортсеттингдата или мсвм \_ синсетицесернетпортсеттингдата с экземпляром \_ класса мсвм GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Класс Msvm_SettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998830"
---
# <a name="msvm_settingdatacomponent-class"></a>\_Класс мсвм сеттингдатакомпонент

Установите связь между экземпляром класса [**мсвм \_ Емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) или [**мсвм \_ Синсетицесернетпортсеттингдата**](msvm-syntheticethernetportsettingdata.md) с экземпляром класса [**мсвм \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сеттингдатакомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сеттингдатакомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ Емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) или [**мсвм \_ синсетицесернетпортсеттингдата**](msvm-syntheticethernetportsettingdata.md) , представляющий порт Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md) , представляющий конфигурацию гостевого сетевого адаптера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

