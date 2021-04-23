---
description: Метод конструктора.
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657397"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="e0021-103">Кбаселист. Кбаселист, конструктор</span><span class="sxs-lookup"><span data-stu-id="e0021-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="e0021-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e0021-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0021-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0021-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="e0021-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0021-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e0021-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e0021-108">Указатель на имя списка.</span><span class="sxs-lookup"><span data-stu-id="e0021-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0021-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0021-109">Remarks</span></span>

<span data-ttu-id="e0021-110">Для повышения эффективности `CBaseList` класс поддерживает кэш узлов списка.</span><span class="sxs-lookup"><span data-stu-id="e0021-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="e0021-111">Эта версия конструктора использует размер кэша по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0021-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0021-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e0021-112">Requirements</span></span>



| <span data-ttu-id="e0021-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e0021-113">Requirement</span></span> | <span data-ttu-id="e0021-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e0021-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0021-115">Header</span><span class="sxs-lookup"><span data-stu-id="e0021-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e0021-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0021-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e0021-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0021-117">Library</span></span><br/> | <dl> <span data-ttu-id="e0021-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0021-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0021-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0021-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0021-120">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="e0021-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




