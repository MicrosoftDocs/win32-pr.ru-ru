---
description: Метод Препарепалетте настраивает палитру на основе типа носителя из фильтра-владельца.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Цимажепалетте. Препарепалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665233"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="c5edc-103">Цимажепалетте. Препарепалетте, метод</span><span class="sxs-lookup"><span data-stu-id="c5edc-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="c5edc-104">`PreparePalette`Метод настраивает палитру на основе типа носителя из фильтра-владельца.</span><span class="sxs-lookup"><span data-stu-id="c5edc-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5edc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5edc-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="c5edc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5edc-107">*пмтнев*</span><span class="sxs-lookup"><span data-stu-id="c5edc-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="c5edc-108">Указатель на новый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="c5edc-108">Pointer to the new media type.</span></span> <span data-ttu-id="c5edc-109">Блок формата должен быть структурой [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="c5edc-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c5edc-110">*пмтолд*</span><span class="sxs-lookup"><span data-stu-id="c5edc-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="c5edc-111">Указатель на старый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="c5edc-111">Pointer to the old media type.</span></span> <span data-ttu-id="c5edc-112">Если тип носителя задается в первый раз, этот параметр может быть пустым типом без блока Format.</span><span class="sxs-lookup"><span data-stu-id="c5edc-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="c5edc-113">В противном случае блок формата должен быть структурой **видеоинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="c5edc-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c5edc-114">*сздевице*</span><span class="sxs-lookup"><span data-stu-id="c5edc-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c5edc-115">Указатель на строку, содержащую имя устройства вывода, которое возвращается функцией GDI **енумдисплайдевицес** .</span><span class="sxs-lookup"><span data-stu-id="c5edc-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="c5edc-116">Чтобы использовать основное устройство вывода, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c5edc-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5edc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5edc-117">Return value</span></span>

<span data-ttu-id="c5edc-118">Возвращает \_ ОК, если палитра была обновлена, или \_ значение false, если палитра не изменилась.</span><span class="sxs-lookup"><span data-stu-id="c5edc-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5edc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5edc-119">Remarks</span></span>

<span data-ttu-id="c5edc-120">Если необходимо обновить палитру, этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c5edc-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="c5edc-121">Вызывает [**Цимажепалетте:: макепалетте**](cimagepalette-makepalette.md) для создания новой логической палитры.</span><span class="sxs-lookup"><span data-stu-id="c5edc-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="c5edc-122">Отправляет событие [**\_ \_ изменения палитры EC**](ec-palette-changed.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="c5edc-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="c5edc-123">Вызывает [**кбасевиндов:: сетпалетте**](cbasewindow-setpalette.md) для объекта **кбасевиндов** .</span><span class="sxs-lookup"><span data-stu-id="c5edc-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="c5edc-124">Вызывает [**кдравимаже:: инкрементпалеттеверсион**](cdrawimage-incrementpaletteversion.md) для объекта **кдравимаже** .</span><span class="sxs-lookup"><span data-stu-id="c5edc-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5edc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c5edc-125">Requirements</span></span>



| <span data-ttu-id="c5edc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c5edc-126">Requirement</span></span> | <span data-ttu-id="c5edc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c5edc-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5edc-128">Header</span><span class="sxs-lookup"><span data-stu-id="c5edc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c5edc-129"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5edc-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5edc-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5edc-130">Library</span></span><br/> | <dl> <span data-ttu-id="c5edc-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c5edc-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5edc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5edc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5edc-133">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="c5edc-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




