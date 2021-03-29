---
description: Указывает, является ли указанный цвет цветом специального окна.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: Функция ФспеЦиалвиндовимеколорстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fb667186789361a106a23f8daa82088b9bcb2ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648116"
---
# <a name="fspecialwindowimecolorstyle-function"></a><span data-ttu-id="1b223-103">Функция ФспеЦиалвиндовимеколорстиле</span><span class="sxs-lookup"><span data-stu-id="1b223-103">FSpecialWindowIMEColorStyle function</span></span>

<span data-ttu-id="1b223-104">Указывает, является ли указанный цвет цветом специального окна.</span><span class="sxs-lookup"><span data-stu-id="1b223-104">Specifies whether the specified color is a special window color.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b223-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b223-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="1b223-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b223-107">*пколорстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b223-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b223-108">Структура **имеколорсти** , возвращаемая функцией [**пколорстилебаккфромиместиле**](pcolorstylebackfromimestyle.md) или [**пколорстилетекстфромиместиле**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="1b223-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b223-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b223-109">Return value</span></span>

<span data-ttu-id="1b223-110">Возвращает **значение true** , если цвет является цветом специального окна (один из специальных цветов).</span><span class="sxs-lookup"><span data-stu-id="1b223-110">Returns **TRUE** when the color is a special window color (one of special color).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b223-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b223-111">Remarks</span></span>

<span data-ttu-id="1b223-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1b223-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b223-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1b223-113">Requirements</span></span>



| <span data-ttu-id="1b223-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1b223-114">Requirement</span></span> | <span data-ttu-id="1b223-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1b223-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b223-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1b223-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1b223-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b223-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b223-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b223-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b223-119">**пколорстилебаккфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="1b223-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="1b223-120">**пколорстилетекстфромиместиле**</span><span class="sxs-lookup"><span data-stu-id="1b223-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
