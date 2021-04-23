---
description: 'Метод Сетактуалдаталенгс задает длину допустимых данных в буфере. Этот метод реализует метод Имедиасампле:: Сетактуалдаталенгс.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Кмедиасампле. Сетактуалдаталенгс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665271"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="ceab2-104">Кмедиасампле. Сетактуалдаталенгс, метод</span><span class="sxs-lookup"><span data-stu-id="ceab2-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="ceab2-105">`SetActualDataLength`Метод задает длину допустимых данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="ceab2-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="ceab2-106">Этот метод реализует метод [**имедиасампле:: сетактуалдаталенгс**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="ceab2-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceab2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceab2-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="ceab2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceab2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceab2-109">*ллен*</span><span class="sxs-lookup"><span data-stu-id="ceab2-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="ceab2-110">Длина допустимых данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ceab2-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceab2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceab2-111">Return value</span></span>

<span data-ttu-id="ceab2-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ceab2-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ceab2-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ceab2-113">Return code</span></span>                                                                                             | <span data-ttu-id="ceab2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ceab2-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="ceab2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ceab2-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ceab2-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ceab2-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ceab2-117"><dt>**\_ \_ переполнение буфера VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ceab2-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="ceab2-118">*ллен* больше размера выделенного буфера.</span><span class="sxs-lookup"><span data-stu-id="ceab2-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ceab2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ceab2-119">Remarks</span></span>

<span data-ttu-id="ceab2-120">Этот метод задает переменную члена [**кмедиасампле:: m \_ лактуал**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="ceab2-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceab2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ceab2-121">Requirements</span></span>



| <span data-ttu-id="ceab2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ceab2-122">Requirement</span></span> | <span data-ttu-id="ceab2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ceab2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceab2-124">Header</span><span class="sxs-lookup"><span data-stu-id="ceab2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ceab2-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ceab2-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ceab2-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ceab2-126">Library</span></span><br/> | <dl> <span data-ttu-id="ceab2-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ceab2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceab2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ceab2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceab2-129">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="ceab2-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




