---
description: Пример очереди носителя.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Элемент Каутпуткуеуе:: m_List (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675534"
---
# <a name="coutputqueuem_list-member"></a><span data-ttu-id="cf11d-103">Элемент списка Каутпуткуеуе:: m \_</span><span class="sxs-lookup"><span data-stu-id="cf11d-103">COutputQueue::m\_List member</span></span>

<span data-ttu-id="cf11d-104">Пример очереди носителя.</span><span class="sxs-lookup"><span data-stu-id="cf11d-104">Media sample queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf11d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf11d-105">Syntax</span></span>


```C++
CSampleList *m_List;
```



## <a name="remarks"></a><span data-ttu-id="cf11d-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf11d-106">Remarks</span></span>

<span data-ttu-id="cf11d-107">Эта переменная-член является указателем на объект [**кженериклист**](cgenericlist.md) , содержащий указатели [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="cf11d-107">This member variable is a pointer to a [**CGenericList**](cgenericlist.md) object that holds [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers.</span></span> <span data-ttu-id="cf11d-108">Тип **ксамплелист** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf11d-108">The **CSampleList** type is defined as follows:</span></span>

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a><span data-ttu-id="cf11d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cf11d-109">Requirements</span></span>



| <span data-ttu-id="cf11d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cf11d-110">Requirement</span></span> | <span data-ttu-id="cf11d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cf11d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf11d-112">Header</span><span class="sxs-lookup"><span data-stu-id="cf11d-112">Header</span></span><br/>  | <dl> <span data-ttu-id="cf11d-113"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf11d-113"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf11d-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf11d-114">Library</span></span><br/> | <dl> <span data-ttu-id="cf11d-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cf11d-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf11d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf11d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf11d-117">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="cf11d-117">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




