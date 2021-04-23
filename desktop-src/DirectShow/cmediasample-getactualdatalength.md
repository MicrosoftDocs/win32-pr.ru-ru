---
description: 'Метод Жетактуалдаталенгс извлекает длину допустимых данных в буфере. Этот метод реализует метод Имедиасампле:: Жетактуалдаталенгс.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Кмедиасампле. Жетактуалдаталенгс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669223"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="08a17-104">Кмедиасампле. Жетактуалдаталенгс, метод</span><span class="sxs-lookup"><span data-stu-id="08a17-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="08a17-105">`GetActualDataLength`Метод получает длину допустимых данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="08a17-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="08a17-106">Этот метод реализует метод [**имедиасампле:: жетактуалдаталенгс**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="08a17-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a17-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08a17-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="08a17-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08a17-108">Parameters</span></span>

<span data-ttu-id="08a17-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="08a17-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08a17-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08a17-110">Return value</span></span>

<span data-ttu-id="08a17-111">Возвращает длину допустимых данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="08a17-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a17-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a17-112">Remarks</span></span>

<span data-ttu-id="08a17-113">Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ лактуал**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="08a17-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a17-114">Требования</span><span class="sxs-lookup"><span data-stu-id="08a17-114">Requirements</span></span>



| <span data-ttu-id="08a17-115">Требование</span><span class="sxs-lookup"><span data-stu-id="08a17-115">Requirement</span></span> | <span data-ttu-id="08a17-116">Значение</span><span class="sxs-lookup"><span data-stu-id="08a17-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a17-117">Header</span><span class="sxs-lookup"><span data-stu-id="08a17-117">Header</span></span><br/>  | <dl> <span data-ttu-id="08a17-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08a17-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="08a17-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08a17-119">Library</span></span><br/> | <dl> <span data-ttu-id="08a17-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="08a17-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a17-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08a17-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a17-122">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="08a17-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

