---
description: Получает стиль цвета текста для указанного стиля.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Функция Пколорстилетекстфромиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648874"
---
# <a name="pcolorstyletextfromimestyle-function"></a>Функция Пколорстилетекстфромиместиле

Получает стиль цвета текста для указанного стиля.

## <a name="syntax"></a>Синтаксис


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
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

Указатель на структуру **имеколорсти** , представляющую стиль цвета текста.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Структура **имеколорсти** определяется следующим образом:

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пиместилефроматтр**](pimestylefromattr.md)
</dt> </dl>

 

 
