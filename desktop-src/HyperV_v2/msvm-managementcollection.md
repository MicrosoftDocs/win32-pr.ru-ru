---
description: Представляет коллекцию других коллекций.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Класс Msvm_ManagementCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684475"
---
# <a name="msvm_managementcollection-class"></a>\_Класс мсвм манажементколлектион

Представляет коллекцию других коллекций.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ манажементколлектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ манажементколлектион** имеет следующие свойства.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Уникальная идентификация объекта коллекции.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Определяемое пользователем имя коллекции. Обратите внимание, что это не обязательно должно быть уникальным.

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

[**\_КОЛЛЕКТИОНОФМСЕС CIM**](cim-collectionofmses.md)
</dt> </dl>

 

