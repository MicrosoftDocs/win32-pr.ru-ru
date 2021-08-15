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
ms.openlocfilehash: 5e5a1007516e5b8b7d827f0a96e1fd7fd5541cba2277111830605971c6d8a101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427124"
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

### <a name="properties"></a>Элемент Property

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОЛЛЕКТЕДМСЕС CIM**](cim-collectedmses.md)
</dt> </dl>

 

