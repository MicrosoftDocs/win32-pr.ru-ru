---
description: Метод Жеткуррентсампле извлекает текущий образец.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Кбасерендерер. Жеткуррентсампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657475"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="32734-103">Кбасерендерер. Жеткуррентсампле, метод</span><span class="sxs-lookup"><span data-stu-id="32734-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="32734-104">`GetCurrentSample`Метод извлекает текущий образец.</span><span class="sxs-lookup"><span data-stu-id="32734-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="32734-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32734-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="32734-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32734-106">Parameters</span></span>

<span data-ttu-id="32734-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="32734-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32734-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32734-108">Return value</span></span>

<span data-ttu-id="32734-109">Возвращает указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца или **значение NULL** , если образец недоступен.</span><span class="sxs-lookup"><span data-stu-id="32734-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="32734-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32734-110">Remarks</span></span>

<span data-ttu-id="32734-111">Если метод не возвращает **значение NULL**, метод вызывает **AddRef** для указателя [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="32734-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="32734-112">Вызывающий объект должен освободить указатель.</span><span class="sxs-lookup"><span data-stu-id="32734-112">The caller must release the pointer.</span></span> <span data-ttu-id="32734-113">(Неявно, необходимо присвоить возвращаемое значение переменной, чтобы его можно было освободить позже.)</span><span class="sxs-lookup"><span data-stu-id="32734-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="32734-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32734-114">Requirements</span></span>



| <span data-ttu-id="32734-115">Требование</span><span class="sxs-lookup"><span data-stu-id="32734-115">Requirement</span></span> | <span data-ttu-id="32734-116">Значение</span><span class="sxs-lookup"><span data-stu-id="32734-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32734-117">Header</span><span class="sxs-lookup"><span data-stu-id="32734-117">Header</span></span><br/>  | <dl> <span data-ttu-id="32734-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32734-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32734-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32734-119">Library</span></span><br/> | <dl> <span data-ttu-id="32734-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="32734-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32734-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32734-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32734-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="32734-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




