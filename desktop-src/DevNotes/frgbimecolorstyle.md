---
description: Указывает, является ли указанный цвет цветом RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Функция Фргбимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648752"
---
# <a name="frgbimecolorstyle-function"></a>Функция Фргбимеколорстиле

Указывает, является ли указанный цвет цветом RGB.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FRGBIMEColorStyle(
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

Возвращает **значение true** , если цвет является цветом RGB.

## <a name="remarks"></a>Комментарии

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

 

 
