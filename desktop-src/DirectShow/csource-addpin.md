---
description: Метод Аддпин добавляет новый выходной ПИН-код в фильтр.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Метод Ксаурце. Аддпин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665140"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="3ce56-103">Ксаурце. Аддпин, метод</span><span class="sxs-lookup"><span data-stu-id="3ce56-103">CSource.AddPin method</span></span>

<span data-ttu-id="3ce56-104">`AddPin`Метод добавляет новый выходной ПИН-код в фильтр.</span><span class="sxs-lookup"><span data-stu-id="3ce56-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ce56-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="3ce56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ce56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce56-107">*пстреам*</span><span class="sxs-lookup"><span data-stu-id="3ce56-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="3ce56-108">Указатель на объект [**ксаурцестреам**](csourcestream.md) , который реализует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3ce56-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce56-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ce56-109">Return value</span></span>

<span data-ttu-id="3ce56-110">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3ce56-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3ce56-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ce56-111">Return code</span></span>                                                                                   | <span data-ttu-id="3ce56-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3ce56-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="3ce56-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce56-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ce56-114">Успешно</span><span class="sxs-lookup"><span data-stu-id="3ce56-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="3ce56-115"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce56-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ce56-116">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="3ce56-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ce56-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ce56-117">Remarks</span></span>

<span data-ttu-id="3ce56-118">При создании нового ПИН-кода, производного от **ксаурцестреам**, конструктор **ксаурцестреам** автоматически вызывает этот метод для добавления выходного контакта в фильтр.</span><span class="sxs-lookup"><span data-stu-id="3ce56-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce56-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3ce56-119">Requirements</span></span>



| <span data-ttu-id="3ce56-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3ce56-120">Requirement</span></span> | <span data-ttu-id="3ce56-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3ce56-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce56-122">Header</span><span class="sxs-lookup"><span data-stu-id="3ce56-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3ce56-123"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ce56-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3ce56-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ce56-124">Library</span></span><br/> | <dl> <span data-ttu-id="3ce56-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3ce56-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce56-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ce56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce56-127">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="3ce56-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




