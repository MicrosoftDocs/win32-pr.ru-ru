---
description: Метод Get « \_ Автопросмотр» извлекает текущий флаг состояния автоотображения.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Метод CBaseControlWindow.get_AutoShow (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665282"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="67fd3-103">Кбасеконтролвиндов. Get, \_ метод автоотображения</span><span class="sxs-lookup"><span data-stu-id="67fd3-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="67fd3-104">`get_AutoShow`Метод получает текущий флаг состояния автоотображения.</span><span class="sxs-lookup"><span data-stu-id="67fd3-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67fd3-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="67fd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67fd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67fd3-107">*Автоотображение*</span><span class="sxs-lookup"><span data-stu-id="67fd3-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="67fd3-108">Указатель на логический флаг автоматизации (0 — Off, 1 — включено).</span><span class="sxs-lookup"><span data-stu-id="67fd3-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67fd3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67fd3-109">Return value</span></span>

<span data-ttu-id="67fd3-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67fd3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67fd3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67fd3-111">Remarks</span></span>

<span data-ttu-id="67fd3-112">Эта функция члена реализует метод [**ивидеовиндов:: Get для \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="67fd3-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="67fd3-113">Это свойство упрощает доступ к окнам для приложений.</span><span class="sxs-lookup"><span data-stu-id="67fd3-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="67fd3-114">Если задано значение 1 (включено), то окно, которое обычно скрыто после подключения фильтра, будет отображаться автоматически при приостановке или запуске фильтра.</span><span class="sxs-lookup"><span data-stu-id="67fd3-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="67fd3-115">Однако окно не должно быть скрыто при остановке фильтра.</span><span class="sxs-lookup"><span data-stu-id="67fd3-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="67fd3-116">Если этот параметр имеет значение 0 (OFF), окно становится видимым только тогда, когда приложение вызывает [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="67fd3-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="67fd3-117">Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром.</span><span class="sxs-lookup"><span data-stu-id="67fd3-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="67fd3-118">Вызовите функцию члена [**кбасеконтролвиндов:: исаутошовенаблед**](cbasecontrolwindow-isautoshowenabled.md) , чтобы получить это свойство, если не выполняется вызов из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="67fd3-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="67fd3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="67fd3-119">Requirements</span></span>



| <span data-ttu-id="67fd3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="67fd3-120">Requirement</span></span> | <span data-ttu-id="67fd3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="67fd3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fd3-122">Header</span><span class="sxs-lookup"><span data-stu-id="67fd3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="67fd3-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67fd3-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67fd3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="67fd3-124">Library</span></span><br/> | <dl> <span data-ttu-id="67fd3-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="67fd3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67fd3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67fd3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fd3-127">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="67fd3-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




