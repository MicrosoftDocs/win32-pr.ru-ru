---
description: Метод Чекксизес проверяет свойства распределителя относительно текущего типа носителя.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Цимажеаллокатор. Чекксизес, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675829"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="a0171-103">Цимажеаллокатор. Чекксизес, метод</span><span class="sxs-lookup"><span data-stu-id="a0171-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="a0171-104">`CheckSizes`Метод проверяет свойства распределителя по отношению к текущему типу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a0171-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0171-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0171-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="a0171-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0171-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0171-107">*предпоручение*</span><span class="sxs-lookup"><span data-stu-id="a0171-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a0171-108">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , описывающую запрошенные свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="a0171-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0171-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0171-109">Return value</span></span>

<span data-ttu-id="a0171-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0171-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a0171-111">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="a0171-111">Possible values include the following.</span></span>



| <span data-ttu-id="a0171-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a0171-112">Return code</span></span>                                                                                           | <span data-ttu-id="a0171-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a0171-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0171-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a0171-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a0171-115">Запрошенные свойства совместимы с типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a0171-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="a0171-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a0171-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="a0171-117">Запрошенные свойства несовместимы с типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a0171-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="a0171-118"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="a0171-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a0171-119">ПИН-код владельца не подключен.</span><span class="sxs-lookup"><span data-stu-id="a0171-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="a0171-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0171-120">Remarks</span></span>

<span data-ttu-id="a0171-121">Если возвращаемое значение равно S, то при возврате \_ *из метода* элемент **кббуффер** в параметре "предактуальный" содержит фактический размер буфера.</span><span class="sxs-lookup"><span data-stu-id="a0171-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="a0171-122">Это может быть больше запрошенного размера, но никогда не будет меньше.</span><span class="sxs-lookup"><span data-stu-id="a0171-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0171-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a0171-123">Requirements</span></span>



| <span data-ttu-id="a0171-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a0171-124">Requirement</span></span> | <span data-ttu-id="a0171-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a0171-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0171-126">Header</span><span class="sxs-lookup"><span data-stu-id="a0171-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a0171-127"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0171-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0171-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0171-128">Library</span></span><br/> | <dl> <span data-ttu-id="a0171-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a0171-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0171-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0171-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0171-131">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="a0171-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




