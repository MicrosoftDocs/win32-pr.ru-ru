---
description: Метод WebMethod извлекает идентификатор класса (CLSID) объекта. Этот метод реализует метод IPersist::/ClassID.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Метод Ксистемклокк. ClassID (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658113"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="774ac-104">Ксистемклокк. ClassID, метод</span><span class="sxs-lookup"><span data-stu-id="774ac-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="774ac-105">`GetClassID`Метод получает идентификатор класса (CLSID) объекта.</span><span class="sxs-lookup"><span data-stu-id="774ac-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="774ac-106">Этот метод реализует метод **IPersist::/ClassID** .</span><span class="sxs-lookup"><span data-stu-id="774ac-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="774ac-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="774ac-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="774ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="774ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774ac-109">*пклсид*</span><span class="sxs-lookup"><span data-stu-id="774ac-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="774ac-110">Указатель на переменную, которая получает значение CLSID \_ системклокк.</span><span class="sxs-lookup"><span data-stu-id="774ac-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774ac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="774ac-111">Return value</span></span>

<span data-ttu-id="774ac-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="774ac-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="774ac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="774ac-113">Requirements</span></span>



| <span data-ttu-id="774ac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="774ac-114">Requirement</span></span> | <span data-ttu-id="774ac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="774ac-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774ac-116">Версия</span><span class="sxs-lookup"><span data-stu-id="774ac-116">Version</span></span><br/> | <span data-ttu-id="774ac-117">Класс Ксистемклокк</span><span class="sxs-lookup"><span data-stu-id="774ac-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="774ac-118">Header</span><span class="sxs-lookup"><span data-stu-id="774ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="774ac-119"><dt>Сисклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="774ac-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="774ac-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="774ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="774ac-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="774ac-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




