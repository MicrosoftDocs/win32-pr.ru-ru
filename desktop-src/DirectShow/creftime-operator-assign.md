---
description: Оператор = назначает новое время ссылки.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Крефтиме. operator =-метод (Рефтиме. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679701"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="6c6ba-103">Крефтиме. operator =-метод (Рефтиме. h)</span><span class="sxs-lookup"><span data-stu-id="6c6ba-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="6c6ba-104">Оператор = назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c6ba-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="6c6ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c6ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6ba-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="6c6ba-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6ba-108">Ссылка на объект **крефтиме** , указывающий новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6ba-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c6ba-109">Return value</span></span>

<span data-ttu-id="6c6ba-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6ba-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6c6ba-111">Requirements</span></span>



| <span data-ttu-id="6c6ba-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6c6ba-112">Requirement</span></span> | <span data-ttu-id="6c6ba-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6c6ba-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6ba-114">Header</span><span class="sxs-lookup"><span data-stu-id="6c6ba-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6c6ba-115"><dt>Рефтиме. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c6ba-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c6ba-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c6ba-116">Library</span></span><br/> | <dl> <span data-ttu-id="6c6ba-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6c6ba-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




