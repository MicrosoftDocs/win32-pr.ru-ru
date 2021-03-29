---
description: Связывает виртуальный коммутатор Ethernet с расширениями, привязанными к нему в данный момент.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Класс Msvm_HostedEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810438"
---
# <a name="msvm_hostedethernetswitchextension-class"></a>\_Класс мсвм хостедесернетсвитчекстенсион

Связывает виртуальный коммутатор Ethernet с расширениями, привязанными к нему в данный момент.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ хостедесернетсвитчекстенсион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ хостедесернетсвитчекстенсион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий виртуальный коммутатор.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющий экземпляр расширения коммутатора, привязанный к виртуальному коммутатору.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

