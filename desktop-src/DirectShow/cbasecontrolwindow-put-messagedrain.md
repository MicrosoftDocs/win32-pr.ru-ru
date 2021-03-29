---
description: Метод размещения \_ мессажедраин задает для окна получение сообщений окон, отправленных обработчику видео.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Метод CBaseControlWindow.put_MessageDrain (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657868"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="c2cc1-103">Кбасеконтролвиндов. размещение \_ метода мессажедраин</span><span class="sxs-lookup"><span data-stu-id="c2cc1-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="c2cc1-104">`put_MessageDrain`Метод задает для окна получение сообщений окна, отправленных обработчику видео.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2cc1-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="c2cc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2cc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cc1-107">*Остановка*</span><span class="sxs-lookup"><span data-stu-id="c2cc1-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cc1-108">Окно для публикации сообщений.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cc1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2cc1-109">Return value</span></span>

<span data-ttu-id="c2cc1-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2cc1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cc1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2cc1-111">Remarks</span></span>

<span data-ttu-id="c2cc1-112">Сообщения, отправляемые в фильтр модуля подготовки отчетов, можно отправить в другое окно.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="c2cc1-113">Эта функция члена регистрирует окно для получения этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="c2cc1-114">В отличие от функции-члена [**\_ owner кбасеконтролвиндов::p UT**](cbasecontrolwindow-put-owner.md) , эта функция-член не делает окно видео дочерним для другого окна.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="c2cc1-115">Он особенно полезен для модулей подготовки видео в полноэкранном режиме, которые не могут быть дочерними окнами.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cc1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c2cc1-116">Requirements</span></span>



| <span data-ttu-id="c2cc1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c2cc1-117">Requirement</span></span> | <span data-ttu-id="c2cc1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c2cc1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cc1-119">Header</span><span class="sxs-lookup"><span data-stu-id="c2cc1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c2cc1-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2cc1-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2cc1-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2cc1-121">Library</span></span><br/> | <dl> <span data-ttu-id="c2cc1-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c2cc1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cc1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2cc1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cc1-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="c2cc1-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




