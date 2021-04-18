---
description: Метод получения \_ владельца получает текущего владельца окна.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Метод CBaseControlWindow.get_Owner (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668558"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="ecb82-103">Кбасеконтролвиндов. Get, \_ метод Owner</span><span class="sxs-lookup"><span data-stu-id="ecb82-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="ecb82-104">`get_Owner`Метод получает текущего владельца окна.</span><span class="sxs-lookup"><span data-stu-id="ecb82-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecb82-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="ecb82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecb82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb82-107">*Владелец*</span><span class="sxs-lookup"><span data-stu-id="ecb82-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb82-108">Указатель на владельца окна.</span><span class="sxs-lookup"><span data-stu-id="ecb82-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb82-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecb82-109">Return value</span></span>

<span data-ttu-id="ecb82-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ecb82-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb82-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecb82-111">Remarks</span></span>

<span data-ttu-id="ecb82-112">Окно видео может воспроизводиться в среде документа.</span><span class="sxs-lookup"><span data-stu-id="ecb82-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="ecb82-113">Для этого окно должно быть дочерним для другого окна (так что оно обрезается и перемещается соответствующим образом).</span><span class="sxs-lookup"><span data-stu-id="ecb82-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="ecb82-114">Это свойство позволяет устанавливать и извлекать владелец окна.</span><span class="sxs-lookup"><span data-stu-id="ecb82-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="ecb82-115">Если окно принадлежит другому окну, оно просто вызывает функцию Microsoft Win32 **сетпарент** .</span><span class="sxs-lookup"><span data-stu-id="ecb82-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="ecb82-116">Приложение, вызывающее эту функцию, изменит стили окна, чтобы установить \_ дочерний бит WS для.</span><span class="sxs-lookup"><span data-stu-id="ecb82-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="ecb82-117">Когда окно владеет другим окном, оно автоматически пересылает определенные наборы сообщений (в частности, в сообщениях мыши и клавиатуры).</span><span class="sxs-lookup"><span data-stu-id="ecb82-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="ecb82-118">Это позволяет приложению выполнять простые изменения в режиме горячей замены и другие взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="ecb82-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="ecb82-119">Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром.</span><span class="sxs-lookup"><span data-stu-id="ecb82-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="ecb82-120">Вызовите функцию члена [**кбасеконтролвиндов:: жетовнервиндов**](cbasecontrolwindow-getownerwindow.md) , чтобы получить это свойство, если не вызывается из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="ecb82-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb82-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb82-121">Requirements</span></span>



| <span data-ttu-id="ecb82-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb82-122">Requirement</span></span> | <span data-ttu-id="ecb82-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb82-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb82-124">Header</span><span class="sxs-lookup"><span data-stu-id="ecb82-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ecb82-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb82-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ecb82-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecb82-126">Library</span></span><br/> | <dl> <span data-ttu-id="ecb82-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb82-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb82-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecb82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb82-129">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="ecb82-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




