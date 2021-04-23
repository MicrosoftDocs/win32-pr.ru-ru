---
description: 'Метод capabilities извлекает все возможности поиска в потоке. Этот метод реализует метод Имедиасикинг:: Capabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Метод Ксаурцесикинг. Capabilities (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657508"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="740d2-104">Ксаурцесикинг. capabilities, метод</span><span class="sxs-lookup"><span data-stu-id="740d2-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="740d2-105">`GetCapabilities`Метод извлекает все возможности поиска в потоке.</span><span class="sxs-lookup"><span data-stu-id="740d2-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="740d2-106">Этот метод реализует метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="740d2-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="740d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="740d2-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="740d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="740d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="740d2-109">*пкапабилитиес*</span><span class="sxs-lookup"><span data-stu-id="740d2-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="740d2-110">Указатель на переменную, которая получает побитовую комбинацию флагов [**\_ \_ поиска \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="740d2-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="740d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="740d2-111">Return value</span></span>

<span data-ttu-id="740d2-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="740d2-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="740d2-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="740d2-113">Return code</span></span>                                                                               | <span data-ttu-id="740d2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="740d2-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="740d2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="740d2-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="740d2-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="740d2-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="740d2-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="740d2-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="740d2-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="740d2-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="740d2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="740d2-119">Remarks</span></span>

<span data-ttu-id="740d2-120">Возможности поиска задаются переменной члена [**ксаурцесикинг:: m \_ двсикингкапс**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="740d2-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="740d2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="740d2-121">Requirements</span></span>



| <span data-ttu-id="740d2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="740d2-122">Requirement</span></span> | <span data-ttu-id="740d2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="740d2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="740d2-124">Header</span><span class="sxs-lookup"><span data-stu-id="740d2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="740d2-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="740d2-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="740d2-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="740d2-126">Library</span></span><br/> | <dl> <span data-ttu-id="740d2-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="740d2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="740d2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="740d2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740d2-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="740d2-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




