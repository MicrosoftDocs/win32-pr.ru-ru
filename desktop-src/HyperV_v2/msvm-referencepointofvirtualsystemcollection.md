---
description: Связывает референцепоинтколлектион Мсвм \_ с соответствующими \_ объектами мсвм виртуалсистемколлектион.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Класс Msvm_ReferencePointOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650827"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a>\_Класс мсвм референцепоинтофвиртуалсистемколлектион

Связывает [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) с соответствующими объектами [**мсвм \_ виртуалсистемколлектион**](msvm-virtualsystemcollection.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ референцепоинтофвиртуалсистемколлектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ референцепоинтофвиртуалсистемколлектион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ коллектионофмсес**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Коллектионофмсес CIM**](cim-collectionofmses.md) , представляющий независимый объект в этой ассоциации.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ коллекция CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Коллекция CIM**](cim-collection.md) , представляющая объект, который зависит от **предшествующей задачи**.

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

