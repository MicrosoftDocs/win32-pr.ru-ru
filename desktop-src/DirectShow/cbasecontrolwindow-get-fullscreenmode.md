---
description: Метод Get \_ фуллскринмоде извлекает текущий полноэкранный режим.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Метод CBaseControlWindow.get_FullScreenMode (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668838"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="3b075-103">Кбасеконтролвиндов. Get \_ фуллскринмоде, метод</span><span class="sxs-lookup"><span data-stu-id="3b075-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="3b075-104">`get_FullScreenMode`Метод извлекает текущий полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="3b075-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b075-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b075-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="3b075-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b075-107">*фуллскринмоде*</span><span class="sxs-lookup"><span data-stu-id="3b075-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3b075-108">Указатель на текущий полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="3b075-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b075-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b075-109">Return value</span></span>

<span data-ttu-id="3b075-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b075-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b075-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b075-111">Remarks</span></span>

<span data-ttu-id="3b075-112">Эта функция – член \_ по умолчанию возвращает E нотимпл.</span><span class="sxs-lookup"><span data-stu-id="3b075-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="3b075-113">Это информирует распространитель подключаемого модуля [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) о том, что этот модуль подготовки отчетов не реализует полноэкранный визуализатор.</span><span class="sxs-lookup"><span data-stu-id="3b075-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b075-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3b075-114">Requirements</span></span>



| <span data-ttu-id="3b075-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3b075-115">Requirement</span></span> | <span data-ttu-id="3b075-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3b075-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b075-117">Header</span><span class="sxs-lookup"><span data-stu-id="3b075-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3b075-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b075-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b075-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b075-119">Library</span></span><br/> | <dl> <span data-ttu-id="3b075-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3b075-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b075-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b075-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b075-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="3b075-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




