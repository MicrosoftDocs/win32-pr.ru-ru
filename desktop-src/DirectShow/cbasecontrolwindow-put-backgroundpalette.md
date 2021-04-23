---
description: Метод размещения \_ баккграундпалетте устанавливает флаг для реализации палитры в фоновом режиме.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Метод CBaseControlWindow.put_BackgroundPalette (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657351"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="07773-103">Кбасеконтролвиндов. размещение \_ метода баккграундпалетте</span><span class="sxs-lookup"><span data-stu-id="07773-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="07773-104">`put_BackgroundPalette`Метод задает флаг для реализации палитры в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="07773-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="07773-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07773-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="07773-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07773-107">*баккграундпалетте*</span><span class="sxs-lookup"><span data-stu-id="07773-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="07773-108">Логический флаг автоматизации (0 — отключено, 1 — включено).</span><span class="sxs-lookup"><span data-stu-id="07773-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07773-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07773-109">Return value</span></span>

<span data-ttu-id="07773-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07773-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07773-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07773-111">Remarks</span></span>

<span data-ttu-id="07773-112">Для воспроизведения видео в другом приложении или документе может потребоваться использовать собственную палитру.</span><span class="sxs-lookup"><span data-stu-id="07773-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="07773-113">Он может задать, чтобы видео использовало текущую палитру переднего плана, а не собственную в качестве палитры фона, установив для этого флага значение 1.</span><span class="sxs-lookup"><span data-stu-id="07773-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="07773-114">Если задано значение 0, окно будет установлено и использовать собственную предпочтительную палитру.</span><span class="sxs-lookup"><span data-stu-id="07773-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="07773-115">Запрос использования другой палитры в окне приведет к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="07773-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="07773-116">Требования</span><span class="sxs-lookup"><span data-stu-id="07773-116">Requirements</span></span>



| <span data-ttu-id="07773-117">Требование</span><span class="sxs-lookup"><span data-stu-id="07773-117">Requirement</span></span> | <span data-ttu-id="07773-118">Значение</span><span class="sxs-lookup"><span data-stu-id="07773-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07773-119">Header</span><span class="sxs-lookup"><span data-stu-id="07773-119">Header</span></span><br/>  | <dl> <span data-ttu-id="07773-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07773-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07773-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07773-121">Library</span></span><br/> | <dl> <span data-ttu-id="07773-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="07773-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07773-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07773-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07773-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="07773-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




