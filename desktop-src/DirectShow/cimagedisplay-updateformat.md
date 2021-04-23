---
description: Метод Упдатеформат заполняет некоторые необязательные элементы структуры ВИДЕОИНФО.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Цимажедисплай. Упдатеформат, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657347"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="4ee69-103">Цимажедисплай. Упдатеформат, метод</span><span class="sxs-lookup"><span data-stu-id="4ee69-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="4ee69-104">`UpdateFormat`Метод заполняет некоторые необязательные элементы структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="4ee69-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ee69-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4ee69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ee69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee69-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="4ee69-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee69-108">Указатель на структуру **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="4ee69-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee69-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ee69-109">Return value</span></span>

<span data-ttu-id="4ee69-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4ee69-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee69-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ee69-111">Remarks</span></span>

<span data-ttu-id="4ee69-112">Этот метод задает для элементов **биклрусед**, **биклримпортант** и **бисизеимаже** правильные значения и очищает исходный и целевой прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="4ee69-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee69-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4ee69-113">Requirements</span></span>



| <span data-ttu-id="4ee69-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4ee69-114">Requirement</span></span> | <span data-ttu-id="4ee69-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4ee69-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee69-116">Header</span><span class="sxs-lookup"><span data-stu-id="4ee69-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4ee69-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee69-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ee69-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ee69-118">Library</span></span><br/> | <dl> <span data-ttu-id="4ee69-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee69-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee69-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ee69-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee69-121">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="4ee69-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




