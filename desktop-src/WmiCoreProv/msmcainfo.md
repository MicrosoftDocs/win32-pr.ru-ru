---
description: Абстрактный базовый класс, из которого производятся все классы данных поставщика (MCA), например Мсмкаинфо \_ равмкадата. этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Класс Мсмкаинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cef9878ea8e9dd6c11c6b18a62d332e17f24810548360e0edb9c117e02a710c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051192"
---
# <a name="msmcainfo-class"></a>Класс Мсмкаинфо

Класс **мсмкаинфо** является абстрактным базовым классом, из которого производятся все классы данных поставщика (например, [**мсмкаинфо \_ равмкадата**](msmcainfo-rawmcadata.md)). Поставщик MCA также имеет классы событий, производные от [**WMIEvent**](wmievent.md). этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Члены

Класс **мсмкаинфо** не определяет никаких членов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы МСМКА](msmca-classes.md)
</dt> <dt>

[**\_Заголовок мсмкаевент**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




