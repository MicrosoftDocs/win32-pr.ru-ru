---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются, пока для фильтра не будет выдана новая команда Run. Этот метод реализует метод Ипин:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Крендерединпутпин. EndOfStream, метод (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657468"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="edecf-104">Крендерединпутпин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="edecf-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="edecf-105">`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются, пока не будет выполнена новая команда запуска для фильтра.</span><span class="sxs-lookup"><span data-stu-id="edecf-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="edecf-106">Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="edecf-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="edecf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edecf-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="edecf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edecf-108">Parameters</span></span>

<span data-ttu-id="edecf-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="edecf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edecf-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edecf-110">Return value</span></span>

<span data-ttu-id="edecf-111">Возвращает \_ ОК, если успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="edecf-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="edecf-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edecf-112">Remarks</span></span>

<span data-ttu-id="edecf-113">Если фильтр выполняется, этот метод отправляет событие [**\_ завершения EC**](ec-complete.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="edecf-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="edecf-114">В противном случае устанавливает флаг, чтобы \_ при следующем запуске фильтра было отправлено событие EC Complete.</span><span class="sxs-lookup"><span data-stu-id="edecf-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="edecf-115">При сбросе фильтра снимается флажок.</span><span class="sxs-lookup"><span data-stu-id="edecf-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="edecf-116">Этот метод следует переопределить для удержания потоковой блокировки ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="edecf-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="edecf-117">Кроме того, если фильтр обрабатывает вызовы **Receive** асинхронно, ПИН-код должен подождать отправки события EC \_ Complete до тех пор, пока фильтр не обработал все отложенные выборки.</span><span class="sxs-lookup"><span data-stu-id="edecf-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="edecf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="edecf-118">Requirements</span></span>



| <span data-ttu-id="edecf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="edecf-119">Requirement</span></span> | <span data-ttu-id="edecf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="edecf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edecf-121">Header</span><span class="sxs-lookup"><span data-stu-id="edecf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="edecf-122"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edecf-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="edecf-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edecf-123">Library</span></span><br/> | <dl> <span data-ttu-id="edecf-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="edecf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edecf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edecf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edecf-126">**Класс Крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="edecf-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




