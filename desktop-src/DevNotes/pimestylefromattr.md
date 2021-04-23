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
# <a name="pimestylefromattr-function"></a><span data-ttu-id="167b4-103">Функция Пиместилефроматтр</span><span class="sxs-lookup"><span data-stu-id="167b4-103">PIMEStyleFromAttr function</span></span>

<span data-ttu-id="167b4-104">Извлекает стили для данного атрибута.</span><span class="sxs-lookup"><span data-stu-id="167b4-104">Retrieves styles for a given attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="167b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="167b4-105">Syntax</span></span>


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a><span data-ttu-id="167b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="167b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="167b4-107">*attr* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="167b4-107">*attr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="167b4-108">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="167b4-108">This parameter can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="167b4-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**Имесаттр \_ ФИКСЕДКОНВЕРТЕД** (5)</span><span class="sxs-lookup"><span data-stu-id="167b4-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR\_FIXEDCONVERTED** (5)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**Имесаттр \_ ВХОДные данные** (0)</span><span class="sxs-lookup"><span data-stu-id="167b4-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR\_INPUT** (0)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**Имесаттр \_ \_Ошибка ввода** (4)</span><span class="sxs-lookup"><span data-stu-id="167b4-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR\_INPUT\_ERROR** (4)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**Имесаттр \_ MAX** (5)</span><span class="sxs-lookup"><span data-stu-id="167b4-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR\_MAX** (5)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**Имесаттр \_ MIN** (0)</span><span class="sxs-lookup"><span data-stu-id="167b4-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR\_MIN** (0)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**Имесаттр \_ \_Преобразование целевого объекта** (1)</span><span class="sxs-lookup"><span data-stu-id="167b4-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR\_TARGET\_CONVERTED** (1)</span></span>
</dt> <dt>

<span data-ttu-id="167b4-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**Имесаттр \_ Целевой \_ нотконвертед** (4)</span><span class="sxs-lookup"><span data-stu-id="167b4-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR\_TARGET\_NOTCONVERTED** (4)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="167b4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="167b4-116">Return value</span></span>

<span data-ttu-id="167b4-117">Возвращает указатель на структуру **иместиле** , представляющую цвет и параметры, не относящиеся к цвету.</span><span class="sxs-lookup"><span data-stu-id="167b4-117">Returns a pointer to an **IMESTYLE** structure representing the color and non-color settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="167b4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="167b4-118">Remarks</span></span>

<span data-ttu-id="167b4-119">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="167b4-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="167b4-120">Структура **иместиле** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="167b4-120">The **IMESTYLE** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="167b4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="167b4-121">Requirements</span></span>



| <span data-ttu-id="167b4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="167b4-122">Requirement</span></span> | <span data-ttu-id="167b4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="167b4-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="167b4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="167b4-124">DLL</span></span><br/> | <dl> <span data-ttu-id="167b4-125"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="167b4-125"><dt>Imeshare.dll</dt></span></span> </dl> |



 

 
