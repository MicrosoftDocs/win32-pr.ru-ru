---
description: 'Метод Жеттимеформат извлекает текущий формат времени. Этот метод реализует метод Имедиасикинг:: Жеттимеформат.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Кпоспасссру. Жеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658020"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="e3c78-104">Кпоспасссру. Жеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="e3c78-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="e3c78-105">`GetTimeFormat`Метод получает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="e3c78-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="e3c78-106">Этот метод реализует метод [**имедиасикинг:: жеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="e3c78-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3c78-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e3c78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3c78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c78-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="e3c78-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e3c78-110">Указатель на переменную, которая получает GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="e3c78-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c78-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3c78-111">Return value</span></span>

<span data-ttu-id="e3c78-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e3c78-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c78-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e3c78-113">Requirements</span></span>



| <span data-ttu-id="e3c78-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e3c78-114">Requirement</span></span> | <span data-ttu-id="e3c78-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e3c78-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c78-116">Header</span><span class="sxs-lookup"><span data-stu-id="e3c78-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e3c78-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c78-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3c78-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3c78-118">Library</span></span><br/> | <dl> <span data-ttu-id="e3c78-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c78-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c78-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3c78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c78-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e3c78-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="e3c78-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="e3c78-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




