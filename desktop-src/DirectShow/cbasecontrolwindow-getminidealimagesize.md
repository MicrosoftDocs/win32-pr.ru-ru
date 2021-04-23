---
description: Метод Жетминидеалимажесизе извлекает минимальный оптимальный размер изображения.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Кбасеконтролвиндов. Жетминидеалимажесизе, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657320"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a><span data-ttu-id="060e8-103">Кбасеконтролвиндов. Жетминидеалимажесизе, метод</span><span class="sxs-lookup"><span data-stu-id="060e8-103">CBaseControlWindow.GetMinIdealImageSize method</span></span>

<span data-ttu-id="060e8-104">`GetMinIdealImageSize`Метод получает минимальный оптимальный размер изображения.</span><span class="sxs-lookup"><span data-stu-id="060e8-104">The `GetMinIdealImageSize` method retrieves the minimum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="060e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="060e8-105">Syntax</span></span>


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="060e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="060e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060e8-107">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="060e8-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="060e8-108">Указатель на минимальную идеальную ширину (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="060e8-108">Pointer to the minimum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="060e8-109">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="060e8-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="060e8-110">Указатель на минимальную идеальную высоту (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="060e8-110">Pointer to the minimum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060e8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="060e8-111">Return value</span></span>

<span data-ttu-id="060e8-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="060e8-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="060e8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="060e8-113">Remarks</span></span>

<span data-ttu-id="060e8-114">Различные модули подготовки отчетов имеют ограничения производительности на размер отображаемых образов.</span><span class="sxs-lookup"><span data-stu-id="060e8-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="060e8-115">Несмотря на то, что они должны правильно работать при запросе на отображение изображений, превышающих указанное максимальное значение, модули подготовки отчетов могут выдавать минимальные и максимальные оптимальные размеры через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="060e8-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="060e8-116">Этот интерфейс может быть вызван только в том случае, если граф фильтра приостановлен или запущен, так как он не выделяется до тех пор, пока ресурсы не будут выделены и модуль подготовки отчетов не сможет распознать свои ограничения.</span><span class="sxs-lookup"><span data-stu-id="060e8-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="060e8-117">Если ограничений не существует, модуль подготовки отчетов заполняет параметры *пвидс* и *феигхт* собственными видеоизмерениями и возвращает \_ false.</span><span class="sxs-lookup"><span data-stu-id="060e8-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="060e8-118">Если существуют ограничения, то записываются ограниченная ширина и высота, а функция – член возвращает \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="060e8-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="060e8-119">Измерения применяются к размеру целевого видео, а не к общему размеру окна.</span><span class="sxs-lookup"><span data-stu-id="060e8-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="060e8-120">Таким образом, при вычислении размера окна, которое необходимо задать, следует учитывать текущий стиль окна (например, заголовок WS \_ и элемент WS \_ ).</span><span class="sxs-lookup"><span data-stu-id="060e8-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="060e8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="060e8-121">Requirements</span></span>



| <span data-ttu-id="060e8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="060e8-122">Requirement</span></span> | <span data-ttu-id="060e8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="060e8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="060e8-124">Header</span><span class="sxs-lookup"><span data-stu-id="060e8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="060e8-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="060e8-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="060e8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="060e8-126">Library</span></span><br/> | <dl> <span data-ttu-id="060e8-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="060e8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="060e8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="060e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060e8-129">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="060e8-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




