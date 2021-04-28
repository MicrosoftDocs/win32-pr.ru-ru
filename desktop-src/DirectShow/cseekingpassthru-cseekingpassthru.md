---
description: Метод конструктора Ксикингпасссру. Ксикингпасссру.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Конструктор Ксикингпасссру. Ксикингпасссру (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085382"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="d98fe-103">Ксикингпасссру. Ксикингпасссру, конструктор</span><span class="sxs-lookup"><span data-stu-id="d98fe-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="d98fe-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d98fe-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d98fe-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d98fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d98fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98fe-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d98fe-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d98fe-108">Строка, содержащая имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d98fe-108">String containing the name of the object.</span></span> <span data-ttu-id="d98fe-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d98fe-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="d98fe-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d98fe-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d98fe-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d98fe-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d98fe-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="d98fe-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d98fe-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d98fe-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d98fe-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="d98fe-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d98fe-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d98fe-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d98fe-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="d98fe-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d98fe-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d98fe-117">Requirements</span></span>



| <span data-ttu-id="d98fe-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d98fe-118">Requirement</span></span> | <span data-ttu-id="d98fe-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d98fe-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98fe-120">Header</span><span class="sxs-lookup"><span data-stu-id="d98fe-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d98fe-121"><dt>Сикпт. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d98fe-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d98fe-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d98fe-122">Library</span></span><br/> | <dl> <span data-ttu-id="d98fe-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d98fe-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98fe-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d98fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98fe-125">**Класс Ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="d98fe-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




