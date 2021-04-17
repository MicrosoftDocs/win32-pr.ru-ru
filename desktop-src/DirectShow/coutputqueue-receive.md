---
description: Метод Receive доставляет пример носителя во входной ПИН-код.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Метод Каутпуткуеуе. Receive (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665149"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="2ab20-103">Каутпуткуеуе. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="2ab20-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="2ab20-104">`Receive`Метод доставляет пример носителя во входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="2ab20-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ab20-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="2ab20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ab20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab20-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="2ab20-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2ab20-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="2ab20-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab20-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ab20-109">Return value</span></span>

<span data-ttu-id="2ab20-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ab20-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2ab20-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2ab20-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2ab20-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2ab20-112">Return code</span></span>                                                                             | <span data-ttu-id="2ab20-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2ab20-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ab20-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2ab20-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2ab20-115">Перед обработкой этого примера получено уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="2ab20-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="2ab20-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2ab20-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2ab20-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2ab20-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="2ab20-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ab20-118">Remarks</span></span>

<span data-ttu-id="2ab20-119">Этот метод вызывает метод [**каутпуткуеуе:: рецеивемултипле**](coutputqueue-receivemultiple.md) .</span><span class="sxs-lookup"><span data-stu-id="2ab20-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab20-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2ab20-120">Requirements</span></span>



| <span data-ttu-id="2ab20-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2ab20-121">Requirement</span></span> | <span data-ttu-id="2ab20-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2ab20-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab20-123">Header</span><span class="sxs-lookup"><span data-stu-id="2ab20-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2ab20-124"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab20-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2ab20-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ab20-125">Library</span></span><br/> | <dl> <span data-ttu-id="2ab20-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab20-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab20-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ab20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab20-128">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="2ab20-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




