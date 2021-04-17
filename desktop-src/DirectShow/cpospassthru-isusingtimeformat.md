---
description: 'Метод Исусингтимеформат определяет, является ли указанный формат времени используемым в данный момент форматом. Этот метод реализует метод Имедиасикинг:: Исусингтимеформат.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Кпоспасссру. Исусингтимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658016"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="4fcc8-104">Кпоспасссру. Исусингтимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="4fcc8-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="4fcc8-105">`IsUsingTimeFormat`Метод определяет, является ли указанный формат времени используемым в данный момент форматом.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="4fcc8-106">Этот метод реализует метод [**имедиасикинг:: исусингтимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .</span><span class="sxs-lookup"><span data-stu-id="4fcc8-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcc8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fcc8-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4fcc8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fcc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fcc8-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="4fcc8-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4fcc8-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fcc8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fcc8-111">Return value</span></span>

<span data-ttu-id="4fcc8-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fcc8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4fcc8-113">Requirements</span></span>



| <span data-ttu-id="4fcc8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4fcc8-114">Requirement</span></span> | <span data-ttu-id="4fcc8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc8-116">Header</span><span class="sxs-lookup"><span data-stu-id="4fcc8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4fcc8-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fcc8-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4fcc8-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fcc8-118">Library</span></span><br/> | <dl> <span data-ttu-id="4fcc8-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4fcc8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fcc8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fcc8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcc8-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="4fcc8-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="4fcc8-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="4fcc8-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




