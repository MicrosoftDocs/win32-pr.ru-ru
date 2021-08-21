---
description: Перемещает виртуальный жесткий диск из источника в конечный путь.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Класс Msvm_MoveUnmanagedVhd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e631b95c9961262df288b76cf83f953589780c2feb294e940314d08975bcfd57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521124"
---
# <a name="msvm_moveunmanagedvhd-class"></a>\_Класс мсвм мовеунманажедвхд

Перемещает виртуальный жесткий диск из источника в конечный путь.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ мовеунманажедвхд** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ мовеунманажедвхд** имеет следующие свойства.

<dl> <dt>

**вхддестинатионпас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Целевой путь.

</dd> <dt>

**вхдсаурцепас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Исходный путь к перемещаемому виртуальному жесткому диску.

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

[**\_МАНАЖЕДЕЛЕМЕНТ CIM**](cim-managedelement.md)
</dt> </dl>

 

 




