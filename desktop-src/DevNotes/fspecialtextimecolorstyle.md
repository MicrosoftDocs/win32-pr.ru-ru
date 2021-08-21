---
description: Указывает, является ли указанный цвет специальным цветом текста.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Функция ФспеЦиалтекстимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fa964ba5d1020a5d9ba35b7359d81d965778b8a1e1f546a0a6cac19d2611ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017732"
---
# <a name="fspecialtextimecolorstyle-function"></a>Функция ФспеЦиалтекстимеколорстиле

Указывает, является ли указанный цвет специальным цветом текста.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пколорстиле* \[ окне\]
</dt> <dd>

Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если цвет является специальным цветом текста.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
