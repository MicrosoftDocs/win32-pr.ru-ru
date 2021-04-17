---
description: 'Метод Бегинфлуш начинает операцию очистки. Этот метод реализует метод Ипин:: Бегинфлуш.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Ктрансформинпутпин. Бегинфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657361"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="80a6c-104">Ктрансформинпутпин. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="80a6c-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="80a6c-105">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="80a6c-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="80a6c-106">Этот метод реализует метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="80a6c-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a6c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80a6c-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="80a6c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80a6c-108">Parameters</span></span>

<span data-ttu-id="80a6c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="80a6c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80a6c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80a6c-110">Return value</span></span>

<span data-ttu-id="80a6c-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80a6c-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="80a6c-112">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="80a6c-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="80a6c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="80a6c-113">Return code</span></span>                                                                                           | <span data-ttu-id="80a6c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="80a6c-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="80a6c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="80a6c-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="80a6c-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="80a6c-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="80a6c-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="80a6c-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="80a6c-118">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="80a6c-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80a6c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80a6c-119">Remarks</span></span>

<span data-ttu-id="80a6c-120">Этот метод вызывает метод [**кбасеинпутпин:: бегинфлуш**](cbaseinputpin-beginflush.md) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="80a6c-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="80a6c-121">Затем вызывается метод [**ктрансформфилтер:: бегинфлуш**](ctransformfilter-beginflush.md) фильтра для предоставления вызова в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="80a6c-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a6c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="80a6c-122">Requirements</span></span>



| <span data-ttu-id="80a6c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="80a6c-123">Requirement</span></span> | <span data-ttu-id="80a6c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="80a6c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a6c-125">Header</span><span class="sxs-lookup"><span data-stu-id="80a6c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="80a6c-126"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80a6c-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80a6c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80a6c-127">Library</span></span><br/> | <dl> <span data-ttu-id="80a6c-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="80a6c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




