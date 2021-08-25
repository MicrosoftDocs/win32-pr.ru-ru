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
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082894"
---
# <a name="errorlanguage-property"></a>Error. Language, свойство

Свойство **Language** , доступное только для чтения объекта [**Error**](error-object.md) , возвращает **LangID** текущей ошибки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Значение свойства **Language** равно-1, если ошибка не относится к типу Мсмеррорлангуажеунсуппортед или мсмеррорлангуажефаилед. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение \_ языковой функции (объект Error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

