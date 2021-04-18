---
description: 'Метод Куерякцепт определяет, принимает ли ПИН-код указанный тип носителя. Этот метод реализует метод Ипин:: Куерякцепт.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Кбасепин. Куерякцепт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669501"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="814aa-104">Кбасепин. Куерякцепт, метод</span><span class="sxs-lookup"><span data-stu-id="814aa-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="814aa-105">`QueryAccept`Метод определяет, принимает ли ПИН-код указанный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="814aa-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="814aa-106">Этот метод реализует метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .</span><span class="sxs-lookup"><span data-stu-id="814aa-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="814aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="814aa-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="814aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="814aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814aa-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="814aa-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="814aa-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="814aa-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814aa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="814aa-111">Return value</span></span>

<span data-ttu-id="814aa-112">\_Если тип мультимедиа является допустимым, возвращается значение ОК.</span><span class="sxs-lookup"><span data-stu-id="814aa-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="814aa-113">В противном случае возвращает \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="814aa-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="814aa-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="814aa-114">Remarks</span></span>

<span data-ttu-id="814aa-115">В базовом классе этот метод делегирует методу [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="814aa-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="814aa-116">Если **чеккмедиатипе** завершается сбоем, `QueryAccept` возвращает \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="814aa-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="814aa-117">Этот метод не удерживает критическую секцию закрепления ([**кбасепин:: m \_ плокк**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="814aa-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="814aa-118">Если производный класс динамически изменяет набор допустимых типов мультимедиа, следует переопределить этот метод для хранения критической секции.</span><span class="sxs-lookup"><span data-stu-id="814aa-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="814aa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="814aa-119">Requirements</span></span>



| <span data-ttu-id="814aa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="814aa-120">Requirement</span></span> | <span data-ttu-id="814aa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="814aa-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814aa-122">Header</span><span class="sxs-lookup"><span data-stu-id="814aa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="814aa-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="814aa-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="814aa-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="814aa-124">Library</span></span><br/> | <dl> <span data-ttu-id="814aa-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="814aa-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814aa-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="814aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814aa-127">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="814aa-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




