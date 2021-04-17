---
description: Метод «вставить \_ Автоотображение» задает флаг состояния «Автоотображение».
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Метод CBaseControlWindow.put_AutoShow (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657189"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="07272-103">Кбасеконтролвиндов. размещение \_ метода автоотображения</span><span class="sxs-lookup"><span data-stu-id="07272-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="07272-104">`put_AutoShow`Метод задает флаг состояния автоотображения.</span><span class="sxs-lookup"><span data-stu-id="07272-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="07272-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07272-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="07272-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07272-107">*Автоотображение*</span><span class="sxs-lookup"><span data-stu-id="07272-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="07272-108">Логический флаг автоматизации (0 — отключено, 1 — включено).</span><span class="sxs-lookup"><span data-stu-id="07272-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07272-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07272-109">Return value</span></span>

<span data-ttu-id="07272-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07272-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07272-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07272-111">Remarks</span></span>

<span data-ttu-id="07272-112">Это свойство упрощает доступ к окнам для приложений.</span><span class="sxs-lookup"><span data-stu-id="07272-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="07272-113">Если задано значение 1 (включено), то окно, которое обычно скрыто после подключения фильтра, будет отображаться автоматически при приостановке или запуске фильтра.</span><span class="sxs-lookup"><span data-stu-id="07272-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="07272-114">Однако окно не должно быть скрыто при остановке фильтра.</span><span class="sxs-lookup"><span data-stu-id="07272-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="07272-115">Если задано значение 0 (выключено), окно становится видимым только тогда, когда приложение вызывает [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="07272-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="07272-116">Требования</span><span class="sxs-lookup"><span data-stu-id="07272-116">Requirements</span></span>



| <span data-ttu-id="07272-117">Требование</span><span class="sxs-lookup"><span data-stu-id="07272-117">Requirement</span></span> | <span data-ttu-id="07272-118">Значение</span><span class="sxs-lookup"><span data-stu-id="07272-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07272-119">Header</span><span class="sxs-lookup"><span data-stu-id="07272-119">Header</span></span><br/>  | <dl> <span data-ttu-id="07272-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07272-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07272-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07272-121">Library</span></span><br/> | <dl> <span data-ttu-id="07272-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="07272-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07272-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07272-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07272-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="07272-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




