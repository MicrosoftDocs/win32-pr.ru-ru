---
description: Метод конструктора.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Конструктор Крендерерпоспасссру. Крендерерпоспасссру (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668979"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="d4a0b-103">Крендерерпоспасссру. Крендерерпоспасссру, конструктор</span><span class="sxs-lookup"><span data-stu-id="d4a0b-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="d4a0b-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4a0b-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d4a0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a0b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d4a0b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a0b-108">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="d4a0b-109">Выделите этот параметр в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="d4a0b-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d4a0b-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a0b-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d4a0b-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d4a0b-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4a0b-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="d4a0b-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a0b-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4a0b-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d4a0b-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d4a0b-117">*ппин*</span><span class="sxs-lookup"><span data-stu-id="d4a0b-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a0b-118">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4a0b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d4a0b-119">Requirements</span></span>



| <span data-ttu-id="d4a0b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d4a0b-120">Requirement</span></span> | <span data-ttu-id="d4a0b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d4a0b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a0b-122">Header</span><span class="sxs-lookup"><span data-stu-id="d4a0b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4a0b-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a0b-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4a0b-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4a0b-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4a0b-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a0b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




