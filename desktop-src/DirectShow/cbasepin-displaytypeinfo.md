---
description: Метод Дисплайтипеинфо отображает сведения о типе носителя во время отладки.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Кбасепин. Дисплайтипеинфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657514"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="983e5-103">Кбасепин. Дисплайтипеинфо, метод</span><span class="sxs-lookup"><span data-stu-id="983e5-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="983e5-104">`DisplayTypeInfo`Метод отображает сведения о типе носителя во время отладки.</span><span class="sxs-lookup"><span data-stu-id="983e5-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="983e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="983e5-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="983e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="983e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983e5-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="983e5-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="983e5-108">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="983e5-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="983e5-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="983e5-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="983e5-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="983e5-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983e5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="983e5-111">Return value</span></span>

<span data-ttu-id="983e5-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="983e5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="983e5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="983e5-113">Remarks</span></span>

<span data-ttu-id="983e5-114">В отладочных сборках этот метод вызывает функцию [**дбглог**](dbglog.md) для вывода указанного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="983e5-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="983e5-115">В розничных сборках этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="983e5-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="983e5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="983e5-116">Requirements</span></span>



| <span data-ttu-id="983e5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="983e5-117">Requirement</span></span> | <span data-ttu-id="983e5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="983e5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983e5-119">Header</span><span class="sxs-lookup"><span data-stu-id="983e5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="983e5-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="983e5-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="983e5-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="983e5-121">Library</span></span><br/> | <dl> <span data-ttu-id="983e5-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="983e5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983e5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="983e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983e5-124">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="983e5-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




