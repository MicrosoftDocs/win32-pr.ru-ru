---
description: Этот оператор проверяет неравенство между объектами Кмедиатипе.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'Кмедиатипе. Кмедиатипе:: operator! = метод (Мтипе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675198"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="04c0f-103">Кмедиатипе. Кмедиатипе:: operator! = метод</span><span class="sxs-lookup"><span data-stu-id="04c0f-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="04c0f-104">Этот оператор проверяет неравенство между объектами [**кмедиатипе**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="04c0f-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04c0f-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="04c0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04c0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c0f-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="04c0f-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="04c0f-108">Ссылка на объект **кмедиатипе** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="04c0f-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c0f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04c0f-109">Return value</span></span>

<span data-ttu-id="04c0f-110">Возвращает **значение true** , если *RT* не равен этому объекту.</span><span class="sxs-lookup"><span data-stu-id="04c0f-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="04c0f-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="04c0f-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04c0f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="04c0f-112">Requirements</span></span>



| <span data-ttu-id="04c0f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="04c0f-113">Requirement</span></span> | <span data-ttu-id="04c0f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="04c0f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c0f-115">Header</span><span class="sxs-lookup"><span data-stu-id="04c0f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="04c0f-116"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04c0f-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="04c0f-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04c0f-117">Library</span></span><br/> | <dl> <span data-ttu-id="04c0f-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="04c0f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04c0f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04c0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04c0f-120">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="04c0f-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




