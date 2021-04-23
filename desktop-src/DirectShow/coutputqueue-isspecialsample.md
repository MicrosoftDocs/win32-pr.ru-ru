---
description: Метод ИсспеЦиалсампле определяет, являются ли данные в очереди управляющим сообщением.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Каутпуткуеуе. ИсспеЦиалсампле, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665339"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="adf0f-103">Каутпуткуеуе. ИсспеЦиалсампле, метод</span><span class="sxs-lookup"><span data-stu-id="adf0f-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="adf0f-104">`IsSpecialSample`Метод определяет, являются ли данные в очереди управляющим сообщением.</span><span class="sxs-lookup"><span data-stu-id="adf0f-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adf0f-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="adf0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adf0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf0f-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="adf0f-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="adf0f-108">Указатель на элемент в очереди.</span><span class="sxs-lookup"><span data-stu-id="adf0f-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf0f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adf0f-109">Return value</span></span>

<span data-ttu-id="adf0f-110">Возвращает **значение true** , если *псампле* является управляющим сообщением, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="adf0f-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="adf0f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adf0f-111">Remarks</span></span>

<span data-ttu-id="adf0f-112">Метод [**каутпуткуеуе:: QueueSample**](coutputqueue-queuesample.md) может получать управляющие сообщения в дополнение к примерам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="adf0f-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="adf0f-113">Управляющее сообщение — это определенная константа (приведение к \_ типу Long PTR), которая указывает потоку выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="adf0f-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="adf0f-114">Управляющие сообщения не содержат данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="adf0f-114">Control messages do not contain media data.</span></span> <span data-ttu-id="adf0f-115">Дополнительные сведения см. в разделе **каутпуткуеуе:: QueueSample**.</span><span class="sxs-lookup"><span data-stu-id="adf0f-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf0f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="adf0f-116">Requirements</span></span>



| <span data-ttu-id="adf0f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="adf0f-117">Requirement</span></span> | <span data-ttu-id="adf0f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="adf0f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf0f-119">Header</span><span class="sxs-lookup"><span data-stu-id="adf0f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="adf0f-120"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adf0f-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adf0f-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="adf0f-121">Library</span></span><br/> | <dl> <span data-ttu-id="adf0f-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="adf0f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf0f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adf0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf0f-124">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="adf0f-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




