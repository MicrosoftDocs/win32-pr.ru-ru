---
description: Метод IsValid определяет, был ли для этого объекта назначен основной тип.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Метод Кмедиатипе. IsValid (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676009"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="678cf-103">Кмедиатипе. IsValid, метод</span><span class="sxs-lookup"><span data-stu-id="678cf-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="678cf-104">`IsValid`Метод определяет, был ли присвоен основной тип этому объекту.</span><span class="sxs-lookup"><span data-stu-id="678cf-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="678cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="678cf-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="678cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="678cf-106">Parameters</span></span>

<span data-ttu-id="678cf-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="678cf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="678cf-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="678cf-108">Return value</span></span>

<span data-ttu-id="678cf-109">Возвращает **значение true** , если этому объекту был назначен основной тип.</span><span class="sxs-lookup"><span data-stu-id="678cf-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="678cf-110">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="678cf-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="678cf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="678cf-111">Remarks</span></span>

<span data-ttu-id="678cf-112">По умолчанию объекты [**кмедиатипе**](cmediatype.md) инициализируются с помощью основного типа GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="678cf-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="678cf-113">Вызовите этот метод, чтобы определить, правильно ли инициализирован объект.</span><span class="sxs-lookup"><span data-stu-id="678cf-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="678cf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="678cf-114">Requirements</span></span>



| <span data-ttu-id="678cf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="678cf-115">Requirement</span></span> | <span data-ttu-id="678cf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="678cf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="678cf-117">Header</span><span class="sxs-lookup"><span data-stu-id="678cf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="678cf-118"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="678cf-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="678cf-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="678cf-119">Library</span></span><br/> | <dl> <span data-ttu-id="678cf-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="678cf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678cf-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="678cf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678cf-122">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="678cf-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




