---
description: Свойство Датабасетабле только для чтения объекта Error возвращает имя таблицы в базе данных, вызвавшей ошибку.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Ошибка. свойство Датабасетабле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651579"
---
# <a name="errordatabasetable-property"></a>Ошибка. Датабасетабле, свойство

Свойство **датабасетабле** только для чтения объекта [**Error**](error-object.md) возвращает имя таблицы в базе данных, вызвавшей ошибку.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ датабасетабле**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

