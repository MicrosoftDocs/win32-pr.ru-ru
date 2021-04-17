---
description: Задает часть FOURCC объекта Фаурккмап.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Метод Фаурккмап:: Сетфауркк (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689001"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="0f24b-103">Метод Фаурккмап:: Сетфауркк</span><span class="sxs-lookup"><span data-stu-id="0f24b-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="0f24b-104">Задает часть **FourCC** объекта [**фаурккмап**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="0f24b-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f24b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f24b-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="0f24b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f24b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f24b-107">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="0f24b-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="0f24b-108">Указатель на возвращенный глобальный уникальный идентификатор (**GUID**) объекта **фаурккмап** .</span><span class="sxs-lookup"><span data-stu-id="0f24b-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f24b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f24b-109">Return value</span></span>

<span data-ttu-id="0f24b-110">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0f24b-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f24b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0f24b-111">Requirements</span></span>



| <span data-ttu-id="0f24b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0f24b-112">Requirement</span></span> | <span data-ttu-id="0f24b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0f24b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f24b-114">Header</span><span class="sxs-lookup"><span data-stu-id="0f24b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0f24b-115"><dt>FourCC. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f24b-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0f24b-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f24b-116">Library</span></span><br/> | <dl> <span data-ttu-id="0f24b-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0f24b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f24b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f24b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f24b-119">**Класс Фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="0f24b-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




