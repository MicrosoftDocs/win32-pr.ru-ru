---
description: Метод «разместить \_ видимый» позволяет отобразить или скрыть окно.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Метод CBaseControlWindow.put_Visible (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658066"
---
# <a name="cbasecontrolwindowput_visible-method"></a><span data-ttu-id="dc32f-103">Кбасеконтролвиндов. размещение \_ видимого метода</span><span class="sxs-lookup"><span data-stu-id="dc32f-103">CBaseControlWindow.put\_Visible method</span></span>

<span data-ttu-id="dc32f-104">`put_Visible`Метод делает отображение или скрытие окна.</span><span class="sxs-lookup"><span data-stu-id="dc32f-104">The `put_Visible` method makes shows or hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc32f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc32f-105">Syntax</span></span>


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a><span data-ttu-id="dc32f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc32f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc32f-107">*Visible*</span><span class="sxs-lookup"><span data-stu-id="dc32f-107">*Visible*</span></span> 
</dt> <dd>

<span data-ttu-id="dc32f-108">Логический флаг автоматизации (0 означает, что окно скрыто, 1 означает, что окно отображается).</span><span class="sxs-lookup"><span data-stu-id="dc32f-108">Automation Boolean flag (0 means window is hidden,  1 means window is shown).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc32f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc32f-109">Return value</span></span>

<span data-ttu-id="dc32f-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc32f-110">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc32f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dc32f-111">Requirements</span></span>



| <span data-ttu-id="dc32f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dc32f-112">Requirement</span></span> | <span data-ttu-id="dc32f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dc32f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc32f-114">Header</span><span class="sxs-lookup"><span data-stu-id="dc32f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="dc32f-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc32f-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc32f-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc32f-116">Library</span></span><br/> | <dl> <span data-ttu-id="dc32f-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dc32f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc32f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc32f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc32f-119">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="dc32f-119">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




