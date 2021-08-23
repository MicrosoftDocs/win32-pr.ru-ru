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
ms.openlocfilehash: 58fb2c2830f016080ac27c48b188bbd1948406a6cb7516b3279c411c87d9c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955723"
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

## <a name="remarks"></a>Remarks

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

 

 
