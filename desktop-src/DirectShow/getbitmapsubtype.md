---
description: Функция Жетбитмапсубтипе возвращает идентификатор GUID подтипа носителя для указанного точечного рисунка.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Функция Жетбитмапсубтипе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675526"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="1ad27-103">Функция Жетбитмапсубтипе</span><span class="sxs-lookup"><span data-stu-id="1ad27-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="1ad27-104">`GetBitmapSubtype`Функция возвращает **идентификатор GUID** подтипа носителя для указанного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="1ad27-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ad27-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="1ad27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ad27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad27-107">*феадер*</span><span class="sxs-lookup"><span data-stu-id="1ad27-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad27-108">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="1ad27-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad27-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ad27-109">Return value</span></span>

<span data-ttu-id="1ad27-110">Возвращает **GUID** подтипа носителя.</span><span class="sxs-lookup"><span data-stu-id="1ad27-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad27-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ad27-111">Remarks</span></span>

<span data-ttu-id="1ad27-112">Для несжатых типов RGB эта функция сопоставляет поле **бибиткаунт** с подтипом.</span><span class="sxs-lookup"><span data-stu-id="1ad27-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="1ad27-113">Для типов сжатых видео эта функция использует класс [**фаурккмап**](fourccmap.md) для соответствия поля **бикомпрессион** подтипу.</span><span class="sxs-lookup"><span data-stu-id="1ad27-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="1ad27-114">Если функция не может соответствовать формату подтипа, возвращаемое значение — GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="1ad27-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad27-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1ad27-115">Requirements</span></span>



| <span data-ttu-id="1ad27-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad27-116">Requirement</span></span> | <span data-ttu-id="1ad27-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad27-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad27-118">Header</span><span class="sxs-lookup"><span data-stu-id="1ad27-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ad27-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ad27-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1ad27-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ad27-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ad27-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1ad27-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad27-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ad27-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad27-123">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="1ad27-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




