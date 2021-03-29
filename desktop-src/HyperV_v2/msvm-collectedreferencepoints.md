---
description: Связывает референцепоинтколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм виртуалсистемреференцепоинт.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Класс Msvm_CollectedReferencePoints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810918"
---
# <a name="msvm_collectedreferencepoints-class"></a>\_Класс мсвм коллектедреференцепоинтс

Связывает [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) с содержащимися в них объектами [**мсвм \_ виртуалсистемреференцепоинт**](msvm-virtualsystemreferencepoint.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектедреференцепоинтс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ коллектедреференцепоинтс** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ референцепоинтколлектион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Объект [**мсвм \_ референцепоинтколлектион**](msvm-referencepointcollection.md) GROUPING или "сумка", представляющий коллекцию.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалсистемреференцепоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")
</dt> </dl>

Объект [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , содержащий элементы коллекции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОЛЛЕКТЕДМСЕС CIM**](cim-collectedmses.md)
</dt> </dl>

 

