---
description: Метод Get \_ виндовстиликс извлекает расширенные стили окна.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Метод CBaseControlWindow.get_WindowStyleEx (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657924"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="80cf9-103">Кбасеконтролвиндов. Get \_ виндовстиликс, метод</span><span class="sxs-lookup"><span data-stu-id="80cf9-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="80cf9-104">`get_WindowStyleEx`Метод получает расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="80cf9-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="80cf9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80cf9-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="80cf9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80cf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80cf9-107">*пвиндовстиликс*</span><span class="sxs-lookup"><span data-stu-id="80cf9-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="80cf9-108">Указатель на расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="80cf9-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80cf9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80cf9-109">Return value</span></span>

<span data-ttu-id="80cf9-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80cf9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80cf9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80cf9-111">Remarks</span></span>

<span data-ttu-id="80cf9-112">Эта функция члена получает расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="80cf9-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="80cf9-113">Он вызывает функцию члена [**кбасеконтролвиндов::D ожетвиндовстиле**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="80cf9-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="80cf9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="80cf9-114">Requirements</span></span>



| <span data-ttu-id="80cf9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="80cf9-115">Requirement</span></span> | <span data-ttu-id="80cf9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="80cf9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf9-117">Header</span><span class="sxs-lookup"><span data-stu-id="80cf9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="80cf9-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80cf9-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80cf9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80cf9-119">Library</span></span><br/> | <dl> <span data-ttu-id="80cf9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="80cf9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80cf9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80cf9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80cf9-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="80cf9-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




