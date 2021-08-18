---
description: Свойство Модулетабле только для чтения возвращает имя таблицы в модуле, вызвавшем ошибку.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Ошибка. свойство Модулетабле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 47cd9bab5c12230a048da04e60169e1ad21195df2304642f6b656983539f3b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947076"
---
# <a name="errormoduletable-property"></a>Ошибка. Модулетабле, свойство

Свойство **модулетабле** только для чтения возвращает имя таблицы в модуле, вызвавшем ошибку.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ модулетабле**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

