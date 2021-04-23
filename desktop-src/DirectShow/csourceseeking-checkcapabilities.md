---
description: 'Метод Чекккапабилитиес запрашивает, есть ли у потока указанные возможности поиска. Этот метод реализует метод Имедиасикинг:: Чекккапабилитиес.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Ксаурцесикинг. Чекккапабилитиес, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657028"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="45ac6-104">Ксаурцесикинг. Чекккапабилитиес, метод</span><span class="sxs-lookup"><span data-stu-id="45ac6-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="45ac6-105">`CheckCapabilities`Метод запрашивает, имеет ли поток указанные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="45ac6-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="45ac6-106">Этот метод реализует метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="45ac6-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ac6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45ac6-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="45ac6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="45ac6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ac6-109">*пкапабилитиес*</span><span class="sxs-lookup"><span data-stu-id="45ac6-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="45ac6-110">Указатель на побитовую комбинацию одного или нескольких атрибутов [**\_ \_ \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) поиска.</span><span class="sxs-lookup"><span data-stu-id="45ac6-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ac6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45ac6-111">Return value</span></span>

<span data-ttu-id="45ac6-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="45ac6-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="45ac6-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="45ac6-113">Return code</span></span>                                                                               | <span data-ttu-id="45ac6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="45ac6-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45ac6-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="45ac6-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="45ac6-116">Существуют не все возможности в *пкапабилитиес* .</span><span class="sxs-lookup"><span data-stu-id="45ac6-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="45ac6-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="45ac6-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="45ac6-118">В *пкапабилитиес* есть все возможности.</span><span class="sxs-lookup"><span data-stu-id="45ac6-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="45ac6-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="45ac6-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="45ac6-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="45ac6-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="45ac6-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45ac6-121">Remarks</span></span>

<span data-ttu-id="45ac6-122">Как реализованный, этот метод проверяет значение *\* пкапабилитиес* на соответствие переменной члена [**ксаурцесикинг:: m \_ двсикингкапс**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="45ac6-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="45ac6-123">Однако он не устанавливает *\* пкапабилитиес* равным **m \_ двсикингкапс**, как описано в методе [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="45ac6-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="45ac6-124">Кроме того, в случае, если ни одна из указанных возможностей не доступна, метод не возвращает значение E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="45ac6-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="45ac6-125">Более полная реализация будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45ac6-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="45ac6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="45ac6-126">Requirements</span></span>



| <span data-ttu-id="45ac6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="45ac6-127">Requirement</span></span> | <span data-ttu-id="45ac6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="45ac6-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ac6-129">Header</span><span class="sxs-lookup"><span data-stu-id="45ac6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45ac6-130"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45ac6-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45ac6-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45ac6-131">Library</span></span><br/> | <dl> <span data-ttu-id="45ac6-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="45ac6-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ac6-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ac6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ac6-134">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="45ac6-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




