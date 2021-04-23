---
description: Метод Нотифйовнермессаже передает в окно видео определенные сообщения.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Кбасеконтролвиндов. Нотифйовнермессаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658108"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="4f09b-103">Кбасеконтролвиндов. Нотифйовнермессаже, метод</span><span class="sxs-lookup"><span data-stu-id="4f09b-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="4f09b-104">`NotifyOwnerMessage`Метод передает в окно видео определенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f09b-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f09b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f09b-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="4f09b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f09b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f09b-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4f09b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4f09b-108">Обработчик для окна видео.</span><span class="sxs-lookup"><span data-stu-id="4f09b-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="4f09b-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="4f09b-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="4f09b-110">Сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="4f09b-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="4f09b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f09b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f09b-112">Первый параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f09b-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4f09b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f09b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f09b-114">Второй параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f09b-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f09b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f09b-115">Return value</span></span>

<span data-ttu-id="4f09b-116">НЕ возвращает \_ ошибку.</span><span class="sxs-lookup"><span data-stu-id="4f09b-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f09b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f09b-117">Remarks</span></span>

<span data-ttu-id="4f09b-118">Когда окно видео является дочерним по отношению к другому окну, оно не получает определенные сообщения окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4f09b-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="4f09b-119">Эти сообщения могут быть ценными для модуля подготовки отчетов, так как они могут повлиять на его поведение.</span><span class="sxs-lookup"><span data-stu-id="4f09b-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="4f09b-120">`NotifyOwnerMessage` передает любое из следующих сообщений в окно видео.</span><span class="sxs-lookup"><span data-stu-id="4f09b-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="4f09b-121">WM \_ активатеапп</span><span class="sxs-lookup"><span data-stu-id="4f09b-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="4f09b-122">WM \_ девмодечанже</span><span class="sxs-lookup"><span data-stu-id="4f09b-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="4f09b-123">WM \_ дисплайчанже</span><span class="sxs-lookup"><span data-stu-id="4f09b-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="4f09b-124">WM \_ палеттечанжед</span><span class="sxs-lookup"><span data-stu-id="4f09b-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="4f09b-125">WM \_ палеттеисчангинг</span><span class="sxs-lookup"><span data-stu-id="4f09b-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="4f09b-126">WM \_ куериневпалетте</span><span class="sxs-lookup"><span data-stu-id="4f09b-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="4f09b-127">WM \_ сисколорчанже</span><span class="sxs-lookup"><span data-stu-id="4f09b-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="4f09b-128">Вы можете запросить, чтобы окно с подключаемым модулем [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) стало дочерним для другого окна.</span><span class="sxs-lookup"><span data-stu-id="4f09b-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="4f09b-129">В этом случае PID будет искать определенные сообщения, которые могут быть отправлены в окно-владелец.</span><span class="sxs-lookup"><span data-stu-id="4f09b-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="4f09b-130">Идентификатор процесса пересылает эти сообщения в собственное окно.</span><span class="sxs-lookup"><span data-stu-id="4f09b-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="4f09b-131">Обработка сообщений по умолчанию заключается в синхронной отправке их в собственную процедуру окна путем вызова функции Win32 **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="4f09b-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f09b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4f09b-132">Requirements</span></span>



| <span data-ttu-id="4f09b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4f09b-133">Requirement</span></span> | <span data-ttu-id="4f09b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4f09b-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f09b-135">Header</span><span class="sxs-lookup"><span data-stu-id="4f09b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4f09b-136"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f09b-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f09b-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f09b-137">Library</span></span><br/> | <dl> <span data-ttu-id="4f09b-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4f09b-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f09b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f09b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f09b-140">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="4f09b-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




