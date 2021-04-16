---
description: Метод Исусингдефаултсаурце определяет, использует ли модуль подготовки отчетов окно источника по умолчанию.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Кбасеконтролвидео. Исусингдефаултсаурце, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658093"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="487a9-103">Кбасеконтролвидео. Исусингдефаултсаурце, метод</span><span class="sxs-lookup"><span data-stu-id="487a9-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="487a9-104">`IsUsingDefaultSource`Метод определяет, использует ли модуль подготовки отчетов окно источника по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="487a9-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="487a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="487a9-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="487a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="487a9-106">Parameters</span></span>

<span data-ttu-id="487a9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="487a9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="487a9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="487a9-108">Return value</span></span>

<span data-ttu-id="487a9-109">Возвращает \_ ОК, если модуль подготовки отчетов использует источник по умолчанию; в противном случае возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="487a9-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="487a9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="487a9-110">Requirements</span></span>



| <span data-ttu-id="487a9-111">Требование</span><span class="sxs-lookup"><span data-stu-id="487a9-111">Requirement</span></span> | <span data-ttu-id="487a9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="487a9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487a9-113">Header</span><span class="sxs-lookup"><span data-stu-id="487a9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="487a9-114"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="487a9-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="487a9-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="487a9-115">Library</span></span><br/> | <dl> <span data-ttu-id="487a9-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="487a9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487a9-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="487a9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487a9-118">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="487a9-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




