---
description: Метод Сетпалетте устанавливает палитру для окна.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Кбасевиндов. Сетпалетте, метод (Винутил. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657035"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="55d73-103">Кбасевиндов. Сетпалетте, метод (Винутил. h)</span><span class="sxs-lookup"><span data-stu-id="55d73-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="55d73-104">`SetPalette`Метод устанавливает палитру для окна.</span><span class="sxs-lookup"><span data-stu-id="55d73-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55d73-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="55d73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d73-107">*хпалетте*</span><span class="sxs-lookup"><span data-stu-id="55d73-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="55d73-108">Обработчик для новой палитры.</span><span class="sxs-lookup"><span data-stu-id="55d73-108">Handle to the new palette.</span></span> <span data-ttu-id="55d73-109">Не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="55d73-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d73-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55d73-110">Return value</span></span>

<span data-ttu-id="55d73-111">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55d73-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="55d73-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="55d73-112">Return code</span></span>                                                                             | <span data-ttu-id="55d73-113">Описание</span><span class="sxs-lookup"><span data-stu-id="55d73-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="55d73-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="55d73-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="55d73-115">Внутренний вызов **гдифлуш** вернул ошибку.</span><span class="sxs-lookup"><span data-stu-id="55d73-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="55d73-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="55d73-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="55d73-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="55d73-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="55d73-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55d73-118">Remarks</span></span>

<span data-ttu-id="55d73-119">Если значение переменной-члена [**кбасевиндов:: m \_ Бнореализе**](cbasewindow-m-bnorealize.md) равно **false** (значение по умолчанию), этот метод выбирает палитру и реализует ее.</span><span class="sxs-lookup"><span data-stu-id="55d73-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="55d73-120">В противном случае она выбирает палитру, но не реализует ее.</span><span class="sxs-lookup"><span data-stu-id="55d73-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="55d73-121">Объект не удаляет предыдущую палитру, которая использовалась.</span><span class="sxs-lookup"><span data-stu-id="55d73-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="55d73-122">Вызывающий объект отвечает за удаление палитр.</span><span class="sxs-lookup"><span data-stu-id="55d73-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="55d73-123">Любой поток может безопасно вызвать этот метод, а не только поток, которому принадлежит окно.</span><span class="sxs-lookup"><span data-stu-id="55d73-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="55d73-124">Окно отправляет частное сообщение самому себе, которое активирует вызов метода [**кбасевиндов:: онпалеттечанже**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="55d73-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d73-125">Требования</span><span class="sxs-lookup"><span data-stu-id="55d73-125">Requirements</span></span>



| <span data-ttu-id="55d73-126">Требование</span><span class="sxs-lookup"><span data-stu-id="55d73-126">Requirement</span></span> | <span data-ttu-id="55d73-127">Значение</span><span class="sxs-lookup"><span data-stu-id="55d73-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d73-128">Header</span><span class="sxs-lookup"><span data-stu-id="55d73-128">Header</span></span><br/>  | <dl> <span data-ttu-id="55d73-129"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55d73-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55d73-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55d73-130">Library</span></span><br/> | <dl> <span data-ttu-id="55d73-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="55d73-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d73-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55d73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d73-133">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="55d73-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




