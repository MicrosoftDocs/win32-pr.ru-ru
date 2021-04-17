---
description: Метод размещения \_ WindowStyle задает стандартные стили окна.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Метод CBaseControlWindow.put_WindowStyle (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658062"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="7eb38-103">Кбасеконтролвиндов. размещение \_ метода WindowStyle</span><span class="sxs-lookup"><span data-stu-id="7eb38-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="7eb38-104">`put_WindowStyle`Метод задает стандартные стили окна.</span><span class="sxs-lookup"><span data-stu-id="7eb38-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eb38-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="7eb38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7eb38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb38-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="7eb38-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="7eb38-108">Новые стили окна.</span><span class="sxs-lookup"><span data-stu-id="7eb38-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb38-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7eb38-109">Return value</span></span>

<span data-ttu-id="7eb38-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7eb38-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7eb38-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7eb38-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eb38-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7eb38-112">Remarks</span></span>

<span data-ttu-id="7eb38-113">Следите за изменениями стилей окна.</span><span class="sxs-lookup"><span data-stu-id="7eb38-113">Take care when changing the window styles.</span></span> <span data-ttu-id="7eb38-114">В большинстве случаев приложение должно получить текущий стиль, а затем добавить или удалить недопустимые биты.</span><span class="sxs-lookup"><span data-stu-id="7eb38-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="7eb38-115">Эта процедура позволяет не менять различные внутренние стили окна, используемые Windows.</span><span class="sxs-lookup"><span data-stu-id="7eb38-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb38-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7eb38-116">Requirements</span></span>



| <span data-ttu-id="7eb38-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7eb38-117">Requirement</span></span> | <span data-ttu-id="7eb38-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7eb38-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb38-119">Header</span><span class="sxs-lookup"><span data-stu-id="7eb38-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7eb38-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb38-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7eb38-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7eb38-121">Library</span></span><br/> | <dl> <span data-ttu-id="7eb38-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb38-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb38-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7eb38-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb38-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="7eb38-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




