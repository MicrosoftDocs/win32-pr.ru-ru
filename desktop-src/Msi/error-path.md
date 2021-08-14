---
description: в установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой. Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.
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
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378155"
---
# <a name="errorpath-property"></a>Свойство Error. Path

в установщик Windows версии 1,0 и 1,1 свойство Path всегда является пустой строкой. Будущие версии могут использовать это значение для возврата пути к файлу или каталогу, который не удалось создать.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Это значение допустимо только для ошибок типа Мсмеррорфилекреате или Мсмеррордиркреате. Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .

### <a name="c"></a>C++

См. раздел [**Получение \_ пути**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

