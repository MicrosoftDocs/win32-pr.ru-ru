---
description: Указывает, имеет ли стиль, не являющийся цветом, стиль курсивом.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Функция ФиталиЦиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c8160edf46b97544ef27558bf15a8a58e447e78a0e0709432aea840f4567bc0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076118"
---
# <a name="fitalicimestyle-function"></a>Функция ФиталиЦиместиле

Указывает, имеет ли стиль, не являющийся цветом, стиль курсивом.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиместиле* \[ окне\]
</dt> <dd>

Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если стиль имеет курсив.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**пиместилефроматтр**](pimestylefromattr.md)
</dt> </dl>

 

 
