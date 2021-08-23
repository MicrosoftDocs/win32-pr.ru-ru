---
description: Определяет зарегистрированные профили, к которым соответствует указанная система.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Класс Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a80dfcb5ab260b4d60b6370bb34698efb201401f0c6d4924b143e8b9041258a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525054"
---
# <a name="msvm_elementconformstoprofile-class"></a>\_Класс мсвм елементконформстопрофиле

Определяет зарегистрированные профили, к которым соответствует указанная система. Эта ассоциация может применяться к любому управляемому элементу. При обычном использовании он применяется к экземпляру более высокого уровня, например к системе, пространству имен или службе. При применении к экземпляру более высокого уровня все составные части должны вести себя соответствующим образом для поддержки согласованности управляемого элемента с именованным зарегистрированным профилем.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ елементконформстопрофиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ елементконформстопрофиле** имеет следующие свойства.

<dl> <dt>

**конформантстандард**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ регистередпрофиле**](msvm-registeredprofile.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ регистередпрофиле**](msvm-registeredprofile.md) , представляющий зарегистрированный профиль, которому соответствует система.

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий систему, которая соответствует зарегистрированному профилю.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

