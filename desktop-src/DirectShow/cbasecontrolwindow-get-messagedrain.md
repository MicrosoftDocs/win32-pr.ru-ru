---
description: Метод Get \_ мессажедраин извлекает текущую стоку сообщений.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Метод CBaseControlWindow.get_MessageDrain (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657068"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="8ba1c-103">Кбасеконтролвиндов. Get \_ мессажедраин, метод</span><span class="sxs-lookup"><span data-stu-id="8ba1c-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="8ba1c-104">`get_MessageDrain`Метод получает текущую стоку сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ba1c-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ba1c-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="8ba1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ba1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba1c-107">*Остановка*</span><span class="sxs-lookup"><span data-stu-id="8ba1c-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba1c-108">Указатель на текущее окно, принимающее сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="8ba1c-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba1c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ba1c-109">Return value</span></span>

<span data-ttu-id="8ba1c-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ba1c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba1c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ba1c-111">Remarks</span></span>

<span data-ttu-id="8ba1c-112">Сообщения, отправляемые в фильтр модуля подготовки отчетов, можно отправить в другое окно.</span><span class="sxs-lookup"><span data-stu-id="8ba1c-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="8ba1c-113">Окно, зарегистрированное для получения этих сообщений (с помощью функции-члена **кбасеконтролвиндов:: Get \_ мессажедраин** ), является текущим стоком сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ba1c-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba1c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8ba1c-114">Requirements</span></span>



| <span data-ttu-id="8ba1c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8ba1c-115">Requirement</span></span> | <span data-ttu-id="8ba1c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8ba1c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba1c-117">Header</span><span class="sxs-lookup"><span data-stu-id="8ba1c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba1c-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ba1c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ba1c-119">Library</span></span><br/> | <dl> <span data-ttu-id="8ba1c-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba1c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ba1c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba1c-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="8ba1c-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




