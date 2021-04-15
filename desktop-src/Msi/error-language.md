---
description: Свойство Language, доступное только для чтения объекта Error, возвращает LANGID текущей ошибки.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Свойство Error. Language (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652043"
---
# <a name="errorlanguage-property"></a>Error. Language, свойство

Свойство **Language** , доступное только для чтения объекта [**Error**](error-object.md) , возвращает **LangID** текущей ошибки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Значение свойства **Language** равно-1, если ошибка не относится к типу Мсмеррорлангуажеунсуппортед или мсмеррорлангуажефаилед. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение \_ языковой функции (объект Error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

