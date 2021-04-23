---
description: Метод Дорендерсампле визуализирует пример.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Кбасерендерер. Дорендерсампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657477"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="a952a-103">Кбасерендерер. Дорендерсампле, метод</span><span class="sxs-lookup"><span data-stu-id="a952a-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="a952a-104">`DoRenderSample`Метод подготавливает к просмотру пример.</span><span class="sxs-lookup"><span data-stu-id="a952a-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a952a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a952a-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a952a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a952a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a952a-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="a952a-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a952a-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="a952a-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a952a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a952a-109">Return value</span></span>

<span data-ttu-id="a952a-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a952a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a952a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a952a-111">Remarks</span></span>

<span data-ttu-id="a952a-112">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="a952a-112">The derived class must implement this method.</span></span> <span data-ttu-id="a952a-113">Поведение полностью зависит от типа реализуемого фильтра.</span><span class="sxs-lookup"><span data-stu-id="a952a-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="a952a-114">Например, модуль подготовки видео будет рисовать видеоизображение, содержащееся в примере.</span><span class="sxs-lookup"><span data-stu-id="a952a-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="a952a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a952a-115">Requirements</span></span>



| <span data-ttu-id="a952a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a952a-116">Requirement</span></span> | <span data-ttu-id="a952a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a952a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a952a-118">Header</span><span class="sxs-lookup"><span data-stu-id="a952a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a952a-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a952a-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a952a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a952a-120">Library</span></span><br/> | <dl> <span data-ttu-id="a952a-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a952a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a952a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a952a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a952a-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="a952a-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




