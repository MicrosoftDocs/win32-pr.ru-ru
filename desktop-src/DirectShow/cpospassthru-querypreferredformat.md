---
description: 'Метод Куерипреферредформат извлекает предпочтительный формат времени для потока. Этот метод реализует метод Имедиасикинг:: Куерипреферредформат.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Кпоспасссру. Куерипреферредформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675532"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="dcecf-104">Кпоспасссру. Куерипреферредформат, метод</span><span class="sxs-lookup"><span data-stu-id="dcecf-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="dcecf-105">`QueryPreferredFormat`Метод получает предпочтительный формат времени для потока.</span><span class="sxs-lookup"><span data-stu-id="dcecf-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="dcecf-106">Этот метод реализует метод [**имедиасикинг:: куерипреферредформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="dcecf-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcecf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcecf-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="dcecf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcecf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcecf-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="dcecf-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="dcecf-110">Указатель на переменную, которая получает GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="dcecf-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcecf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcecf-111">Return value</span></span>

<span data-ttu-id="dcecf-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="dcecf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcecf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dcecf-113">Requirements</span></span>



| <span data-ttu-id="dcecf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dcecf-114">Requirement</span></span> | <span data-ttu-id="dcecf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dcecf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcecf-116">Header</span><span class="sxs-lookup"><span data-stu-id="dcecf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dcecf-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcecf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcecf-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcecf-118">Library</span></span><br/> | <dl> <span data-ttu-id="dcecf-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dcecf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcecf-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcecf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcecf-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="dcecf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="dcecf-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="dcecf-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




