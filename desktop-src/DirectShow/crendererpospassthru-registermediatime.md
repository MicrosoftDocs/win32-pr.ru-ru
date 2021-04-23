---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657174"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="89f2f-103">Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)</span><span class="sxs-lookup"><span data-stu-id="89f2f-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="89f2f-104">Метод **регистермедиатиме** кэширует метки времени из текущего образца.</span><span class="sxs-lookup"><span data-stu-id="89f2f-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89f2f-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="89f2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89f2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f2f-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="89f2f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="89f2f-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="89f2f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f2f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89f2f-109">Return value</span></span>

<span data-ttu-id="89f2f-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89f2f-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="89f2f-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="89f2f-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="89f2f-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="89f2f-112">Return code</span></span>                                                                                                  | <span data-ttu-id="89f2f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="89f2f-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="89f2f-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="89f2f-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="89f2f-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="89f2f-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="89f2f-116"><dt>**\_ \_ \_ \_ не задано время в \_ подключении к VFW E Media**</dt></span><span class="sxs-lookup"><span data-stu-id="89f2f-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="89f2f-117">Образец не имеет отметки времени.</span><span class="sxs-lookup"><span data-stu-id="89f2f-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89f2f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89f2f-118">Remarks</span></span>

<span data-ttu-id="89f2f-119">Этот метод сохраняет метки времени из текущего образца.</span><span class="sxs-lookup"><span data-stu-id="89f2f-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="89f2f-120">Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.</span><span class="sxs-lookup"><span data-stu-id="89f2f-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="89f2f-121">Фильтр должен вызывать этот метод для каждого получаемого примера.</span><span class="sxs-lookup"><span data-stu-id="89f2f-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="89f2f-122">Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.</span><span class="sxs-lookup"><span data-stu-id="89f2f-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f2f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="89f2f-123">Requirements</span></span>



| <span data-ttu-id="89f2f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="89f2f-124">Requirement</span></span> | <span data-ttu-id="89f2f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="89f2f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f2f-126">Header</span><span class="sxs-lookup"><span data-stu-id="89f2f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="89f2f-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89f2f-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89f2f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89f2f-128">Library</span></span><br/> | <dl> <span data-ttu-id="89f2f-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89f2f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




