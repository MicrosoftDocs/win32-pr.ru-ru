---
description: Метод Get \_ WindowState извлекает текущее состояние окна.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Метод CBaseControlWindow.get_WindowState (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669235"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="bf315-103">Кбасеконтролвиндов. Get \_ WindowState, метод</span><span class="sxs-lookup"><span data-stu-id="bf315-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="bf315-104">`get_WindowState`Метод получает текущее состояние окна.</span><span class="sxs-lookup"><span data-stu-id="bf315-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf315-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf315-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="bf315-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf315-107">*пвиндовстате*</span><span class="sxs-lookup"><span data-stu-id="bf315-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="bf315-108">Указатель на состояние окна.</span><span class="sxs-lookup"><span data-stu-id="bf315-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf315-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf315-109">Return value</span></span>

<span data-ttu-id="bf315-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf315-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf315-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf315-111">Remarks</span></span>

<span data-ttu-id="bf315-112">Эта функция-член возвращает подмножество параметров функции Microsoft Win32 **ShowWindow** .</span><span class="sxs-lookup"><span data-stu-id="bf315-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="bf315-113">В частности, он возвращает SW \_ / \_ Hide, в зависимости от текущей видимости окна.</span><span class="sxs-lookup"><span data-stu-id="bf315-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="bf315-114">В \_ \_ зависимости от того, является ли окно значком или развернутым, он также возвращает значение по раскрытому программному и уменьшенному.</span><span class="sxs-lookup"><span data-stu-id="bf315-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf315-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bf315-115">Requirements</span></span>



| <span data-ttu-id="bf315-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bf315-116">Requirement</span></span> | <span data-ttu-id="bf315-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bf315-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf315-118">Header</span><span class="sxs-lookup"><span data-stu-id="bf315-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bf315-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf315-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf315-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf315-120">Library</span></span><br/> | <dl> <span data-ttu-id="bf315-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf315-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf315-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf315-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf315-123">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="bf315-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




