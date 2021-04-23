---
description: Метод Упдатеколауртабле обновляет таблицу цветов с помощью новой палитры.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Кдравимаже. Упдатеколауртабле, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669494"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="d708f-103">Кдравимаже. Упдатеколауртабле, метод</span><span class="sxs-lookup"><span data-stu-id="d708f-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="d708f-104">`UpdateColourTable`Метод обновляет таблицу цветов с помощью новой палитры.</span><span class="sxs-lookup"><span data-stu-id="d708f-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="d708f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d708f-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="d708f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d708f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d708f-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="d708f-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="d708f-108">Контекст устройства, содержащий изображение.</span><span class="sxs-lookup"><span data-stu-id="d708f-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="d708f-109">*пбми*</span><span class="sxs-lookup"><span data-stu-id="d708f-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="d708f-110">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , содержащую новую палитру.</span><span class="sxs-lookup"><span data-stu-id="d708f-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d708f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d708f-111">Return value</span></span>

<span data-ttu-id="d708f-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d708f-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d708f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d708f-113">Requirements</span></span>



| <span data-ttu-id="d708f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d708f-114">Requirement</span></span> | <span data-ttu-id="d708f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d708f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d708f-116">Header</span><span class="sxs-lookup"><span data-stu-id="d708f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d708f-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d708f-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d708f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d708f-118">Library</span></span><br/> | <dl> <span data-ttu-id="d708f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d708f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d708f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d708f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d708f-121">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="d708f-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




