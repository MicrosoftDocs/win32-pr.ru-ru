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
# <a name="fspecialimecolorstyle-function"></a><span data-ttu-id="dc4e8-103">Функция ФспеЦиалимеколорстиле</span><span class="sxs-lookup"><span data-stu-id="dc4e8-103">FSpecialIMEColorStyle function</span></span>

<span data-ttu-id="dc4e8-104">Указывает, является ли указанный цвет специальным цветом.</span><span class="sxs-lookup"><span data-stu-id="dc4e8-104">Specifies whether the specified color is a special color.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc4e8-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="dc4e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc4e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4e8-107">*пколорстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc4e8-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4e8-108">Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="dc4e8-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4e8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc4e8-109">Return value</span></span>

<span data-ttu-id="dc4e8-110">Возвращает **значение true** , если цвет является специальным цветом.</span><span class="sxs-lookup"><span data-stu-id="dc4e8-110">Returns **TRUE** when the color is a special color.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4e8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc4e8-111">Remarks</span></span>

<span data-ttu-id="dc4e8-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="dc4e8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4e8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dc4e8-113">Requirements</span></span>



| <span data-ttu-id="dc4e8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dc4e8-114">Requirement</span></span> | <span data-ttu-id="dc4e8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dc4e8-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4e8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="dc4e8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="dc4e8-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e8-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4e8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc4e8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4e8-119">**пколорстилебаккфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="dc4e8-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="dc4e8-120">**пколорстилетекстфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="dc4e8-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
