---
description: Метод Крендереринпутпин является методом-конструктором.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Конструктор Крендереринпутпин. Крендереринпутпин (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669375"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="4daa0-103">Крендереринпутпин. Крендереринпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="4daa0-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="4daa0-104">`CRendererInputPin`Метод является методом-конструктором.</span><span class="sxs-lookup"><span data-stu-id="4daa0-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4daa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4daa0-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="4daa0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4daa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4daa0-107">*прендерер*</span><span class="sxs-lookup"><span data-stu-id="4daa0-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="4daa0-108">Указатель на объект [**кбасерендерер**](cbaserenderer.md) , реализующий фильтр.</span><span class="sxs-lookup"><span data-stu-id="4daa0-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="4daa0-109">*фр*</span><span class="sxs-lookup"><span data-stu-id="4daa0-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="4daa0-110">Указатель на переменную, которая получает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4daa0-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="4daa0-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="4daa0-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="4daa0-112">Указатель на строку расширенных символов, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4daa0-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4daa0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4daa0-113">Requirements</span></span>



| <span data-ttu-id="4daa0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4daa0-114">Requirement</span></span> | <span data-ttu-id="4daa0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4daa0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4daa0-116">Header</span><span class="sxs-lookup"><span data-stu-id="4daa0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4daa0-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4daa0-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4daa0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4daa0-118">Library</span></span><br/> | <dl> <span data-ttu-id="4daa0-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4daa0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4daa0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4daa0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4daa0-121">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="4daa0-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




