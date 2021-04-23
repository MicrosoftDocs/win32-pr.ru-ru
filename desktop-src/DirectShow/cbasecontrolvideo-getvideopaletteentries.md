---
description: Метод Жетвидеопалеттинтриес извлекает диапазон записей палитры для видео.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Кбасеконтролвидео. Жетвидеопалеттинтриес, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689266"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="c09fc-103">Кбасеконтролвидео. Жетвидеопалеттинтриес, метод</span><span class="sxs-lookup"><span data-stu-id="c09fc-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="c09fc-104">`GetVideoPaletteEntries`Метод извлекает диапазон записей палитры для видео.</span><span class="sxs-lookup"><span data-stu-id="c09fc-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09fc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c09fc-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c09fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c09fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c09fc-107">*StartIndex*</span><span class="sxs-lookup"><span data-stu-id="c09fc-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c09fc-108">Запись начальной палитры с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="c09fc-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="c09fc-109">*Записи*</span><span class="sxs-lookup"><span data-stu-id="c09fc-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="c09fc-110">Число необходимых записей.</span><span class="sxs-lookup"><span data-stu-id="c09fc-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="c09fc-111">*претриевед*</span><span class="sxs-lookup"><span data-stu-id="c09fc-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="c09fc-112">Указатель на число полученных цветов.</span><span class="sxs-lookup"><span data-stu-id="c09fc-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="c09fc-113">*ппалетте*</span><span class="sxs-lookup"><span data-stu-id="c09fc-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="c09fc-114">Указатель на выходной буфер для цветов.</span><span class="sxs-lookup"><span data-stu-id="c09fc-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c09fc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c09fc-115">Return value</span></span>

<span data-ttu-id="c09fc-116">Если \_ \_ \_ \_ в видеороликах не хватает цветовой палитры, в случае нехватки памяти, e INVALIDARG, если параметр startIndex является недопустимым, то при успешном возврате значения не отображаются, если \_ \_  \_ в палитре нет цветов, то в окне VFW e нет доступных палитр.</span><span class="sxs-lookup"><span data-stu-id="c09fc-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="c09fc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c09fc-117">Remarks</span></span>

<span data-ttu-id="c09fc-118">Эта функция – член возвращает текущую палитру видео в виде массива, выделенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="c09fc-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="c09fc-119">Чтобы сохранить целостность, используйте члены в структуре Win32 **палеттинтри** , чтобы получить цвета, а не элементы в структуре **ргбкуад** (хотя параметр является **длинным**).</span><span class="sxs-lookup"><span data-stu-id="c09fc-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="c09fc-120">Память выделяется вызывающим объектом, поэтому просто скопируйте каждую из них в свою очередь.</span><span class="sxs-lookup"><span data-stu-id="c09fc-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="c09fc-121">Определите, что количество запрошенных записей и смещение начальной позиции являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="c09fc-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="c09fc-122">Если число записей равно нулю, возвращается \_ код false.</span><span class="sxs-lookup"><span data-stu-id="c09fc-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09fc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c09fc-123">Requirements</span></span>



| <span data-ttu-id="c09fc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c09fc-124">Requirement</span></span> | <span data-ttu-id="c09fc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c09fc-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09fc-126">Header</span><span class="sxs-lookup"><span data-stu-id="c09fc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c09fc-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c09fc-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c09fc-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c09fc-128">Library</span></span><br/> | <dl> <span data-ttu-id="c09fc-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c09fc-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c09fc-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c09fc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09fc-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="c09fc-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




