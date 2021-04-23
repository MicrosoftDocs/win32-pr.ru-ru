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
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="c5214-103">Функция Пколорстилебаккфромиместиле</span><span class="sxs-lookup"><span data-stu-id="c5214-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="c5214-104">Извлекает стиль цвета фона для указанного стиля.</span><span class="sxs-lookup"><span data-stu-id="c5214-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5214-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5214-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="c5214-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5214-107">*пиместиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5214-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5214-108">Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="c5214-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5214-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5214-109">Return value</span></span>

<span data-ttu-id="c5214-110">Указатель на структуру **имеколорсти** , представляющую стиль цвета фона.</span><span class="sxs-lookup"><span data-stu-id="c5214-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5214-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5214-111">Remarks</span></span>

<span data-ttu-id="c5214-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c5214-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="c5214-113">Структура **имеколорсти** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c5214-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="c5214-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c5214-114">Requirements</span></span>



| <span data-ttu-id="c5214-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c5214-115">Requirement</span></span> | <span data-ttu-id="c5214-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c5214-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5214-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c5214-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c5214-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5214-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5214-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5214-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5214-120">**пиместилефроматтр**</span><span class="sxs-lookup"><span data-stu-id="c5214-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
