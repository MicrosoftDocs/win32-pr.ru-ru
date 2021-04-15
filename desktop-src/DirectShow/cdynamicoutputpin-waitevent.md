---
description: Метод Ваитевент ожидает, пока заданное событие не будет сигнальным.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Кдинамикаутпутпин. Ваитевент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668936"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="c9455-103">Кдинамикаутпутпин. Ваитевент, метод</span><span class="sxs-lookup"><span data-stu-id="c9455-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="c9455-104">`WaitEvent`Метод ожидает, пока заданное событие не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="c9455-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9455-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9455-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c9455-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9455-107">*хевент*</span><span class="sxs-lookup"><span data-stu-id="c9455-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="c9455-108">Дескриптор события.</span><span class="sxs-lookup"><span data-stu-id="c9455-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9455-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9455-109">Return value</span></span>

<span data-ttu-id="c9455-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9455-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c9455-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9455-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c9455-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9455-112">Return code</span></span>                                                                                  | <span data-ttu-id="c9455-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c9455-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="c9455-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c9455-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c9455-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="c9455-116"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c9455-117">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c9455-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9455-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c9455-118">Requirements</span></span>



| <span data-ttu-id="c9455-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c9455-119">Requirement</span></span> | <span data-ttu-id="c9455-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c9455-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9455-121">Header</span><span class="sxs-lookup"><span data-stu-id="c9455-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9455-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c9455-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9455-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9455-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c9455-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9455-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9455-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9455-126">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c9455-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




