---
description: Метод unadvise удаляет запрос Advise.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Метод Камсчедуле. unadvise (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657526"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="21436-103">Камсчедуле. unadvise, метод</span><span class="sxs-lookup"><span data-stu-id="21436-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="21436-104">`Unadvise`Метод удаляет запрос Advise.</span><span class="sxs-lookup"><span data-stu-id="21436-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="21436-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21436-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="21436-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21436-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21436-107">*двадвисекукие*</span><span class="sxs-lookup"><span data-stu-id="21436-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="21436-108">Идентификатор запроса advise, возвращаемый методом [**камсчедуле:: аддадвисепаккет**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="21436-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21436-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21436-109">Return value</span></span>

<span data-ttu-id="21436-110">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="21436-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="21436-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="21436-111">Return code</span></span>                                                                             | <span data-ttu-id="21436-112">Описание</span><span class="sxs-lookup"><span data-stu-id="21436-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="21436-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="21436-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="21436-114">Не найдено</span><span class="sxs-lookup"><span data-stu-id="21436-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="21436-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="21436-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="21436-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="21436-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="21436-117">Требования</span><span class="sxs-lookup"><span data-stu-id="21436-117">Requirements</span></span>



| <span data-ttu-id="21436-118">Требование</span><span class="sxs-lookup"><span data-stu-id="21436-118">Requirement</span></span> | <span data-ttu-id="21436-119">Значение</span><span class="sxs-lookup"><span data-stu-id="21436-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21436-120">Header</span><span class="sxs-lookup"><span data-stu-id="21436-120">Header</span></span><br/>  | <dl> <span data-ttu-id="21436-121"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21436-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="21436-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21436-122">Library</span></span><br/> | <dl> <span data-ttu-id="21436-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="21436-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21436-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21436-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21436-125">**Класс Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="21436-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




