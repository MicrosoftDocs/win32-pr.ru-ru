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
ms.openlocfilehash: b9e52523b37c90de4c4592fdeb059e6269f4e05e240242e69e14f0be6d4d53a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378175"
---
# <a name="errordatabasetable-property"></a>Ошибка. Датабасетабле, свойство

Свойство **датабасетабле** только для чтения объекта [**Error**](error-object.md) возвращает имя таблицы в базе данных, вызвавшей ошибку.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ датабасетабле**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

