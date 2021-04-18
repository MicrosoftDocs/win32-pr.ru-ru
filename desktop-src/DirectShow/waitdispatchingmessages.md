---
description: Функция Ваитдиспатчингмессажес ожидает сигнала объекта, во время диспетчеризации сообщений окна.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Функция Ваитдиспатчингмессажес (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685365"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="05cb9-103">Функция Ваитдиспатчингмессажес</span><span class="sxs-lookup"><span data-stu-id="05cb9-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="05cb9-104">`WaitDispatchingMessages`Функция ожидает сигнала объекта, во время диспетчеризации сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="05cb9-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="05cb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05cb9-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="05cb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05cb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05cb9-107">*хобжект*</span><span class="sxs-lookup"><span data-stu-id="05cb9-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="05cb9-108">Обрабатываемый объект для ожидания.</span><span class="sxs-lookup"><span data-stu-id="05cb9-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="05cb9-109">*двваит*</span><span class="sxs-lookup"><span data-stu-id="05cb9-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="05cb9-110">Интервал времени ожидания (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="05cb9-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="05cb9-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="05cb9-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="05cb9-112">Необязательный обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="05cb9-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="05cb9-113">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="05cb9-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="05cb9-114">Необязательное окно сообщения с указанием отправляемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="05cb9-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="05cb9-115">*хевент*</span><span class="sxs-lookup"><span data-stu-id="05cb9-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="05cb9-116">Необязательный обработчик события для ожидания.</span><span class="sxs-lookup"><span data-stu-id="05cb9-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05cb9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05cb9-117">Return value</span></span>

<span data-ttu-id="05cb9-118">Возвращает значение из функции **WaitForMultipleObjects** .</span><span class="sxs-lookup"><span data-stu-id="05cb9-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="05cb9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05cb9-119">Remarks</span></span>

<span data-ttu-id="05cb9-120">Если объект владеет окном, он должен отправлять сообщения окна в ожидании.</span><span class="sxs-lookup"><span data-stu-id="05cb9-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="05cb9-121">Эта функция позволяет объекту ожидать события, семафора или другого взаимоисключающего объекта во время диспетчеризации сообщений.</span><span class="sxs-lookup"><span data-stu-id="05cb9-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="05cb9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="05cb9-122">Requirements</span></span>



| <span data-ttu-id="05cb9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="05cb9-123">Requirement</span></span> | <span data-ttu-id="05cb9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="05cb9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05cb9-125">Header</span><span class="sxs-lookup"><span data-stu-id="05cb9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="05cb9-126"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05cb9-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="05cb9-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05cb9-127">Library</span></span><br/> | <dl> <span data-ttu-id="05cb9-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="05cb9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05cb9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05cb9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05cb9-130">Различные вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="05cb9-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




