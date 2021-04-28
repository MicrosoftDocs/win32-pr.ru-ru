---
description: 'Ксаурцесикинг. capabilities-метод — метод capabilities извлекает все возможности поиска в потоке. Этот метод реализует метод Имедиасикинг:: Capabilities.'
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
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098782"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="5e6c4-104">Ксаурцесикинг. capabilities, метод</span><span class="sxs-lookup"><span data-stu-id="5e6c4-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="5e6c4-105">`GetCapabilities`Метод извлекает все возможности поиска в потоке.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="5e6c4-106">Этот метод реализует метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="5e6c4-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e6c4-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="5e6c4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e6c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6c4-109">*пкапабилитиес*</span><span class="sxs-lookup"><span data-stu-id="5e6c4-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="5e6c4-110">Указатель на переменную, которая получает побитовую комбинацию флагов [**\_ \_ поиска \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="5e6c4-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6c4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e6c4-111">Return value</span></span>

<span data-ttu-id="5e6c4-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="5e6c4-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5e6c4-113">Return code</span></span>                                                                               | <span data-ttu-id="5e6c4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5e6c4-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="5e6c4-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5e6c4-116">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="5e6c4-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="5e6c4-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5e6c4-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="5e6c4-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e6c4-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="5e6c4-119">Remarks</span></span>

<span data-ttu-id="5e6c4-120">Возможности поиска задаются переменной члена [**ксаурцесикинг:: m \_ двсикингкапс**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="5e6c4-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6c4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5e6c4-121">Requirements</span></span>



| <span data-ttu-id="5e6c4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5e6c4-122">Requirement</span></span> | <span data-ttu-id="5e6c4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6c4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6c4-124">Header</span><span class="sxs-lookup"><span data-stu-id="5e6c4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5e6c4-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e6c4-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e6c4-126">Library</span></span><br/> | <dl> <span data-ttu-id="5e6c4-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e6c4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5e6c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6c4-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="5e6c4-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




