---
description: Указывает, является ли указанный цвет специальным цветом текста.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Функция ФспеЦиалтекстимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648097"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="958f2-103">Функция ФспеЦиалтекстимеколорстиле</span><span class="sxs-lookup"><span data-stu-id="958f2-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="958f2-104">Указывает, является ли указанный цвет специальным цветом текста.</span><span class="sxs-lookup"><span data-stu-id="958f2-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="958f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="958f2-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="958f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="958f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958f2-107">*пколорстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="958f2-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958f2-108">Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="958f2-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958f2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="958f2-109">Return value</span></span>

<span data-ttu-id="958f2-110">Возвращает **значение true** , если цвет является специальным цветом текста.</span><span class="sxs-lookup"><span data-stu-id="958f2-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="958f2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="958f2-111">Remarks</span></span>

<span data-ttu-id="958f2-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="958f2-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="958f2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="958f2-113">Requirements</span></span>



| <span data-ttu-id="958f2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="958f2-114">Requirement</span></span> | <span data-ttu-id="958f2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="958f2-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="958f2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="958f2-116">DLL</span></span><br/> | <dl> <span data-ttu-id="958f2-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="958f2-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="958f2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="958f2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958f2-119">**пколорстилебаккфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="958f2-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="958f2-120">**пколорстилетекстфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="958f2-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
