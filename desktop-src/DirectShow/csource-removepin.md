---
description: Метод Ремовепин удаляет указанный ПИН-код из фильтра. Метод не удаляет ПИН-код.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Метод Ксаурце. Ремовепин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657905"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="b0185-104">Ксаурце. Ремовепин, метод</span><span class="sxs-lookup"><span data-stu-id="b0185-104">CSource.RemovePin method</span></span>

<span data-ttu-id="b0185-105">`RemovePin`Метод удаляет указанный ПИН-код из фильтра.</span><span class="sxs-lookup"><span data-stu-id="b0185-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="b0185-106">Метод не удаляет ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="b0185-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0185-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0185-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="b0185-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0185-109">*пстреам*</span><span class="sxs-lookup"><span data-stu-id="b0185-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="b0185-110">Указатель на объект [**ксаурцестреам**](csourcestream.md) , который реализует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="b0185-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0185-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0185-111">Return value</span></span>

<span data-ttu-id="b0185-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b0185-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b0185-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0185-113">Return code</span></span>                                                                             | <span data-ttu-id="b0185-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b0185-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b0185-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0185-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b0185-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b0185-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="b0185-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b0185-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b0185-118">Фильтр не содержит этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="b0185-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0185-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0185-119">Remarks</span></span>

<span data-ttu-id="b0185-120">Метод деструктора вызывает этот метод, чтобы удалить закрепление вывода из фильтра.</span><span class="sxs-lookup"><span data-stu-id="b0185-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0185-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b0185-121">Requirements</span></span>



| <span data-ttu-id="b0185-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b0185-122">Requirement</span></span> | <span data-ttu-id="b0185-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b0185-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0185-124">Header</span><span class="sxs-lookup"><span data-stu-id="b0185-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b0185-125"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0185-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b0185-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0185-126">Library</span></span><br/> | <dl> <span data-ttu-id="b0185-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b0185-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0185-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0185-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0185-129">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="b0185-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




