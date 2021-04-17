---
description: Метод Receive вызывается, когда объект получает пример носителя из выходного ПИН-кода. Производный класс должен реализовывать этот метод.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Метод Кпуллпин. Receive (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679647"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="d182b-104">Кпуллпин. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="d182b-104">CPullPin.Receive method</span></span>

<span data-ttu-id="d182b-105">`Receive`Метод вызывается, когда объект получает пример мультимедиа из выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d182b-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="d182b-106">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="d182b-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d182b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d182b-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d182b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d182b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d182b-109">*псампле*</span><span class="sxs-lookup"><span data-stu-id="d182b-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d182b-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) примера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d182b-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d182b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d182b-111">Return value</span></span>

<span data-ttu-id="d182b-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d182b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d182b-113">Возврат значения, отличного от S \_ ОК, останавливает поток извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="d182b-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="d182b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d182b-114">Remarks</span></span>

<span data-ttu-id="d182b-115">Этот метод вызывается каждый раз, когда новый пример прибывает из выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d182b-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="d182b-116">Напишите этот метод точно так же, как метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="d182b-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="d182b-117">Метки времени в образце задают смещение в байтах относительно исходной начальной позиции, указанной в методе [**кпуллпин:: Seek**](cpullpin-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="d182b-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="d182b-118">Начальная позиция округляется вниз до ближайшей границы выравнивания, а позиция остановки округляется до ближайшей границы выравнивания.</span><span class="sxs-lookup"><span data-stu-id="d182b-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="d182b-119">Кроме того, если позиция окончания превышает общую длительность, вместо нее используется длительность.</span><span class="sxs-lookup"><span data-stu-id="d182b-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="d182b-120">Все отметки времени задаются как смещение в байтах, умноженное на 10 000 000, определенное как постоянные единицы.</span><span class="sxs-lookup"><span data-stu-id="d182b-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="d182b-121">Таким же, по одной секунде — один байт.</span><span class="sxs-lookup"><span data-stu-id="d182b-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="d182b-122">Чтобы найти фактические смещения в байтах, вызовите [**имедиасампле:: Time**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) и разделите результаты на единицы.</span><span class="sxs-lookup"><span data-stu-id="d182b-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="d182b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d182b-123">Requirements</span></span>



| <span data-ttu-id="d182b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d182b-124">Requirement</span></span> | <span data-ttu-id="d182b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d182b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d182b-126">Header</span><span class="sxs-lookup"><span data-stu-id="d182b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d182b-127"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="d182b-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d182b-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d182b-128">Library</span></span><br/> | <dl> <span data-ttu-id="d182b-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d182b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d182b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d182b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d182b-131">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="d182b-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




