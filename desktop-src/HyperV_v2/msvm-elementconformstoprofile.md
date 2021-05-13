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
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843285"
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
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

