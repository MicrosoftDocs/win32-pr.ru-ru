---
description: Метод Блоккаутпутпин блокирует ПИН-код.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Кдинамикаутпутпин. Блоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658081"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="de244-103">Кдинамикаутпутпин. Блоккаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="de244-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="de244-104">`BlockOutputPin`Метод блокирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="de244-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="de244-105">Пока ПИН-код заблокирован, метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) ожидает, пока ПИН-код не будет разблокирован.</span><span class="sxs-lookup"><span data-stu-id="de244-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="de244-106">Состояние блокировки предотвращает появление образцов, изменение выходного формата или повторное подключение к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="de244-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="de244-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de244-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="de244-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de244-108">Parameters</span></span>

<span data-ttu-id="de244-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="de244-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de244-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de244-110">Return value</span></span>

<span data-ttu-id="de244-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="de244-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de244-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de244-112">Remarks</span></span>

<span data-ttu-id="de244-113">Перед вызовом этого метода удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="de244-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="de244-114">Не вызывайте этот метод, если поток потоковой передачи использует ПИН-код для доставки данных или изменения соединения.</span><span class="sxs-lookup"><span data-stu-id="de244-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="de244-115">Чтобы проверить, использует ли поток потоковой передачи ПИН-код, вызовите метод [**кдинамикаутпутпин:: стреамингсреадусингаутпутпин**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="de244-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="de244-116">Требования</span><span class="sxs-lookup"><span data-stu-id="de244-116">Requirements</span></span>



| <span data-ttu-id="de244-117">Требование</span><span class="sxs-lookup"><span data-stu-id="de244-117">Requirement</span></span> | <span data-ttu-id="de244-118">Значение</span><span class="sxs-lookup"><span data-stu-id="de244-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de244-119">Header</span><span class="sxs-lookup"><span data-stu-id="de244-119">Header</span></span><br/>  | <dl> <span data-ttu-id="de244-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de244-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de244-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de244-121">Library</span></span><br/> | <dl> <span data-ttu-id="de244-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="de244-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de244-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de244-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de244-124">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="de244-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




