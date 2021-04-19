---
description: Является устаревшей. Вместо этого используйте AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Функция Амовиесетупрегистерфилтер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688940"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="d4e26-104">Функция Амовиесетупрегистерфилтер</span><span class="sxs-lookup"><span data-stu-id="d4e26-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="d4e26-105">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="d4e26-105">Obsolete.</span></span> <span data-ttu-id="d4e26-106">Вместо этого используйте [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e26-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e26-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4e26-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="d4e26-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4e26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e26-109">*псетупдата*</span><span class="sxs-lookup"><span data-stu-id="d4e26-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e26-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d4e26-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d4e26-111">*пифм*</span><span class="sxs-lookup"><span data-stu-id="d4e26-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e26-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d4e26-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d4e26-113">*брегистер*</span><span class="sxs-lookup"><span data-stu-id="d4e26-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e26-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d4e26-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e26-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4e26-115">Return value</span></span>

<span data-ttu-id="d4e26-116">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4e26-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4e26-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4e26-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e26-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d4e26-118">Requirements</span></span>



| <span data-ttu-id="d4e26-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d4e26-119">Requirement</span></span> | <span data-ttu-id="d4e26-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d4e26-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e26-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4e26-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d4e26-122"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e26-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d4e26-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4e26-123">Library</span></span><br/> | <dl> <span data-ttu-id="d4e26-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e26-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e26-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4e26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e26-126">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="d4e26-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




