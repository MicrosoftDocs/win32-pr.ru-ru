---
description: Возвращает идентификатор класса для этого фильтра.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Метод Кперсистстреам. ClassID (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675690"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="98c07-103">Кперсистстреам. ClassID, метод</span><span class="sxs-lookup"><span data-stu-id="98c07-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="98c07-104">Возвращает идентификатор класса для этого фильтра.</span><span class="sxs-lookup"><span data-stu-id="98c07-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98c07-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="98c07-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c07-107">*пклсид*</span><span class="sxs-lookup"><span data-stu-id="98c07-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="98c07-108">Указатель на структуру CLSID.</span><span class="sxs-lookup"><span data-stu-id="98c07-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="98c07-109">Скопируйте идентификатор класса здесь.</span><span class="sxs-lookup"><span data-stu-id="98c07-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c07-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98c07-110">Return value</span></span>

<span data-ttu-id="98c07-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98c07-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c07-112">Требования</span><span class="sxs-lookup"><span data-stu-id="98c07-112">Requirements</span></span>



| <span data-ttu-id="98c07-113">Требование</span><span class="sxs-lookup"><span data-stu-id="98c07-113">Requirement</span></span> | <span data-ttu-id="98c07-114">Значение</span><span class="sxs-lookup"><span data-stu-id="98c07-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c07-115">Header</span><span class="sxs-lookup"><span data-stu-id="98c07-115">Header</span></span><br/>  | <dl> <span data-ttu-id="98c07-116"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c07-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98c07-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98c07-117">Library</span></span><br/> | <dl> <span data-ttu-id="98c07-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="98c07-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c07-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98c07-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c07-120">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="98c07-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




