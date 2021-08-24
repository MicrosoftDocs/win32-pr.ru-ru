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
ms.openlocfilehash: 7922f60d347a91b461031d1a56cc51b9630389e99fbef778a8f75007b17f1558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795174"
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

 

 
