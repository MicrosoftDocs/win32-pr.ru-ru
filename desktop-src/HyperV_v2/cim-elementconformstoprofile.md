---
description: Представляет ассоциацию, в которой управляемый элемент соответствует стандарту зарегистрированного профиля.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Класс CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662598"
---
# <a name="cim_elementconformstoprofile-class"></a>\_Класс CIM елементконформстопрофиле

Представляет ассоциацию, в которой управляемый элемент соответствует стандарту зарегистрированного профиля. Эта ассоциация обычно применяется к экземпляру более высокого уровня, например к системе, пространству имен или службе. При применении к экземпляру более высокого уровня все составные части должны вести себя соответствующим образом для обеспечения соответствия Манажеделемент с именованным Регистередпрофиле.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ елементконформстопрофиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ елементконформстопрофиле** имеет следующие свойства.

<dl> <dt>

**конформантстандард**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ регистередпрофиле**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Зарегистрированный профиль, которому соответствует управляемый элемент.

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Управляемый элемент, который соответствует зарегистрированному профилю.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

