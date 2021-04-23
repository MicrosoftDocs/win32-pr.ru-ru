---
description: 'Метод Куеривендоринфо извлекает строку, содержащую сведения о поставщике. Этот метод реализует метод Ибасефилтер:: Куеривендоринфо.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Кбасефилтер. Куеривендоринфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658090"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="0e289-104">Кбасефилтер. Куеривендоринфо, метод</span><span class="sxs-lookup"><span data-stu-id="0e289-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="0e289-105">`QueryVendorInfo`Метод извлекает строку, содержащую сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="0e289-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="0e289-106">Этот метод реализует метод [**ибасефилтер:: куеривендоринфо**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .</span><span class="sxs-lookup"><span data-stu-id="0e289-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e289-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e289-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0e289-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e289-109">*пвендоринфо*</span><span class="sxs-lookup"><span data-stu-id="0e289-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0e289-110">Адрес переменной, которая получает указатель на строку расширенных символов, содержащую сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="0e289-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e289-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e289-111">Return value</span></span>

<span data-ttu-id="0e289-112">Возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="0e289-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e289-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e289-113">Remarks</span></span>

<span data-ttu-id="0e289-114">Чтобы предоставить сведения о поставщике для фильтра, Переопределите этот метод.</span><span class="sxs-lookup"><span data-stu-id="0e289-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="0e289-115">При реализации этого метода используйте функцию **CoTaskMemAlloc** , чтобы выделить память для строки.</span><span class="sxs-lookup"><span data-stu-id="0e289-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="0e289-116">Вызывающий объект отвечает за вызов функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="0e289-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e289-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0e289-117">Requirements</span></span>



| <span data-ttu-id="0e289-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0e289-118">Requirement</span></span> | <span data-ttu-id="0e289-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0e289-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e289-120">Header</span><span class="sxs-lookup"><span data-stu-id="0e289-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0e289-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e289-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0e289-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e289-122">Library</span></span><br/> | <dl> <span data-ttu-id="0e289-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0e289-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e289-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e289-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e289-125">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="0e289-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




