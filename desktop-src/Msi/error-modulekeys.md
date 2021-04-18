---
description: Свойство Модулекэйс только для чтения объекта Error возвращает указатель на коллекцию строк, содержащую первичные ключи строки в модуле, вызвавшей ошибку, по одному ключу на запись в коллекции.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Ошибка. свойство Модулекэйс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651746"
---
# <a name="errormodulekeys-property"></a>Ошибка. Модулекэйс, свойство

Свойство **модулекэйс** только для чтения объекта [**Error**](error-object.md) возвращает указатель на коллекцию строк, содержащую первичные ключи строки в модуле, вызвавшей ошибку, по одному ключу на запись в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Клиент несет ответственность за освобождение коллекции строк, когда она больше не нужна.

Если значения не применяются к типу ошибки, коллекция пуста. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение функции \_ модулекэйс**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

