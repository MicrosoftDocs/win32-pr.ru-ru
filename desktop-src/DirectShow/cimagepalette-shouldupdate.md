---
description: Метод Шаулдупдате определяет, требуется ли создать новую палитру.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Цимажепалетте. Шаулдупдате, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665231"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="f78dc-103">Цимажепалетте. Шаулдупдате, метод</span><span class="sxs-lookup"><span data-stu-id="f78dc-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="f78dc-104">`ShouldUpdate`Метод определяет, нужно ли создавать новую палитру.</span><span class="sxs-lookup"><span data-stu-id="f78dc-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f78dc-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f78dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f78dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f78dc-107">*пневинфо*</span><span class="sxs-lookup"><span data-stu-id="f78dc-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f78dc-108">Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую новую таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="f78dc-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="f78dc-109">*полдинфо*</span><span class="sxs-lookup"><span data-stu-id="f78dc-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f78dc-110">Указатель на структуру **видеоинфохеадер** , содержащую старую таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="f78dc-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="f78dc-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f78dc-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f78dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f78dc-112">Return value</span></span>

<span data-ttu-id="f78dc-113">Возвращает **значение true** , если требуется обновить палитру, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f78dc-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78dc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f78dc-114">Remarks</span></span>

-   <span data-ttu-id="f78dc-115">Если ни одна из структур **видеоинфохеадер** не содержит таблицу цветов, метод возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f78dc-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="f78dc-116">Если только одна структура содержит таблицу цветов или если *полдинфо* имеет **значение NULL**, метод возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f78dc-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="f78dc-117">Если обе структуры содержат таблицы цветов, а записи цветов совпадают, метод возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f78dc-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="f78dc-118">Если обе структуры содержат таблицы цветов, но записи цветов не совпадают, метод возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f78dc-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78dc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f78dc-119">Requirements</span></span>



| <span data-ttu-id="f78dc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f78dc-120">Requirement</span></span> | <span data-ttu-id="f78dc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f78dc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78dc-122">Header</span><span class="sxs-lookup"><span data-stu-id="f78dc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f78dc-123"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f78dc-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f78dc-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f78dc-124">Library</span></span><br/> | <dl> <span data-ttu-id="f78dc-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f78dc-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f78dc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f78dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78dc-127">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="f78dc-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




