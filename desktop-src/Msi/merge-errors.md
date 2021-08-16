---
description: Свойство ошибки только для чтения объекта Merge Возвращает коллекцию объектов Error, которые являются текущим набором ошибок.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Свойство MERGE. Errors (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3a6abd02a59582a9fbbc65772d781c93ec68f7ffd29cf165cb624daf7d5c6a3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628912"
---
# <a name="mergeerrors-property"></a>Свойство MERGE. Errors

Свойство **ошибки** только для чтения объекта [**Merge**](merge-object.md) Возвращает коллекцию объектов [**Error**](error-object.md) , которые являются текущим набором ошибок.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Извлечение является обратимым. Несколько экземпляров коллекции ошибок могут быть извлечены путем многократного вызова этого метода.

### <a name="c"></a>C++

См. раздел [**Get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
