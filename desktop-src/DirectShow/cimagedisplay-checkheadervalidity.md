---
description: Метод Чеккхеадервалидити проверяет структуру БИТМАПИНФОХЕАДЕР. Этот метод полезен только для несжатых типов RGB, а не для сжатых типов или YUV-типов.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Цимажедисплай. Чеккхеадервалидити, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674992"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="b0360-104">Цимажедисплай. Чеккхеадервалидити, метод</span><span class="sxs-lookup"><span data-stu-id="b0360-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="b0360-105">`CheckHeaderValidity`Метод проверяет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="b0360-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="b0360-106">Этот метод полезен только для несжатых типов RGB, а не для сжатых типов или YUV-типов.</span><span class="sxs-lookup"><span data-stu-id="b0360-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0360-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0360-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="b0360-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0360-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0360-109">*пинпут*</span><span class="sxs-lookup"><span data-stu-id="b0360-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="b0360-110">Указатель на структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , содержащую структуру **битмапинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="b0360-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0360-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0360-111">Return value</span></span>

<span data-ttu-id="b0360-112">Возвращает **значение true** , если **битмапинфохеадер** является допустимым, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b0360-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0360-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0360-113">Remarks</span></span>

<span data-ttu-id="b0360-114">Этот метод проверяет, что размеры изображения не отрицательны; тип сжатия — BI \_ RGB или BI \_ битовых полей; глубина цвета и цветовая маска являются допустимыми; элемент **бипланес** равен единице, а элементы **бисизе** и **бисизеимаже** являются правильными.</span><span class="sxs-lookup"><span data-stu-id="b0360-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="b0360-115">Он также проверяет наличие типичных ошибок в записях палитры, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="b0360-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0360-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b0360-116">Requirements</span></span>



| <span data-ttu-id="b0360-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b0360-117">Requirement</span></span> | <span data-ttu-id="b0360-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b0360-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0360-119">Header</span><span class="sxs-lookup"><span data-stu-id="b0360-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b0360-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0360-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0360-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0360-121">Library</span></span><br/> | <dl> <span data-ttu-id="b0360-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b0360-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0360-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0360-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0360-124">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="b0360-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




