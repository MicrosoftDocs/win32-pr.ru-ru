---
description: Метод конструктора.
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
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665143"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="723a1-103">Ксикингпасссру. Ксикингпасссру, конструктор</span><span class="sxs-lookup"><span data-stu-id="723a1-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="723a1-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="723a1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="723a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="723a1-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="723a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="723a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723a1-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="723a1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="723a1-108">Строка, содержащая имя объекта.</span><span class="sxs-lookup"><span data-stu-id="723a1-108">String containing the name of the object.</span></span> <span data-ttu-id="723a1-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="723a1-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="723a1-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="723a1-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="723a1-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="723a1-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="723a1-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="723a1-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="723a1-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="723a1-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="723a1-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="723a1-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="723a1-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="723a1-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="723a1-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="723a1-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="723a1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="723a1-117">Requirements</span></span>



| <span data-ttu-id="723a1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="723a1-118">Requirement</span></span> | <span data-ttu-id="723a1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="723a1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723a1-120">Header</span><span class="sxs-lookup"><span data-stu-id="723a1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="723a1-121"><dt>Сикпт. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="723a1-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="723a1-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="723a1-122">Library</span></span><br/> | <dl> <span data-ttu-id="723a1-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="723a1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723a1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="723a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723a1-125">**Класс Ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="723a1-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




