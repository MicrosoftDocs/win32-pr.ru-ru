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
ms.openlocfilehash: 075fba028dd045c831adb84a7133fd524398fc74037b7e3c31116b76a4c95a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086044"
---
# <a name="errordatabasekeys-property"></a>Ошибка. Датабасекэйс, свойство

Свойство **датабасекэйс** только для чтения объекта [**Error**](error-object.md) Возвращает коллекцию строк, содержащую первичные ключи строки базы данных, вызвавшей ошибку. В коллекции имеется один ключ для каждой записи.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Клиент несет ответственность за освобождение коллекции строк, когда она больше не нужна.

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ датабасекэйс**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

