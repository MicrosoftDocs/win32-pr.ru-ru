---
description: Метод ВИДЕОИНФО извлекает цветовую маску для указанного формата.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Метод Цимажедисплай. с битовой маски (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658002"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="c6a1b-103">Цимажедисплай..., метод</span><span class="sxs-lookup"><span data-stu-id="c6a1b-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="c6a1b-104">`GetBitMasks`Метод извлекает цветовую маску для указанного формата [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c6a1b-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6a1b-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c6a1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6a1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a1b-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="c6a1b-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a1b-108">Указатель на структуру **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="c6a1b-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a1b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6a1b-109">Return value</span></span>

<span data-ttu-id="c6a1b-110">Возвращает массив из трех значений **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c6a1b-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a1b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6a1b-111">Remarks</span></span>

<span data-ttu-id="c6a1b-112">Если элемент **бикомпрессион** является BI \_ битовых полей, метод возвращает указатель на цветовую маску, переданную в элементе **двбитмаскс** .</span><span class="sxs-lookup"><span data-stu-id="c6a1b-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="c6a1b-113">Если элемент **бикомпрессион** является BI \_ RGB, метод возвращает цветовые маски, соответствующие глубине цвета.</span><span class="sxs-lookup"><span data-stu-id="c6a1b-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="c6a1b-114">Если метод завершается ошибкой (например, глубина разрядности меньше 16), метод возвращает массив {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="c6a1b-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a1b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c6a1b-115">Requirements</span></span>



| <span data-ttu-id="c6a1b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c6a1b-116">Requirement</span></span> | <span data-ttu-id="c6a1b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c6a1b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a1b-118">Header</span><span class="sxs-lookup"><span data-stu-id="c6a1b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c6a1b-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6a1b-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6a1b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6a1b-120">Library</span></span><br/> | <dl> <span data-ttu-id="c6a1b-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c6a1b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a1b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6a1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a1b-123">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="c6a1b-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




