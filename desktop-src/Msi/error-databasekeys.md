---
description: Свойство Датабасекэйс только для чтения объекта Error Возвращает коллекцию строк, содержащую первичные ключи строки базы данных, вызвавшей ошибку. В коллекции имеется один ключ для каждой записи.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Ошибка. свойство Датабасекэйс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651580"
---
# <a name="errordatabasekeys-property"></a>Ошибка. Датабасекэйс, свойство

Свойство **датабасекэйс** только для чтения объекта [**Error**](error-object.md) Возвращает коллекцию строк, содержащую первичные ключи строки базы данных, вызвавшей ошибку. В коллекции имеется один ключ для каждой записи.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Клиент несет ответственность за освобождение коллекции строк, когда она больше не нужна.

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ датабасекэйс**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

