---
description: Метод Поссиблеатмессаже позволяет производному классу пересылать сообщения в другое окно.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Кбасевиндов. Поссиблеатмессаже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657036"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="60e0e-103">Кбасевиндов. Поссиблеатмессаже, метод</span><span class="sxs-lookup"><span data-stu-id="60e0e-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="60e0e-104">`PossiblyEatMessage`Метод позволяет производному классу пересылать сообщения в другое окно.</span><span class="sxs-lookup"><span data-stu-id="60e0e-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60e0e-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="60e0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60e0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e0e-107">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="60e0e-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="60e0e-108">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e0e-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="60e0e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60e0e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60e0e-110">Первый параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e0e-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="60e0e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60e0e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60e0e-112">Второй параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e0e-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e0e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60e0e-113">Return value</span></span>

<span data-ttu-id="60e0e-114">Возвращает **значение true** , если сообщение было переслано, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="60e0e-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="60e0e-115">Базовый класс возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60e0e-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60e0e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60e0e-116">Remarks</span></span>

<span data-ttu-id="60e0e-117">Перед тем как метод [**кбасевиндов:: онрецеивемессаже**](cbasewindow-onreceivemessage.md) обрабатывает сообщение, он вызывает `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="60e0e-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="60e0e-118">Если `PossiblyEatMessage` возвращает **значение true**, **онрецеивемессаже** игнорирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="60e0e-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="60e0e-119">Производный класс может переопределить `PossiblyEatMessage` , чтобы он перенаправлял некоторые сообщения в окно владельца.</span><span class="sxs-lookup"><span data-stu-id="60e0e-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="60e0e-120">Например, класс [**кбасеконтролвиндов**](cbasecontrolwindow.md) , который является производным от **кбасевиндов**, перенаправляет сообщения клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="60e0e-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e0e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="60e0e-121">Requirements</span></span>



| <span data-ttu-id="60e0e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="60e0e-122">Requirement</span></span> | <span data-ttu-id="60e0e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="60e0e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e0e-124">Header</span><span class="sxs-lookup"><span data-stu-id="60e0e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60e0e-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60e0e-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60e0e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60e0e-126">Library</span></span><br/> | <dl> <span data-ttu-id="60e0e-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="60e0e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e0e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60e0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e0e-129">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="60e0e-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




