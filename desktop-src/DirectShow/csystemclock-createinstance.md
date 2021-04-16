---
description: Метод CreateInstance создает новый экземпляр этого объекта.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Метод Ксистемклокк. CreateInstance (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658114"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="5f0ef-103">Ксистемклокк. CreateInstance, метод</span><span class="sxs-lookup"><span data-stu-id="5f0ef-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="5f0ef-104">`CreateInstance`Метод создает новый экземпляр этого объекта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f0ef-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="5f0ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f0ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0ef-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="5f0ef-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0ef-108">Указатель на агрегированный интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="5f0ef-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="5f0ef-109">*фр*</span><span class="sxs-lookup"><span data-stu-id="5f0ef-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0ef-110">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f0ef-111">Return value</span></span>

<span data-ttu-id="5f0ef-112">Возвращает указатель на новый экземпляр этого объекта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f0ef-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f0ef-113">Remarks</span></span>

<span data-ttu-id="5f0ef-114">Фабрика классов вызывает этот метод для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0ef-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5f0ef-115">Requirements</span></span>



| <span data-ttu-id="5f0ef-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5f0ef-116">Requirement</span></span> | <span data-ttu-id="5f0ef-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5f0ef-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0ef-118">Header</span><span class="sxs-lookup"><span data-stu-id="5f0ef-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5f0ef-119"><dt>Сисклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ef-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f0ef-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f0ef-120">Library</span></span><br/> | <dl> <span data-ttu-id="5f0ef-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ef-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




