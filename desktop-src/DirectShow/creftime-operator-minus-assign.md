---
description: Оператор-= Вычитает одно время ссылки из другого.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: Метод Крефтиме. operator-= (Рефтиме. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675712"
---
# <a name="creftimeoperator--method"></a><span data-ttu-id="bf2ea-103">Крефтиме. operator-= метод</span><span class="sxs-lookup"><span data-stu-id="bf2ea-103">CRefTime.operator-= method</span></span>

<span data-ttu-id="bf2ea-104">Оператор-= Вычитает одно время ссылки из другого.</span><span class="sxs-lookup"><span data-stu-id="bf2ea-104">The -= operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf2ea-105">Syntax</span></span>


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="bf2ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf2ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2ea-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="bf2ea-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ea-108">Ссылка на объект **крефтиме** .</span><span class="sxs-lookup"><span data-stu-id="bf2ea-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2ea-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf2ea-109">Return value</span></span>

<span data-ttu-id="bf2ea-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="bf2ea-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2ea-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bf2ea-111">Requirements</span></span>



| <span data-ttu-id="bf2ea-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bf2ea-112">Requirement</span></span> | <span data-ttu-id="bf2ea-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bf2ea-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2ea-114">Header</span><span class="sxs-lookup"><span data-stu-id="bf2ea-114">Header</span></span><br/>  | <dl> <span data-ttu-id="bf2ea-115"><dt>Рефтиме. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ea-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf2ea-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf2ea-116">Library</span></span><br/> | <dl> <span data-ttu-id="bf2ea-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ea-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




