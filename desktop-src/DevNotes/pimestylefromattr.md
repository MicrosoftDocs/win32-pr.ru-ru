---
description: Извлекает стили для данного атрибута.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: Функция Пиместилефроматтр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647978"
---
# <a name="pimestylefromattr-function"></a>Функция Пиместилефроматтр

Извлекает стили для данного атрибута.

## <a name="syntax"></a>Синтаксис


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*attr* \[ окне\]
</dt> <dd>

Этот параметр может принимать одно из указанных ниже значений.

<dl> <dt>

<span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**Имесаттр \_ ФИКСЕДКОНВЕРТЕД** (5)
</dt> <dt>

<span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**Имесаттр \_ ВХОДные данные** (0)
</dt> <dt>

<span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**Имесаттр \_ \_Ошибка ввода** (4)
</dt> <dt>

<span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**Имесаттр \_ MAX** (5)
</dt> <dt>

<span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**Имесаттр \_ MIN** (0)
</dt> <dt>

<span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**Имесаттр \_ \_Преобразование целевого объекта** (1)
</dt> <dt>

<span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**Имесаттр \_ Целевой \_ нотконвертед** (4)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на структуру **иместиле** , представляющую цвет и параметры, не относящиеся к цвету.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Структура **иместиле** определяется следующим образом:

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



 

 
