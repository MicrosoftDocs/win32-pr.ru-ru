---
description: Извлекает стиль цвета фона для указанного стиля.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: Функция Пколорстилебаккфромиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668679"
---
# <a name="pcolorstylebackfromimestyle-function"></a>Функция Пколорстилебаккфромиместиле

Извлекает стиль цвета фона для указанного стиля.

## <a name="syntax"></a>Синтаксис


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
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

Указатель на структуру **имеколорсти** , представляющую стиль цвета фона.

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

 

 
