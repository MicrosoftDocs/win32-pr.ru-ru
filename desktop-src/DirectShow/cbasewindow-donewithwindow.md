---
description: Метод Доневисвиндов уничтожает окно.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Кбасевиндов. Доневисвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656952"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="a2a5c-103">Кбасевиндов. Доневисвиндов, метод</span><span class="sxs-lookup"><span data-stu-id="a2a5c-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="a2a5c-104">`DoneWithWindow`Метод уничтожает окно.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2a5c-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="a2a5c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2a5c-106">Parameters</span></span>

<span data-ttu-id="a2a5c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2a5c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2a5c-108">Return value</span></span>

<span data-ttu-id="a2a5c-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a5c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2a5c-110">Remarks</span></span>

<span data-ttu-id="a2a5c-111">Вызовите этот метод из метода деструктора производного объекта.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="a2a5c-112">Если этот метод вызывается из того же потока, который создал окно, метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a2a5c-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="a2a5c-113">Вызывает метод [**кбасевиндов:: инактиватевиндов**](cbasewindow-inactivatewindow.md) , который деактивирует окно.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="a2a5c-114">Вызывает метод [**кбасевиндов:: унинитиалисевиндов**](cbasewindow-uninitialisewindow.md) , который освобождает ресурсы, используемые окном.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="a2a5c-115">Уничтожает окно.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-115">Destroys the window.</span></span>

<span data-ttu-id="a2a5c-116">Если поток вызывает `DoneWithWindow` не поток, создавший окно, метод отправляет в окно частное сообщение "Destroy".</span><span class="sxs-lookup"><span data-stu-id="a2a5c-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="a2a5c-117">Когда окно получает это сообщение, оно вызывает `DoneWithWindow` сам себя.</span><span class="sxs-lookup"><span data-stu-id="a2a5c-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="a2a5c-118">(Если [**кбасевиндов:: m \_ Бдопосттодестрой**](cbasewindow-m-bdoposttodestroy.md) имеет **значение true**, окно отправляет сообщение.)</span><span class="sxs-lookup"><span data-stu-id="a2a5c-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a5c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a2a5c-119">Requirements</span></span>



| <span data-ttu-id="a2a5c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a2a5c-120">Requirement</span></span> | <span data-ttu-id="a2a5c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a2a5c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a5c-122">Header</span><span class="sxs-lookup"><span data-stu-id="a2a5c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a2a5c-123"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2a5c-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2a5c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2a5c-124">Library</span></span><br/> | <dl> <span data-ttu-id="a2a5c-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a2a5c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2a5c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2a5c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a5c-127">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="a2a5c-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




