---
description: Метод Чеккпалеттехеадер проверяет записи палитры в структуре ВИДЕОИНФО.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Цимажедисплай. Чеккпалеттехеадер, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679741"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="03262-103">Цимажедисплай. Чеккпалеттехеадер, метод</span><span class="sxs-lookup"><span data-stu-id="03262-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="03262-104">`CheckPaletteHeader`Метод проверяет записи палитры в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="03262-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="03262-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03262-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="03262-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03262-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03262-107">*пинпут*</span><span class="sxs-lookup"><span data-stu-id="03262-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="03262-108">Указатель на структуру **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="03262-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03262-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03262-109">Return value</span></span>

<span data-ttu-id="03262-110">Возвращает **значение true** , если записи палитры допустимы, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="03262-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="03262-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03262-111">Remarks</span></span>

<span data-ttu-id="03262-112">Если формат изображения не палеттизед, метод проверяет, что **биклрусед** равен нулю.</span><span class="sxs-lookup"><span data-stu-id="03262-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="03262-113">В противном случае метод проверяет, что флаг **бикомпрессион** — это BI \_ RGB; **биклримпортант** не превышает **биклрусед**; и число записей в палитре не превышает максимальное значение, учитывая глубину цвета.</span><span class="sxs-lookup"><span data-stu-id="03262-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="03262-114">Требования</span><span class="sxs-lookup"><span data-stu-id="03262-114">Requirements</span></span>



| <span data-ttu-id="03262-115">Требование</span><span class="sxs-lookup"><span data-stu-id="03262-115">Requirement</span></span> | <span data-ttu-id="03262-116">Значение</span><span class="sxs-lookup"><span data-stu-id="03262-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03262-117">Header</span><span class="sxs-lookup"><span data-stu-id="03262-117">Header</span></span><br/>  | <dl> <span data-ttu-id="03262-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03262-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03262-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03262-119">Library</span></span><br/> | <dl> <span data-ttu-id="03262-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="03262-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03262-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03262-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03262-122">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="03262-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




