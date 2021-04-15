---
description: Этот оператор проверяет равенство между объектами Кмедиатипе.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Кмедиатипе. Кмедиатипе:: operator = = метод (Мтипе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689102"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="9f97d-103">Кмедиатипе. Кмедиатипе:: operator = = метод</span><span class="sxs-lookup"><span data-stu-id="9f97d-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="9f97d-104">Этот оператор проверяет равенство между объектами [**кмедиатипе**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="9f97d-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f97d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f97d-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="9f97d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f97d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f97d-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="9f97d-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9f97d-108">Ссылка на объект **кмедиатипе** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="9f97d-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f97d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f97d-109">Return value</span></span>

<span data-ttu-id="9f97d-110">Возвращает **значение true** , если *RT* равно этому объекту.</span><span class="sxs-lookup"><span data-stu-id="9f97d-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="9f97d-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9f97d-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f97d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9f97d-112">Requirements</span></span>



| <span data-ttu-id="9f97d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9f97d-113">Requirement</span></span> | <span data-ttu-id="9f97d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9f97d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f97d-115">Header</span><span class="sxs-lookup"><span data-stu-id="9f97d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f97d-116"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f97d-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9f97d-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f97d-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f97d-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9f97d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f97d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f97d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f97d-120">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="9f97d-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




