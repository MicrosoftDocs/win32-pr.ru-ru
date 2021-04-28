---
description: Метод конструктора Кперсистстреам. Кперсистстреам.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Конструктор Кперсистстреам. Кперсистстреам (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085612"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="471f2-103">Кперсистстреам. Кперсистстреам, конструктор</span><span class="sxs-lookup"><span data-stu-id="471f2-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="471f2-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="471f2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="471f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="471f2-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="471f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="471f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="471f2-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="471f2-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="471f2-108">Указатель на интерфейс **IUnknown** делегированного объекта.</span><span class="sxs-lookup"><span data-stu-id="471f2-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="471f2-109">*фр*</span><span class="sxs-lookup"><span data-stu-id="471f2-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="471f2-110">Указатель на общее возвращаемое значение COM.</span><span class="sxs-lookup"><span data-stu-id="471f2-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="471f2-111">Это значение изменяется только в случае сбоя этой функции.</span><span class="sxs-lookup"><span data-stu-id="471f2-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="471f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="471f2-112">Requirements</span></span>



| <span data-ttu-id="471f2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="471f2-113">Requirement</span></span> | <span data-ttu-id="471f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="471f2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471f2-115">Header</span><span class="sxs-lookup"><span data-stu-id="471f2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="471f2-116"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="471f2-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="471f2-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="471f2-117">Library</span></span><br/> | <dl> <span data-ttu-id="471f2-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="471f2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="471f2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="471f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471f2-120">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="471f2-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




