---
description: Метод конструктора Цимажепалетте. Цимажепалетте.
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
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085682"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="aafbb-103">Цимажепалетте. Цимажепалетте, конструктор</span><span class="sxs-lookup"><span data-stu-id="aafbb-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="aafbb-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="aafbb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafbb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aafbb-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="aafbb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aafbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aafbb-107">*пбасефилтер*</span><span class="sxs-lookup"><span data-stu-id="aafbb-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="aafbb-108">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="aafbb-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="aafbb-109">*пбасевиндов*</span><span class="sxs-lookup"><span data-stu-id="aafbb-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="aafbb-110">Указатель на объект **кбасевиндов** , который управляет окном, в котором реализована палитра.</span><span class="sxs-lookup"><span data-stu-id="aafbb-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="aafbb-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aafbb-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aafbb-112">*пдравимаже*</span><span class="sxs-lookup"><span data-stu-id="aafbb-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="aafbb-113">Указатель на объект **кдравимаже** , который рисует изображение видео.</span><span class="sxs-lookup"><span data-stu-id="aafbb-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="aafbb-114">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aafbb-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aafbb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="aafbb-115">Requirements</span></span>



| <span data-ttu-id="aafbb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="aafbb-116">Requirement</span></span> | <span data-ttu-id="aafbb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="aafbb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aafbb-118">Header</span><span class="sxs-lookup"><span data-stu-id="aafbb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aafbb-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aafbb-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aafbb-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aafbb-120">Library</span></span><br/> | <dl> <span data-ttu-id="aafbb-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="aafbb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aafbb-122">См. также</span><span class="sxs-lookup"><span data-stu-id="aafbb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafbb-123">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="aafbb-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




