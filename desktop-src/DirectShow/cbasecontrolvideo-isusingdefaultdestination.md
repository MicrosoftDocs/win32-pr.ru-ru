---
description: Метод Исусингдефаултдестинатион определяет, использует ли модуль подготовки отчетов окно назначения по умолчанию.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Кбасеконтролвидео. Исусингдефаултдестинатион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668931"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a><span data-ttu-id="2bfd2-103">Кбасеконтролвидео. Исусингдефаултдестинатион, метод</span><span class="sxs-lookup"><span data-stu-id="2bfd2-103">CBaseControlVideo.IsUsingDefaultDestination method</span></span>

<span data-ttu-id="2bfd2-104">`IsUsingDefaultDestination`Метод определяет, использует ли модуль подготовки отчетов окно назначения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-104">The `IsUsingDefaultDestination` method determines if the renderer is using the default destination window.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bfd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bfd2-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a><span data-ttu-id="2bfd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bfd2-106">Parameters</span></span>

<span data-ttu-id="2bfd2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bfd2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bfd2-108">Return value</span></span>

<span data-ttu-id="2bfd2-109">\_При использовании назначения по умолчанию возвращает значение s ОК; в противном случае возвращает \_ false.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-109">Returns S\_OK if using the default destination; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bfd2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2bfd2-110">Requirements</span></span>



| <span data-ttu-id="2bfd2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2bfd2-111">Requirement</span></span> | <span data-ttu-id="2bfd2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2bfd2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfd2-113">Header</span><span class="sxs-lookup"><span data-stu-id="2bfd2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2bfd2-114"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bfd2-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2bfd2-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2bfd2-115">Library</span></span><br/> | <dl> <span data-ttu-id="2bfd2-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2bfd2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bfd2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bfd2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bfd2-118">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="2bfd2-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




