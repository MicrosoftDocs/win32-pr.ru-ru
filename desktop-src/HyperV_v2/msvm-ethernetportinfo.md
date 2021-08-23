---
description: Ассоциация между экземпляром \_ класса мсвм есернетсвитчпорт и экземпляром \_ класса мсвм есернетпортдата, который представляет данные, собранные по порту с помощью расширения коммутатора.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Класс Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ef8f8f4ab7191400cfead94d20c4f601b97e48d46ee160d31c7b26b8e567b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524894"
---
# <a name="msvm_ethernetportinfo-class"></a>\_Класс мсвм есернетпортинфо

Ассоциация между экземпляром класса [**мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md) и экземпляром класса [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md) , который представляет данные, собранные по порту с помощью расширения коммутатора.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетпортинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетпортинфо** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ есернетсвитчпорт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Экземпляр класса [**мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md) , представляющий порт коммутатора.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ есернетпортдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")
</dt> </dl>

Экземпляр класса [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md) , представляющий данные порта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

