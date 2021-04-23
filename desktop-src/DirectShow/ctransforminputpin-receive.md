---
description: 'Метод Receive получает следующий образец носителя в потоке. Этот метод реализует метод Имеминпутпин:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Метод Ктрансформинпутпин. Receive (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658038"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="86943-104">Ктрансформинпутпин. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="86943-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="86943-105">`Receive`Метод получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="86943-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="86943-106">Этот метод реализует метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="86943-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86943-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86943-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="86943-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86943-109">*псампле*</span><span class="sxs-lookup"><span data-stu-id="86943-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="86943-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="86943-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86943-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86943-111">Return value</span></span>

<span data-ttu-id="86943-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86943-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="86943-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="86943-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="86943-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="86943-114">Return code</span></span>                                                                             | <span data-ttu-id="86943-115">Описание</span><span class="sxs-lookup"><span data-stu-id="86943-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="86943-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="86943-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="86943-117">ПИН-код в данный момент очищается; Пример отклонен.</span><span class="sxs-lookup"><span data-stu-id="86943-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="86943-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="86943-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="86943-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="86943-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="86943-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86943-120">Remarks</span></span>

<span data-ttu-id="86943-121">Этот метод вызывает метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) ПИН-кода, который проверяет состояние потоковой передачи ПИН-кода и проверяет наличие изменений формата в типе носителя.</span><span class="sxs-lookup"><span data-stu-id="86943-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="86943-122">Затем вызывается метод [**ктрансформфилтер:: Receive**](ctransformfilter-receive.md) фильтра, который обрабатывает пример и доставляет его в нисходящий.</span><span class="sxs-lookup"><span data-stu-id="86943-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="86943-123">Если фильтру необходимо получить доступ к примеру после возврата этого метода, он должен содержать счетчик ссылок путем вызова метода **IUnknown:: AddRef** в примере.</span><span class="sxs-lookup"><span data-stu-id="86943-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="86943-124">Например, некоторым фильтрам декодера требуется текущий пример для декодирования следующей выборки.</span><span class="sxs-lookup"><span data-stu-id="86943-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="86943-125">Требования</span><span class="sxs-lookup"><span data-stu-id="86943-125">Requirements</span></span>



| <span data-ttu-id="86943-126">Требование</span><span class="sxs-lookup"><span data-stu-id="86943-126">Requirement</span></span> | <span data-ttu-id="86943-127">Значение</span><span class="sxs-lookup"><span data-stu-id="86943-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86943-128">Header</span><span class="sxs-lookup"><span data-stu-id="86943-128">Header</span></span><br/>  | <dl> <span data-ttu-id="86943-129"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86943-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="86943-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86943-130">Library</span></span><br/> | <dl> <span data-ttu-id="86943-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="86943-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




