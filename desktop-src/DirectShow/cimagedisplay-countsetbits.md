---
description: Метод Каунтсетбитс возвращает число битов, заданное равным 1, в указанном битовом поле.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Цимажедисплай. Каунтсетбитс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679950"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="d349a-103">Цимажедисплай. Каунтсетбитс, метод</span><span class="sxs-lookup"><span data-stu-id="d349a-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="d349a-104">`CountSetBits`Метод возвращает число бит, установленное в 1, в указанном битовом поле.</span><span class="sxs-lookup"><span data-stu-id="d349a-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="d349a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d349a-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="d349a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d349a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d349a-107">*Поле*</span><span class="sxs-lookup"><span data-stu-id="d349a-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="d349a-108">Задает битовое поле в виде значения **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d349a-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d349a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d349a-109">Return value</span></span>

<span data-ttu-id="d349a-110">Возвращает число битов, для которых задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="d349a-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d349a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d349a-111">Requirements</span></span>



| <span data-ttu-id="d349a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d349a-112">Requirement</span></span> | <span data-ttu-id="d349a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d349a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d349a-114">Header</span><span class="sxs-lookup"><span data-stu-id="d349a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d349a-115"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d349a-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d349a-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d349a-116">Library</span></span><br/> | <dl> <span data-ttu-id="d349a-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d349a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d349a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d349a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d349a-119">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="d349a-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




