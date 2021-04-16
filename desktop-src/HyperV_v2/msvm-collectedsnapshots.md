---
description: Связывает снапшотколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм виртуалсистемсеттингдата.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Класс Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662663"
---
# <a name="msvm_collectedsnapshots-class"></a>\_Класс мсвм коллектедснапшотс

Связывает [**\_ снапшотколлектион мсвм**](msvm-snapshotcollection.md) с содержащимися в них объектами [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектедснапшотс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ коллектедснапшотс** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ снапшотколлектион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Объект [**мсвм \_ снапшотколлектион**](msvm-snapshotcollection.md) GROUPING или "сумка", представляющий коллекцию.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалсистемсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")
</dt> </dl>

Объект [**\_ виртуалсистемсеттингдата мсвм**](msvm-virtualsystemsettingdata.md) , содержащий элементы коллекции.

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

 

