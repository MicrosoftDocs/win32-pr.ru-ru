---
description: Кбасепин. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Кбасепин. Чеккконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096052"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="c9233-103">Кбасепин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="c9233-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="c9233-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="c9233-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9233-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9233-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c9233-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9233-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="c9233-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c9233-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c9233-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9233-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9233-109">Return value</span></span>

<span data-ttu-id="c9233-110">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9233-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c9233-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9233-111">Return code</span></span>                                                                                               | <span data-ttu-id="c9233-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c9233-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="c9233-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c9233-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="c9233-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c9233-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="c9233-115"><dt>**VFW \_ E \_ недопустимое \_ направление**</dt></span><span class="sxs-lookup"><span data-stu-id="c9233-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="c9233-116">Направления ПИН-кода несовместимы.</span><span class="sxs-lookup"><span data-stu-id="c9233-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9233-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c9233-117">Remarks</span></span>

<span data-ttu-id="c9233-118">Этот метод вызывается на обоих ПИН-кодах в начале процесса подключения.</span><span class="sxs-lookup"><span data-stu-id="c9233-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="c9233-119">Соединительный ПИН-код вызывает его в методе [**кбасепин:: Connect**](cbasepin-connect.md) , а принимающий ПИН-код вызывает его из метода [**Кбасепин:: рецеивеконнектион**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="c9233-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="c9233-120">Используйте этот метод, чтобы определить, подходит ли закрепление, заданное параметром *ппин* , для соединения.</span><span class="sxs-lookup"><span data-stu-id="c9233-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="c9233-121">Базовый класс возвращает ошибку, если оба контакта имеют одинаковое направление (как вход, так и оба вывода).</span><span class="sxs-lookup"><span data-stu-id="c9233-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="c9233-122">Производные классы могут переопределять этот метод для проверки других функций ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c9233-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="c9233-123">Например, класс [**кбасеаутпутпин**](cbaseoutputpin.md) запрашивает входной ПИН-код для своего интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="c9233-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="c9233-124">Если этот метод завершается неудачно, происходит сбой соединения, и ПИН-код вызывает метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c9233-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="c9233-125">Используйте **бреакконнект** , чтобы освободить все ресурсы, полученные в `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="c9233-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="c9233-126">Например, если `CheckConnect` вызывается метод **QueryInterface** , **бреакконнект** должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c9233-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9233-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c9233-127">Requirements</span></span>



| <span data-ttu-id="c9233-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c9233-128">Requirement</span></span> | <span data-ttu-id="c9233-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c9233-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9233-130">Header</span><span class="sxs-lookup"><span data-stu-id="c9233-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c9233-131"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9233-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c9233-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9233-132">Library</span></span><br/> | <dl> <span data-ttu-id="c9233-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c9233-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9233-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c9233-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9233-135">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="c9233-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




