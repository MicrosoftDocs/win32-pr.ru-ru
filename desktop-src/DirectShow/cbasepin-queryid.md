---
description: 'Метод QueryId извлекает идентификатор ПИН-кода. Этот метод реализует метод Ипин:: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Кбасепин. QueryId, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668544"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="ac2cb-104">Кбасепин. QueryId, метод</span><span class="sxs-lookup"><span data-stu-id="ac2cb-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="ac2cb-105">`QueryId`Метод получает идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="ac2cb-106">Этот метод реализует метод [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="ac2cb-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac2cb-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="ac2cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac2cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac2cb-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="ac2cb-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="ac2cb-110">Указатель на идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac2cb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac2cb-111">Return value</span></span>

<span data-ttu-id="ac2cb-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac2cb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ac2cb-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="ac2cb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ac2cb-114">Return code</span></span>                                                                                   | <span data-ttu-id="ac2cb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ac2cb-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ac2cb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ac2cb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ac2cb-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ac2cb-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ac2cb-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ac2cb-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="ac2cb-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac2cb-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ac2cb-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="ac2cb-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac2cb-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac2cb-122">Remarks</span></span>

<span data-ttu-id="ac2cb-123">Этот метод возвращает копию переменной-члена [**кбасепин:: m \_ pName**](cbasepin-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2cb-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2cb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ac2cb-124">Requirements</span></span>



| <span data-ttu-id="ac2cb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ac2cb-125">Requirement</span></span> | <span data-ttu-id="ac2cb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ac2cb-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2cb-127">Header</span><span class="sxs-lookup"><span data-stu-id="ac2cb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ac2cb-128"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac2cb-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ac2cb-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac2cb-129">Library</span></span><br/> | <dl> <span data-ttu-id="ac2cb-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ac2cb-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac2cb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac2cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2cb-132">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="ac2cb-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




