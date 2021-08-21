---
description: Абстрактный класс для подклассов, представляющих коллекцию объектов CIM \_ манажедсистемелемент. Эти коллекции позволяют группировать управляемые системные элементы для целей идентификации и упростить сопоставление параметров и конфигураций.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Класс CIM_CollectionOfMSEs (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8598b8208b9291ec9dabc405f1b1c8d18513ff111e22ec8caa6c8bf32fb946f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813327"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>Класс CIM_CollectionOfMSEs (Управление Hyper-V)

Абстрактный класс для подклассов, представляющих коллекцию объектов [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) . Эти коллекции позволяют группировать управляемые системные элементы для целей идентификации и упростить сопоставление параметров и конфигураций.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ коллектионофмсес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ коллектионофмсес** имеет следующие свойства.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Идентификация объекта коллекции. При создании подкласса свойство **CollectionID** может быть переопределено как свойство ключа.

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

[**\_Коллекция CIM**](cim-collection.md)
</dt> </dl>

 

