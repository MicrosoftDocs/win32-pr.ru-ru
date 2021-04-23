---
description: Метод Чанжестарт вызывается при изменении начальной координаты.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Ксаурцесикинг. Чанжестарт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658032"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="dbcba-103">Ксаурцесикинг. Чанжестарт, метод</span><span class="sxs-lookup"><span data-stu-id="dbcba-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="dbcba-104">`ChangeStart`Метод вызывается при изменении начальной должности.</span><span class="sxs-lookup"><span data-stu-id="dbcba-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbcba-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="dbcba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbcba-106">Parameters</span></span>

<span data-ttu-id="dbcba-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dbcba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbcba-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbcba-108">Return value</span></span>

<span data-ttu-id="dbcba-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbcba-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbcba-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbcba-110">Remarks</span></span>

<span data-ttu-id="dbcba-111">Метод [**ксаурцесикинг:: сетпоситионс**](csourceseeking-setpositions.md) вызывает этот метод при изменении начальной должности.</span><span class="sxs-lookup"><span data-stu-id="dbcba-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="dbcba-112">Этот метод является чисто виртуальным; производный класс должен реализовать его.</span><span class="sxs-lookup"><span data-stu-id="dbcba-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="dbcba-113">После операции поиска штампы времени должны перезапускаться с нуля.</span><span class="sxs-lookup"><span data-stu-id="dbcba-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="dbcba-114">Время работы с носителями должно соответствовать новому времени начала.</span><span class="sxs-lookup"><span data-stu-id="dbcba-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="dbcba-115">В следующем примере показана возможная реализация:</span><span class="sxs-lookup"><span data-stu-id="dbcba-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="dbcba-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dbcba-116">Requirements</span></span>



| <span data-ttu-id="dbcba-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dbcba-117">Requirement</span></span> | <span data-ttu-id="dbcba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dbcba-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcba-119">Header</span><span class="sxs-lookup"><span data-stu-id="dbcba-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dbcba-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbcba-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dbcba-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbcba-121">Library</span></span><br/> | <dl> <span data-ttu-id="dbcba-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dbcba-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbcba-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbcba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcba-124">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="dbcba-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




