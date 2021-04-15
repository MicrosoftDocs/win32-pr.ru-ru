---
description: Указывает, является ли заданный цвет фундаментальным.
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: Функция Ффундаменталимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c7de1bf4ef84d159d673e1039ad6ea328153b216
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648777"
---
# <a name="ffundamentalimecolorstyle-function"></a>Функция Ффундаменталимеколорстиле

Указывает, является ли заданный цвет фундаментальным.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
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

Возвращает **значение true** , если цвет является фундаментальным.

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

 

 
