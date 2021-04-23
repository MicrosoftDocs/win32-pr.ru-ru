---
description: Метод Форцерефреш устарел.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Кпоспасссру. Форцерефреш, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675785"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="1bc2f-103">Кпоспасссру. Форцерефреш, метод</span><span class="sxs-lookup"><span data-stu-id="1bc2f-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="1bc2f-104">`ForceRefresh`Метод устарел.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bc2f-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="1bc2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bc2f-106">Parameters</span></span>

<span data-ttu-id="1bc2f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bc2f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bc2f-108">Return value</span></span>

<span data-ttu-id="1bc2f-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc2f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bc2f-110">Remarks</span></span>

<span data-ttu-id="1bc2f-111">Изначально этот класс был разработан для кэширования указателей на интерфейсы [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="1bc2f-112">`ForceRefresh`Метод освободил эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="1bc2f-113">Как уже реализовано, этот класс не кэширует эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="1bc2f-114">Для обеспечения совместимости `ForceRefresh` метод по-прежнему включается, но возвращает \_ ОК, не делая ничего.</span><span class="sxs-lookup"><span data-stu-id="1bc2f-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc2f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1bc2f-115">Requirements</span></span>



| <span data-ttu-id="1bc2f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1bc2f-116">Requirement</span></span> | <span data-ttu-id="1bc2f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1bc2f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc2f-118">Header</span><span class="sxs-lookup"><span data-stu-id="1bc2f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1bc2f-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc2f-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1bc2f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1bc2f-120">Library</span></span><br/> | <dl> <span data-ttu-id="1bc2f-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc2f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc2f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bc2f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc2f-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="1bc2f-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




