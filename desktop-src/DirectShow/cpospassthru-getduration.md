---
description: Кпоспасссру. Duration-метод — метод методаической длительности извлекает длительность потока. Этот метод реализует метод Имедиасикинг::/Duration.
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Кпоспасссру. метод Duration (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085582"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="dffe4-104">Кпоспасссру. метод Duration</span><span class="sxs-lookup"><span data-stu-id="dffe4-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="dffe4-105">`GetDuration`Метод получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="dffe4-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="dffe4-106">Этот метод реализует метод [**имедиасикинг::/Duration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="dffe4-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffe4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dffe4-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="dffe4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dffe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffe4-109">*пдуратион*</span><span class="sxs-lookup"><span data-stu-id="dffe4-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="dffe4-110">Указатель на переменную, которая получает длительность в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="dffe4-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffe4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dffe4-111">Return value</span></span>

<span data-ttu-id="dffe4-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="dffe4-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffe4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dffe4-113">Requirements</span></span>



| <span data-ttu-id="dffe4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dffe4-114">Requirement</span></span> | <span data-ttu-id="dffe4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dffe4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffe4-116">Header</span><span class="sxs-lookup"><span data-stu-id="dffe4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dffe4-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dffe4-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dffe4-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dffe4-118">Library</span></span><br/> | <dl> <span data-ttu-id="dffe4-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dffe4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffe4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="dffe4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffe4-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="dffe4-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




