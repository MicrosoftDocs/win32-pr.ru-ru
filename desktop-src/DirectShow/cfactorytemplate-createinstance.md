---
description: Метод CreateInstance вызывает функцию создания объекта для класса.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Метод Кфакторитемплате. CreateInstance (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657577"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="8e123-103">Кфакторитемплате. CreateInstance, метод</span><span class="sxs-lookup"><span data-stu-id="8e123-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="8e123-104">`CreateInstance`Метод вызывает функцию создания объекта для класса.</span><span class="sxs-lookup"><span data-stu-id="8e123-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e123-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e123-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="8e123-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e123-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8e123-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8e123-108">Указатель на агрегированный интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="8e123-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="8e123-109">*фр*</span><span class="sxs-lookup"><span data-stu-id="8e123-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8e123-110">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="8e123-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e123-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e123-111">Return value</span></span>

<span data-ttu-id="8e123-112">Возвращает экземпляр объекта класса.</span><span class="sxs-lookup"><span data-stu-id="8e123-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e123-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e123-113">Remarks</span></span>

<span data-ttu-id="8e123-114">Метод **IClassFactory:: CreateInstance** вызывает этот метод класса.</span><span class="sxs-lookup"><span data-stu-id="8e123-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="8e123-115">Этот метод вызывает функцию, на которую указывает переменная члена [**кфакторитемплате:: m \_ лпфннев**](cfactorytemplate-m-lpfnnew.md) .</span><span class="sxs-lookup"><span data-stu-id="8e123-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e123-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8e123-116">Requirements</span></span>



| <span data-ttu-id="8e123-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8e123-117">Requirement</span></span> | <span data-ttu-id="8e123-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8e123-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e123-119">Header</span><span class="sxs-lookup"><span data-stu-id="8e123-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8e123-120"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e123-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e123-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e123-121">Library</span></span><br/> | <dl> <span data-ttu-id="8e123-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8e123-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e123-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e123-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e123-124">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="8e123-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




