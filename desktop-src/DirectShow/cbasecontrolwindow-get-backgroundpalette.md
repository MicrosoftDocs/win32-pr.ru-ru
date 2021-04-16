---
description: Метод Get \_ баккграундпалетте извлекает реализованную палитру в фоновом флаге.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Метод CBaseControlWindow.get_BackgroundPalette (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656981"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="82a03-103">Кбасеконтролвиндов. Get \_ баккграундпалетте, метод</span><span class="sxs-lookup"><span data-stu-id="82a03-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="82a03-104">`get_BackgroundPalette`Метод извлекает реализованную палитру в фоновом флаге.</span><span class="sxs-lookup"><span data-stu-id="82a03-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82a03-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="82a03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82a03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a03-107">*пбаккграундпалетте*</span><span class="sxs-lookup"><span data-stu-id="82a03-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="82a03-108">Указатель на логический флаг автоматизации (0 — Off, 1 — включено).</span><span class="sxs-lookup"><span data-stu-id="82a03-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a03-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82a03-109">Return value</span></span>

<span data-ttu-id="82a03-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82a03-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82a03-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82a03-111">Remarks</span></span>

<span data-ttu-id="82a03-112">Эта функция члена реализует метод [**ивидеовиндов:: Get \_ баккграундпалетте**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="82a03-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="82a03-113">Если видео будет воспроизводиться в другом приложении или документе, может потребоваться использовать собственную палитру приложения.</span><span class="sxs-lookup"><span data-stu-id="82a03-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="82a03-114">Он может задать, чтобы видео использовало текущую палитру переднего плана, а не собственную, установив для этого флага значение 1.</span><span class="sxs-lookup"><span data-stu-id="82a03-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="82a03-115">Если задано значение 0, окно будет установлено и использовать собственную предпочтительную палитру.</span><span class="sxs-lookup"><span data-stu-id="82a03-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="82a03-116">Обратите внимание, что запрос на использование другой палитры приведет к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="82a03-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a03-117">Требования</span><span class="sxs-lookup"><span data-stu-id="82a03-117">Requirements</span></span>



| <span data-ttu-id="82a03-118">Требование</span><span class="sxs-lookup"><span data-stu-id="82a03-118">Requirement</span></span> | <span data-ttu-id="82a03-119">Значение</span><span class="sxs-lookup"><span data-stu-id="82a03-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a03-120">Header</span><span class="sxs-lookup"><span data-stu-id="82a03-120">Header</span></span><br/>  | <dl> <span data-ttu-id="82a03-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82a03-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82a03-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82a03-122">Library</span></span><br/> | <dl> <span data-ttu-id="82a03-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="82a03-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a03-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82a03-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a03-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="82a03-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




