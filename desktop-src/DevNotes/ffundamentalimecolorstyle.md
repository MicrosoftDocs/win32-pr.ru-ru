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
# <a name="ffundamentalimecolorstyle-function"></a><span data-ttu-id="0948f-103">Функция Ффундаменталимеколорстиле</span><span class="sxs-lookup"><span data-stu-id="0948f-103">FFundamentalIMEColorStyle function</span></span>

<span data-ttu-id="0948f-104">Указывает, является ли заданный цвет фундаментальным.</span><span class="sxs-lookup"><span data-stu-id="0948f-104">Specifies whether the specified color is a fundamental color.</span></span>

## <a name="syntax"></a><span data-ttu-id="0948f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0948f-105">Syntax</span></span>


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="0948f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0948f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0948f-107">*пколорстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0948f-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0948f-108">Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="0948f-108">An **IMECOLORSTY** structure returned from the [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0948f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0948f-109">Return value</span></span>

<span data-ttu-id="0948f-110">Возвращает **значение true** , если цвет является фундаментальным.</span><span class="sxs-lookup"><span data-stu-id="0948f-110">Returns **TRUE** when the color is a fundamental color.</span></span>

## <a name="remarks"></a><span data-ttu-id="0948f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0948f-111">Remarks</span></span>

<span data-ttu-id="0948f-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0948f-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0948f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0948f-113">Requirements</span></span>



| <span data-ttu-id="0948f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0948f-114">Requirement</span></span> | <span data-ttu-id="0948f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0948f-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0948f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0948f-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0948f-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0948f-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0948f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0948f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0948f-119">**пколорстилебаккфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="0948f-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="0948f-120">**пколорстилетекстфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="0948f-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
