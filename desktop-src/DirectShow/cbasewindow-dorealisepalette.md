---
description: Метод Дореалисепалетте реализует текущую палитру окна.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Кбасевиндов. Дореалисепалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656951"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="82102-103">Кбасевиндов. Дореалисепалетте, метод</span><span class="sxs-lookup"><span data-stu-id="82102-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="82102-104">`DoRealisePalette`Метод реализует текущую палитру окна.</span><span class="sxs-lookup"><span data-stu-id="82102-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="82102-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82102-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="82102-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82102-107">*бфорцебаккграунд*</span><span class="sxs-lookup"><span data-stu-id="82102-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="82102-108">Логическое значение, указывающее, должна ли палитра быть палитрой фона.</span><span class="sxs-lookup"><span data-stu-id="82102-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="82102-109">Дополнительные сведения см. в разделе **селектпалетте** в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="82102-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82102-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82102-110">Return value</span></span>

<span data-ttu-id="82102-111">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="82102-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="82102-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82102-112">Return code</span></span>                                                                             | <span data-ttu-id="82102-113">Описание</span><span class="sxs-lookup"><span data-stu-id="82102-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="82102-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="82102-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="82102-115">Внутренний вызов **гдифлуш** вернул ошибку.</span><span class="sxs-lookup"><span data-stu-id="82102-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="82102-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82102-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="82102-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="82102-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="82102-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82102-118">Remarks</span></span>

<span data-ttu-id="82102-119">Метод [**кбасевиндов:: онпалеттечанже**](cbasewindow-onpalettechange.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="82102-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="82102-120">Чтобы задать новую палитру, вызовите метод [**кбасевиндов:: сетпалетте**](cbasewindow-setpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="82102-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="82102-121">Требования</span><span class="sxs-lookup"><span data-stu-id="82102-121">Requirements</span></span>



| <span data-ttu-id="82102-122">Требование</span><span class="sxs-lookup"><span data-stu-id="82102-122">Requirement</span></span> | <span data-ttu-id="82102-123">Значение</span><span class="sxs-lookup"><span data-stu-id="82102-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82102-124">Header</span><span class="sxs-lookup"><span data-stu-id="82102-124">Header</span></span><br/>  | <dl> <span data-ttu-id="82102-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82102-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82102-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82102-126">Library</span></span><br/> | <dl> <span data-ttu-id="82102-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="82102-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82102-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82102-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82102-129">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="82102-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




