---
description: Преобразует структуру ИМЕКОЛОРСТИ в структуру COLORREF.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: Функция Ргбфромимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647967"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="78f43-103">Функция Ргбфромимеколорстиле</span><span class="sxs-lookup"><span data-stu-id="78f43-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="78f43-104">Преобразует структуру **имеколорсти** в структуру [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="78f43-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78f43-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="78f43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78f43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f43-107">*пколорстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78f43-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f43-108">Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="78f43-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f43-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78f43-109">Return value</span></span>

<span data-ttu-id="78f43-110">Возвращает структуру [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="78f43-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f43-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78f43-111">Remarks</span></span>

<span data-ttu-id="78f43-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="78f43-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f43-113">Требования</span><span class="sxs-lookup"><span data-stu-id="78f43-113">Requirements</span></span>



| <span data-ttu-id="78f43-114">Требование</span><span class="sxs-lookup"><span data-stu-id="78f43-114">Requirement</span></span> | <span data-ttu-id="78f43-115">Значение</span><span class="sxs-lookup"><span data-stu-id="78f43-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f43-116">DLL</span><span class="sxs-lookup"><span data-stu-id="78f43-116">DLL</span></span><br/> | <dl> <span data-ttu-id="78f43-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f43-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f43-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78f43-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f43-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="78f43-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="78f43-120">**пколорстилебаккфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="78f43-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="78f43-121">**пколорстилетекстфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="78f43-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
