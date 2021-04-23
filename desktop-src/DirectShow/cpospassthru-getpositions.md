---
description: 'Метод Disposition извлекает текущую и заданную позиции относительно общей продолжительности потока. Этот метод реализует метод Имедиасикинг:: Disposition.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Метод Кпоспасссру. Disposition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657538"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="e673f-104">Метод Кпоспасссру. Disposition</span><span class="sxs-lookup"><span data-stu-id="e673f-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="e673f-105">`GetPositions`Метод получает текущую и заданную позиции относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="e673f-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="e673f-106">Этот метод реализует метод [**имедиасикинг:: Disposition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="e673f-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e673f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e673f-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="e673f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e673f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e673f-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="e673f-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="e673f-110">Указатель на переменную, которая получает текущую координату в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="e673f-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="e673f-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="e673f-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="e673f-112">Указатель на переменную, которая получает точку окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="e673f-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e673f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e673f-113">Return value</span></span>

<span data-ttu-id="e673f-114">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e673f-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e673f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e673f-115">Requirements</span></span>



| <span data-ttu-id="e673f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e673f-116">Requirement</span></span> | <span data-ttu-id="e673f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e673f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e673f-118">Header</span><span class="sxs-lookup"><span data-stu-id="e673f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e673f-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e673f-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e673f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e673f-120">Library</span></span><br/> | <dl> <span data-ttu-id="e673f-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e673f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e673f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e673f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e673f-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e673f-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




