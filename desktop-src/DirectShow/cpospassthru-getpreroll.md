---
description: 'Метод Жетпреролл извлекает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиасикинг:: Жетпреролл.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Кпоспасссру. Жетпреролл, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675822"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="cc769-104">Кпоспасссру. Жетпреролл, метод</span><span class="sxs-lookup"><span data-stu-id="cc769-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="cc769-105">`GetPreroll`Метод получает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="cc769-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="cc769-106">Этот метод реализует метод [**имедиасикинг:: жетпреролл**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="cc769-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc769-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc769-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="cc769-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc769-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc769-109">*пллпреролл*</span><span class="sxs-lookup"><span data-stu-id="cc769-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="cc769-110">Указатель на переменную, которая получает время предвыполнения, в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="cc769-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc769-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc769-111">Return value</span></span>

<span data-ttu-id="cc769-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cc769-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc769-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cc769-113">Requirements</span></span>



| <span data-ttu-id="cc769-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cc769-114">Requirement</span></span> | <span data-ttu-id="cc769-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cc769-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc769-116">Header</span><span class="sxs-lookup"><span data-stu-id="cc769-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cc769-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc769-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc769-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc769-118">Library</span></span><br/> | <dl> <span data-ttu-id="cc769-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cc769-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc769-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc769-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc769-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="cc769-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




