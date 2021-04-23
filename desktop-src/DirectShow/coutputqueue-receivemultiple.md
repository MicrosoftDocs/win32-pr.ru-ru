---
description: Метод Рецеивемултипле доставляет пакет образцов мультимедиа во входной ПИН-код.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Каутпуткуеуе. Рецеивемултипле, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674880"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="acf47-103">Каутпуткуеуе. Рецеивемултипле, метод</span><span class="sxs-lookup"><span data-stu-id="acf47-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="acf47-104">`ReceiveMultiple`Метод доставляет пакет образцов мультимедиа во входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="acf47-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf47-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acf47-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="acf47-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="acf47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf47-107">*ппсамплес*</span><span class="sxs-lookup"><span data-stu-id="acf47-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="acf47-108">Адрес указателя на массив выборок.</span><span class="sxs-lookup"><span data-stu-id="acf47-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="acf47-109">*нсамплес*</span><span class="sxs-lookup"><span data-stu-id="acf47-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="acf47-110">Число выборок в массиве.</span><span class="sxs-lookup"><span data-stu-id="acf47-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="acf47-111">*нсамплеспроцессед*</span><span class="sxs-lookup"><span data-stu-id="acf47-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="acf47-112">Указатель на переменную, которая получает количество успешно доставленных выборок.</span><span class="sxs-lookup"><span data-stu-id="acf47-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf47-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acf47-113">Return value</span></span>

<span data-ttu-id="acf47-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acf47-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="acf47-115">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="acf47-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="acf47-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="acf47-116">Return code</span></span>                                                                             | <span data-ttu-id="acf47-117">Описание</span><span class="sxs-lookup"><span data-stu-id="acf47-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="acf47-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="acf47-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="acf47-119">Перед обработкой этого примера получено уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="acf47-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="acf47-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="acf47-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="acf47-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="acf47-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="acf47-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acf47-122">Remarks</span></span>

<span data-ttu-id="acf47-123">Если объект использует поток, этот метод помещает все образцы, переданные в массив, в очередь.</span><span class="sxs-lookup"><span data-stu-id="acf47-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="acf47-124">В противном случае метод вызывает метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="acf47-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf47-125">Требования</span><span class="sxs-lookup"><span data-stu-id="acf47-125">Requirements</span></span>



| <span data-ttu-id="acf47-126">Требование</span><span class="sxs-lookup"><span data-stu-id="acf47-126">Requirement</span></span> | <span data-ttu-id="acf47-127">Значение</span><span class="sxs-lookup"><span data-stu-id="acf47-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf47-128">Header</span><span class="sxs-lookup"><span data-stu-id="acf47-128">Header</span></span><br/>  | <dl> <span data-ttu-id="acf47-129"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acf47-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="acf47-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="acf47-130">Library</span></span><br/> | <dl> <span data-ttu-id="acf47-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="acf47-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf47-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acf47-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf47-133">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="acf47-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




