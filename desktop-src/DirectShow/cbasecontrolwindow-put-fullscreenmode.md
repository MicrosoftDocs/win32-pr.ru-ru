---
description: Метод размещения \_ фуллскринмоде задает полноэкранный режим модуля подготовки отчетов.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Метод CBaseControlWindow.put_FullScreenMode (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657348"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="037ff-103">Кбасеконтролвиндов. размещение \_ метода фуллскринмоде</span><span class="sxs-lookup"><span data-stu-id="037ff-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="037ff-104">`put_FullScreenMode`Метод задает полноэкранный режим для модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="037ff-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="037ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="037ff-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="037ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="037ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="037ff-107">*фуллскринмоде*</span><span class="sxs-lookup"><span data-stu-id="037ff-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="037ff-108">Полноэкранный режим для применения.</span><span class="sxs-lookup"><span data-stu-id="037ff-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="037ff-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="037ff-109">Return value</span></span>

<span data-ttu-id="037ff-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="037ff-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="037ff-111">Текущая реализация возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="037ff-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="037ff-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="037ff-112">Remarks</span></span>

<span data-ttu-id="037ff-113">Модуль подготовки видео, реализующий полноэкранный режим, должен переопределять эту функцию-член и реализовывать все поддерживаемые им режимы.</span><span class="sxs-lookup"><span data-stu-id="037ff-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="037ff-114">Требования</span><span class="sxs-lookup"><span data-stu-id="037ff-114">Requirements</span></span>



| <span data-ttu-id="037ff-115">Требование</span><span class="sxs-lookup"><span data-stu-id="037ff-115">Requirement</span></span> | <span data-ttu-id="037ff-116">Значение</span><span class="sxs-lookup"><span data-stu-id="037ff-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="037ff-117">Header</span><span class="sxs-lookup"><span data-stu-id="037ff-117">Header</span></span><br/>  | <dl> <span data-ttu-id="037ff-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="037ff-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="037ff-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="037ff-119">Library</span></span><br/> | <dl> <span data-ttu-id="037ff-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="037ff-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="037ff-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="037ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037ff-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="037ff-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




