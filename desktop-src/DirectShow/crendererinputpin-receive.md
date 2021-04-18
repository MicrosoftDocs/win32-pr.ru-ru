---
description: 'Метод Receive получает следующий образец носителя в потоке. Этот метод переопределяет метод Кбасеинпутпин:: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Метод Крендереринпутпин. Receive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658007"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="b6e30-104">Крендереринпутпин. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="b6e30-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="b6e30-105">`Receive`Метод получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="b6e30-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="b6e30-106">Этот метод переопределяет метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="b6e30-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e30-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6e30-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b6e30-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6e30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e30-109">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="b6e30-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e30-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="b6e30-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e30-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6e30-111">Return value</span></span>

<span data-ttu-id="b6e30-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6e30-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e30-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6e30-113">Remarks</span></span>

<span data-ttu-id="b6e30-114">Этот метод вызывает метод [**кбасерендерер:: Receive**](cbaserenderer-receive.md) фильтра, который обрабатывает отрисовку.</span><span class="sxs-lookup"><span data-stu-id="b6e30-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="b6e30-115">В случае сбоя этого метода ПИН-код отправляет \_ событие EC еррораборт.</span><span class="sxs-lookup"><span data-stu-id="b6e30-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e30-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b6e30-116">Requirements</span></span>



| <span data-ttu-id="b6e30-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b6e30-117">Requirement</span></span> | <span data-ttu-id="b6e30-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b6e30-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e30-119">Header</span><span class="sxs-lookup"><span data-stu-id="b6e30-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b6e30-120"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6e30-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6e30-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6e30-121">Library</span></span><br/> | <dl> <span data-ttu-id="b6e30-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6e30-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e30-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6e30-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e30-124">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="b6e30-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




