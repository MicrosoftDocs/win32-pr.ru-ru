---
description: Метод конструктора.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Конструктор Цимажепалетте. Цимажепалетте (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679823"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="cadb3-103">Цимажепалетте. Цимажепалетте, конструктор</span><span class="sxs-lookup"><span data-stu-id="cadb3-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="cadb3-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="cadb3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cadb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cadb3-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="cadb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cadb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadb3-107">*пбасефилтер*</span><span class="sxs-lookup"><span data-stu-id="cadb3-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="cadb3-108">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="cadb3-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="cadb3-109">*пбасевиндов*</span><span class="sxs-lookup"><span data-stu-id="cadb3-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="cadb3-110">Указатель на объект **кбасевиндов** , который управляет окном, в котором реализована палитра.</span><span class="sxs-lookup"><span data-stu-id="cadb3-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="cadb3-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cadb3-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cadb3-112">*пдравимаже*</span><span class="sxs-lookup"><span data-stu-id="cadb3-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="cadb3-113">Указатель на объект **кдравимаже** , который рисует изображение видео.</span><span class="sxs-lookup"><span data-stu-id="cadb3-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="cadb3-114">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cadb3-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cadb3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cadb3-115">Requirements</span></span>



| <span data-ttu-id="cadb3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cadb3-116">Requirement</span></span> | <span data-ttu-id="cadb3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cadb3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cadb3-118">Header</span><span class="sxs-lookup"><span data-stu-id="cadb3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cadb3-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cadb3-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cadb3-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cadb3-120">Library</span></span><br/> | <dl> <span data-ttu-id="cadb3-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cadb3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadb3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cadb3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cadb3-123">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="cadb3-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




