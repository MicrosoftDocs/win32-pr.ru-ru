---
description: Метод конструктора Кбаселист. Кбаселист.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Конструктор Кбаселист. Кбаселист (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096331"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="9ce7e-103">Кбаселист. Кбаселист, конструктор</span><span class="sxs-lookup"><span data-stu-id="9ce7e-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="9ce7e-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ce7e-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="9ce7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ce7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce7e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9ce7e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce7e-108">Указатель на имя списка.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ce7e-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ce7e-109">Remarks</span></span>

<span data-ttu-id="9ce7e-110">Для повышения эффективности `CBaseList` класс поддерживает кэш узлов списка.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="9ce7e-111">Эта версия конструктора использует размер кэша по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce7e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce7e-112">Requirements</span></span>



| <span data-ttu-id="9ce7e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce7e-113">Requirement</span></span> | <span data-ttu-id="9ce7e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce7e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce7e-115">Header</span><span class="sxs-lookup"><span data-stu-id="9ce7e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9ce7e-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9ce7e-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ce7e-117">Library</span></span><br/> | <dl> <span data-ttu-id="9ce7e-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce7e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9ce7e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce7e-120">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="9ce7e-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




