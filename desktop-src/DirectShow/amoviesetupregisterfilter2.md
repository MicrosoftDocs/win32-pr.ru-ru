---
description: Функция AMovieSetupRegisterFilter2 регистрирует в реестре, ПИН-коды и типы мультимедиа, с помощью интерфейса IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Функция AMovieSetupRegisterFilter2 (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657837"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="4739a-103">Функция AMovieSetupRegisterFilter2</span><span class="sxs-lookup"><span data-stu-id="4739a-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="4739a-104">Функция **AMovieSetupRegisterFilter2** регистрирует в реестре, ПИН-коды и типы мультимедиа, с помощью интерфейса [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="4739a-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4739a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4739a-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="4739a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4739a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4739a-107">*псетупдата*</span><span class="sxs-lookup"><span data-stu-id="4739a-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="4739a-108">Указатель на данные [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="4739a-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="4739a-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="4739a-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="4739a-110">Указатель на интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="4739a-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4739a-111">*брегистер*</span><span class="sxs-lookup"><span data-stu-id="4739a-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="4739a-112">Значение, указывающее, следует ли регистрировать фильтр. **Значение true** указывает зарегистрировать фильтр, **значение false** — отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="4739a-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4739a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4739a-113">Return value</span></span>

<span data-ttu-id="4739a-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4739a-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4739a-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4739a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4739a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4739a-116">Remarks</span></span>

<span data-ttu-id="4739a-117">Функция [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) вызывает эту вспомогательную функцию для регистрации фильтра после регистрации сервера COM.</span><span class="sxs-lookup"><span data-stu-id="4739a-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="4739a-118">Как правило, фильтр будет использовать [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) и не будет вызывать эту функцию напрямую.</span><span class="sxs-lookup"><span data-stu-id="4739a-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="4739a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4739a-119">Requirements</span></span>



| <span data-ttu-id="4739a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4739a-120">Requirement</span></span> | <span data-ttu-id="4739a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4739a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4739a-122">Header</span><span class="sxs-lookup"><span data-stu-id="4739a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4739a-123"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4739a-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4739a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4739a-124">Library</span></span><br/> | <dl> <span data-ttu-id="4739a-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4739a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4739a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4739a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4739a-127">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="4739a-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




