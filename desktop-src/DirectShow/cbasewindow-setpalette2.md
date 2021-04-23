---
description: Метод Сетпалетте устанавливает палитру для окна. Этот метод не имеет параметров.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Кбасевиндов. Сетпалетте, метод (Винутил. h) — без параметров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104273994"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="330c5-104">Кбасевиндов. Сетпалетте, метод (Винутил. h) — без параметров</span><span class="sxs-lookup"><span data-stu-id="330c5-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="330c5-105">`SetPalette`Метод устанавливает палитру для окна.</span><span class="sxs-lookup"><span data-stu-id="330c5-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="330c5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="330c5-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="330c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="330c5-107">Parameters</span></span>

<span data-ttu-id="330c5-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="330c5-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="330c5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="330c5-109">Return value</span></span>

<span data-ttu-id="330c5-110">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="330c5-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="330c5-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="330c5-111">Return code</span></span>                                                                             | <span data-ttu-id="330c5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="330c5-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="330c5-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="330c5-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="330c5-114">Внутренний вызов **гдифлуш** вернул ошибку.</span><span class="sxs-lookup"><span data-stu-id="330c5-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="330c5-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="330c5-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="330c5-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="330c5-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="330c5-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="330c5-117">Remarks</span></span>

<span data-ttu-id="330c5-118">Выбрана палитра, заданная переменной-членом [**кбасевиндов:: m \_ хпалетте**](cbasewindow-m-hpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="330c5-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="330c5-119">Вызывающий объект должен гарантировать допустимость **m \_ хпалетте**.</span><span class="sxs-lookup"><span data-stu-id="330c5-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="330c5-120">Если значение переменной-члена [**кбасевиндов:: m \_ Бнореализе**](cbasewindow-m-bnorealize.md) равно **false** (значение по умолчанию), этот метод выбирает палитру и реализует ее.</span><span class="sxs-lookup"><span data-stu-id="330c5-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="330c5-121">В противном случае она выбирает палитру, но не реализует ее.</span><span class="sxs-lookup"><span data-stu-id="330c5-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="330c5-122">Объект не удаляет предыдущую палитру, которая использовалась.</span><span class="sxs-lookup"><span data-stu-id="330c5-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="330c5-123">Вызывающий объект отвечает за удаление палитр.</span><span class="sxs-lookup"><span data-stu-id="330c5-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="330c5-124">Любой поток может безопасно вызвать этот метод, а не только поток, которому принадлежит окно.</span><span class="sxs-lookup"><span data-stu-id="330c5-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="330c5-125">Окно отправляет частное сообщение самому себе, которое активирует вызов метода [**кбасевиндов:: онпалеттечанже**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="330c5-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="330c5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="330c5-126">Requirements</span></span>

| <span data-ttu-id="330c5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="330c5-127">Requirement</span></span> | <span data-ttu-id="330c5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="330c5-128">Value</span></span> |
|-|-|
| <span data-ttu-id="330c5-129">Header</span><span class="sxs-lookup"><span data-stu-id="330c5-129">Header</span></span> | <span data-ttu-id="330c5-130">Винутил. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="330c5-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="330c5-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="330c5-131">Library</span></span>| <span data-ttu-id="330c5-132">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="330c5-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="330c5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="330c5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330c5-134">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="330c5-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




