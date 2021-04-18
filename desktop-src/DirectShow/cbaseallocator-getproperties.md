---
description: 'Метод WebMethod извлекает количество буферов, которые будут созданы распределителем, и свойства буфера. Этот метод реализует метод Имемаллокатор:: Properties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Метод Кбасеаллокатор.-Properties (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657332"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="8c1d2-104">Кбасеаллокатор... Properties, метод</span><span class="sxs-lookup"><span data-stu-id="8c1d2-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="8c1d2-105">`GetProperties`Метод получает количество буферов, которые будут созданы распределителем, и свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="8c1d2-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="8c1d2-106">Этот метод реализует метод [**имемаллокатор:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="8c1d2-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c1d2-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="8c1d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c1d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c1d2-109">*ппропс*</span><span class="sxs-lookup"><span data-stu-id="8c1d2-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="8c1d2-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая получает свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="8c1d2-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c1d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c1d2-111">Return value</span></span>

<span data-ttu-id="8c1d2-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8c1d2-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1d2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8c1d2-113">Requirements</span></span>



| <span data-ttu-id="8c1d2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8c1d2-114">Requirement</span></span> | <span data-ttu-id="8c1d2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8c1d2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1d2-116">Header</span><span class="sxs-lookup"><span data-stu-id="8c1d2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8c1d2-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c1d2-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c1d2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c1d2-118">Library</span></span><br/> | <dl> <span data-ttu-id="8c1d2-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8c1d2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1d2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c1d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1d2-121">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="8c1d2-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




