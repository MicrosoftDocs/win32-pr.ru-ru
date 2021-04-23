---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Ктрансформинпутпин. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657410"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="4443a-103">Ктрансформинпутпин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="4443a-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="4443a-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="4443a-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4443a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4443a-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="4443a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4443a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4443a-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="4443a-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4443a-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="4443a-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4443a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4443a-109">Return value</span></span>

<span data-ttu-id="4443a-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4443a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4443a-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4443a-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4443a-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4443a-112">Return code</span></span>                                                                                               | <span data-ttu-id="4443a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4443a-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="4443a-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4443a-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="4443a-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="4443a-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="4443a-116"><dt>**VFW \_ E \_ недопустимое \_ направление**</dt></span><span class="sxs-lookup"><span data-stu-id="4443a-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="4443a-117">Неправильное направление ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="4443a-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4443a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4443a-118">Remarks</span></span>

<span data-ttu-id="4443a-119">Этот метод переопределяет метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4443a-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="4443a-120">Он вызывает метод [**ктрансформфилтер:: чеккконнект**](ctransformfilter-checkconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="4443a-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="4443a-121">Производный класс может переопределить метод **ктрансформфилтер:: чеккконнект** для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="4443a-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="4443a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4443a-122">Requirements</span></span>



| <span data-ttu-id="4443a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4443a-123">Requirement</span></span> | <span data-ttu-id="4443a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4443a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4443a-125">Header</span><span class="sxs-lookup"><span data-stu-id="4443a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4443a-126"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4443a-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4443a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4443a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4443a-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4443a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




