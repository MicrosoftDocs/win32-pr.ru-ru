---
description: Извлекает объект FOURCC&\# 160; DWORD из объекта фаурккмап.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'Метод Фаурккмап:: Жетфауркк (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651715"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="2d0e6-103">Метод Фаурккмап:: Жетфауркк</span><span class="sxs-lookup"><span data-stu-id="2d0e6-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="2d0e6-104">Извлекает DWORD **FourCC**  из объекта [**фаурккмап**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0e6-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d0e6-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="2d0e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d0e6-106">Parameters</span></span>

<span data-ttu-id="2d0e6-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2d0e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d0e6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d0e6-108">Return value</span></span>

<span data-ttu-id="2d0e6-109">Возвращает значение  **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2d0e6-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="2d0e6-110">Обратите внимание, что при создании **идентификатора GUID** , который изначально не был производным от **FourCC**, возвращаемое значение будет фактически случайным.</span><span class="sxs-lookup"><span data-stu-id="2d0e6-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d0e6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2d0e6-111">Requirements</span></span>



| <span data-ttu-id="2d0e6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2d0e6-112">Requirement</span></span> | <span data-ttu-id="2d0e6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2d0e6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0e6-114">Header</span><span class="sxs-lookup"><span data-stu-id="2d0e6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2d0e6-115"><dt>FourCC. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e6-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2d0e6-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d0e6-116">Library</span></span><br/> | <dl> <span data-ttu-id="2d0e6-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d0e6-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d0e6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0e6-119">**Класс Фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="2d0e6-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




