---
description: Указывает, является ли указанный цвет специальным цветом.
ms.assetid: fda856c4-37b9-444f-9c54-d9eb848a4b05
title: Функция ФспеЦиалимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: af6edf14f4c2167a4609cd8cbb671e85e297368d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648098"
---
# <a name="fspecialimecolorstyle-function"></a>Функция ФспеЦиалимеколорстиле

Указывает, является ли указанный цвет специальным цветом.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FSpecialIMEColorStyle(
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

Возвращает **значение true** , если цвет является специальным цветом.

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

 

 
