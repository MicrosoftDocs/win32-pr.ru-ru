---
description: Msvm_CollectedCollections класс — связывает виртуалсистемколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм ComputerSystem.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Класс Msvm_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c645bc4c6dbf7cf6f7b3fb43cc229af3ef744b264b088356d192e4ad58e68a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790184"
---
# <a name="msvm_collectedcollections-class"></a>\_Класс мсвм коллектедколлектионс

Связывает [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) с содержащимися в них объектами [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектедколлектионс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ коллектедколлектионс** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ манажементколлектион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Объект [**мсвм \_ манажементколлектион**](msvm-managementcollection.md) GROUPING или "сумка", представляющий коллекцию.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ коллектионофмсес**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")
</dt> </dl>

[**\_ Коллектионофмсес CIM**](cim-collectionofmses.md) , содержащий элементы коллекции.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_КОЛЛЕКТЕДМСЕС CIM**](cim-collectedmses.md)
</dt> </dl>

 

