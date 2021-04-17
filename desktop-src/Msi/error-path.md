---
description: В установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой. Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Свойство Error. Path (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685308"
---
# <a name="errorpath-property"></a>Свойство Error. Path

В установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой. Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Это значение допустимо только для ошибок типа Мсмеррорфилекреате или Мсмеррордиркреате. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение \_ пути**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

