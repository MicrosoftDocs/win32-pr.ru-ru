---
description: Представляет связь между экземпляром Мсвм \_ гуестсервицеинтерфацекомпонент и экземпляром мсвм \_ гуестсервице, который представляет службу, работающую в гостевой системе.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Класс Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf2e551a30f169477f9dc73e58ecd9e6c3a78b708c047eb0088f36782623da3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130444"
---
# <a name="msvm_registeredguestservice-class"></a>\_Класс мсвм регистередгуестсервице

Представляет связь между экземпляром [**мсвм \_ гуестсервицеинтерфацекомпонент**](msvm-guestserviceinterfacecomponent.md) и экземпляром [**мсвм \_ гуестсервице**](msvm-guestservice.md), который представляет службу, работающую в гостевой системе. Этот класс является производным от [**класса \_ зависимостей CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ регистередгуестсервице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ регистередгуестсервице** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ гуестсервицеинтерфацекомпонент**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Ссылка на компонент интерфейса гостевой службы в этой ассоциации.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ гуестсервице**](msvm-guestservice.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")
</dt> </dl>

Ссылка на зарегистрированную гостевую службу, которая зависит от свойства **Antecedent** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> <dt>

[**\_Зависимость CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

