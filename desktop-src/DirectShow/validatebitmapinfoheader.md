---
description: Функция Валидатебитмапинфохеадер проверяет структуру БИТМАПИНФОХЕАДЕР для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Функция Валидатебитмапинфохеадер (Чеккбми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679984"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="71024-103">Функция Валидатебитмапинфохеадер</span><span class="sxs-lookup"><span data-stu-id="71024-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="71024-104">`ValidateBitmapInfoHeader`Функция проверяет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="71024-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="71024-105">Эта функция не гарантирует, что структура [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) является допустимой или что код, использующий структуру, является безопасным.</span><span class="sxs-lookup"><span data-stu-id="71024-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="71024-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71024-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="71024-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71024-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71024-108">*пбми*</span><span class="sxs-lookup"><span data-stu-id="71024-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="71024-109">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) для проверки.</span><span class="sxs-lookup"><span data-stu-id="71024-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="71024-110">*кбсизе*</span><span class="sxs-lookup"><span data-stu-id="71024-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="71024-111">Размер блока памяти, в котором хранится структура, в байтах.</span><span class="sxs-lookup"><span data-stu-id="71024-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71024-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71024-112">Return value</span></span>

<span data-ttu-id="71024-113">Возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="71024-113">Returns a Boolean value.</span></span> <span data-ttu-id="71024-114">Если значение равно **false**, структура [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) недопустима.</span><span class="sxs-lookup"><span data-stu-id="71024-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="71024-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71024-115">Remarks</span></span>

<span data-ttu-id="71024-116">Эта функция защищает от следующих ошибок:</span><span class="sxs-lookup"><span data-stu-id="71024-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="71024-117">Арифметическое переполнение при размере структуры или недопустимом размере структуры.</span><span class="sxs-lookup"><span data-stu-id="71024-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="71024-118">Недопустимое значение для элемента **биклрусед** .</span><span class="sxs-lookup"><span data-stu-id="71024-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="71024-119">Арифметическое переполнение в размере изображения (**бисизеимаже**).</span><span class="sxs-lookup"><span data-stu-id="71024-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="71024-120">Недопустимые значения для размера изображения (**бисизеимаже**) для форматов RGB.</span><span class="sxs-lookup"><span data-stu-id="71024-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="71024-121">Функция не проверяет, описывает ли структура допустимый формат видео.</span><span class="sxs-lookup"><span data-stu-id="71024-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="71024-122">Требования</span><span class="sxs-lookup"><span data-stu-id="71024-122">Requirements</span></span>



| <span data-ttu-id="71024-123">Требование</span><span class="sxs-lookup"><span data-stu-id="71024-123">Requirement</span></span> | <span data-ttu-id="71024-124">Значение</span><span class="sxs-lookup"><span data-stu-id="71024-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71024-125">Header</span><span class="sxs-lookup"><span data-stu-id="71024-125">Header</span></span><br/> | <dl> <span data-ttu-id="71024-126"><dt>Чеккбми. h</dt></span><span class="sxs-lookup"><span data-stu-id="71024-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71024-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71024-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71024-128">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="71024-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




