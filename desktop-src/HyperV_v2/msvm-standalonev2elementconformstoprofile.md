---
description: Определяет зарегистрированные профили, на которые ссылается изолированная автономная система.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Класс Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991463"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>\_Класс мсвм StandaloneV2ElementConformsToProfile

Определяет зарегистрированные профили, на которые ссылается изолированная автономная система.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ StandaloneV2ElementConformsToProfile** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ StandaloneV2ElementConformsToProfile** имеет следующие свойства.

<dl> <dt>

**конформантстандард**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ регистередпрофиле**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Зарегистрированный профиль, которому соответствует автономная система.

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("Корневая \\ \\ виртуализация \\ \\ v2")
</dt> </dl>

Автономная система, которая соответствует зарегистрированному профилю.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневое \\ взаимодействие<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ елементконформстопрофиле**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

