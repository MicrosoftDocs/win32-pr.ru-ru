---
description: Сведения о методе конструктора для Кженериклист. Кженериклист (Вкслист. h). Этот метод использует параметр "pName".
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Кженериклист. Кженериклист-конструктор (Вкслист. h) — параметр pName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914835"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="b2215-104">Кженериклист. Кженериклист-конструктор (Вкслист. h) — параметр pName</span><span class="sxs-lookup"><span data-stu-id="b2215-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="b2215-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="b2215-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2215-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2215-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="b2215-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2215-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2215-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="b2215-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b2215-109">Указатель на имя списка.</span><span class="sxs-lookup"><span data-stu-id="b2215-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2215-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2215-110">Remarks</span></span>

<span data-ttu-id="b2215-111">Для повышения эффективности `CGenericList` класс поддерживает кэш узлов списка.</span><span class="sxs-lookup"><span data-stu-id="b2215-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="b2215-112">Эта версия конструктора использует размер кэша по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2215-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2215-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b2215-113">Requirements</span></span>

| <span data-ttu-id="b2215-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b2215-114">Requirement</span></span> | <span data-ttu-id="b2215-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b2215-115">Value</span></span> |
|-|-|
| <span data-ttu-id="b2215-116">Header</span><span class="sxs-lookup"><span data-stu-id="b2215-116">Header</span></span> | <span data-ttu-id="b2215-117">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="b2215-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="b2215-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2215-118">Library</span></span>| <span data-ttu-id="b2215-119">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="b2215-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b2215-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2215-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2215-121">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="b2215-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




