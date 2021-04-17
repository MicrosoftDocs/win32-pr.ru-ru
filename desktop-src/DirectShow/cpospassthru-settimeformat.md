---
description: 'Метод Сеттимеформат задает формат времени. Этот метод реализует метод Имедиасикинг:: Сеттимеформат.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Кпоспасссру. Сеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657365"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="20866-104">Кпоспасссру. Сеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="20866-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="20866-105">Метод Сеттимеформат задает формат времени.</span><span class="sxs-lookup"><span data-stu-id="20866-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="20866-106">Этот метод реализует метод [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="20866-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20866-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20866-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="20866-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20866-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20866-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="20866-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="20866-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="20866-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20866-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20866-111">Return value</span></span>

<span data-ttu-id="20866-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="20866-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="20866-113">Требования</span><span class="sxs-lookup"><span data-stu-id="20866-113">Requirements</span></span>



| <span data-ttu-id="20866-114">Требование</span><span class="sxs-lookup"><span data-stu-id="20866-114">Requirement</span></span> | <span data-ttu-id="20866-115">Значение</span><span class="sxs-lookup"><span data-stu-id="20866-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20866-116">Header</span><span class="sxs-lookup"><span data-stu-id="20866-116">Header</span></span><br/>  | <dl> <span data-ttu-id="20866-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20866-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20866-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20866-118">Library</span></span><br/> | <dl> <span data-ttu-id="20866-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="20866-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20866-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20866-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20866-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="20866-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="20866-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="20866-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




