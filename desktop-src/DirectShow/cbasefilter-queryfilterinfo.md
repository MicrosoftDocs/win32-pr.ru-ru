---
description: 'Метод Куерифилтеринфо извлекает сведения о фильтре. Этот метод реализует метод Ибасефилтер:: Куерифилтеринфо.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Кбасефилтер. Куерифилтеринфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658091"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="18ee4-104">Кбасефилтер. Куерифилтеринфо, метод</span><span class="sxs-lookup"><span data-stu-id="18ee4-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="18ee4-105">`QueryFilterInfo`Метод получает сведения о фильтре.</span><span class="sxs-lookup"><span data-stu-id="18ee4-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="18ee4-106">Этот метод реализует метод [**ибасефилтер:: куерифилтеринфо**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .</span><span class="sxs-lookup"><span data-stu-id="18ee4-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ee4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18ee4-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="18ee4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ee4-109">*пинфо*</span><span class="sxs-lookup"><span data-stu-id="18ee4-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="18ee4-110">Указатель на структуру [**\_ сведений о фильтре**](/windows/win32/api/strmif/ns-strmif-filter_info) .</span><span class="sxs-lookup"><span data-stu-id="18ee4-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ee4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18ee4-111">Return value</span></span>

<span data-ttu-id="18ee4-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="18ee4-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ee4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18ee4-113">Remarks</span></span>

<span data-ttu-id="18ee4-114">Этот метод копирует имя фильтра из переменной члена [**кбасефилтер:: m \_ pName**](cbasefilter-m-pname.md) в элемент **АЧНАМЕ** \_ структуры сведений о фильтре.</span><span class="sxs-lookup"><span data-stu-id="18ee4-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="18ee4-115">Если **m \_ pname** имеет **значение NULL**, метод устанавливает **ачнаме** в L " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="18ee4-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="18ee4-116">Метод задает элемент **пграф** \_ структуры сведений о фильтре, равный переменной члена [**кбасефилтер:: m \_ пграф**](cbasefilter-m-pgraph.md) , и увеличивает счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="18ee4-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="18ee4-117">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="18ee4-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ee4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="18ee4-118">Requirements</span></span>



| <span data-ttu-id="18ee4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="18ee4-119">Requirement</span></span> | <span data-ttu-id="18ee4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="18ee4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ee4-121">Header</span><span class="sxs-lookup"><span data-stu-id="18ee4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="18ee4-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18ee4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="18ee4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18ee4-123">Library</span></span><br/> | <dl> <span data-ttu-id="18ee4-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="18ee4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ee4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18ee4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ee4-126">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="18ee4-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




