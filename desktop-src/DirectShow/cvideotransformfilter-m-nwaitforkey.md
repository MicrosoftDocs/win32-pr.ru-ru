---
description: Текущее максимальное число удаляемых разностных кадров.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Элемент Квидеотрансформфилтер:: m_nWaitForKey (Втранс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674850"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="f44f8-103">Элемент Квидеотрансформфилтер:: m \_ нваитфоркэй</span><span class="sxs-lookup"><span data-stu-id="f44f8-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="f44f8-104">Текущее максимальное число удаляемых разностных кадров.</span><span class="sxs-lookup"><span data-stu-id="f44f8-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="f44f8-105">Хотя эта переменная больше нуля, фильтр будет удалять кадры до тех пор, пока не достигнет ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="f44f8-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="f44f8-106">Для каждого удаляемого кадра фильтр уменьшает значение этой переменной на единицу, что предотвращает удаление фильтром чрезмерного количества кадров.</span><span class="sxs-lookup"><span data-stu-id="f44f8-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="f44f8-107">После 30 Дельта-кадров в строке без ключевых кадров фильтр начнет доставлять кадры снова.</span><span class="sxs-lookup"><span data-stu-id="f44f8-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f44f8-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="f44f8-109">Требования</span><span class="sxs-lookup"><span data-stu-id="f44f8-109">Requirements</span></span>



| <span data-ttu-id="f44f8-110">Требование</span><span class="sxs-lookup"><span data-stu-id="f44f8-110">Requirement</span></span> | <span data-ttu-id="f44f8-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f44f8-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44f8-112">Header</span><span class="sxs-lookup"><span data-stu-id="f44f8-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f44f8-113"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f44f8-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f44f8-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f44f8-114">Library</span></span><br/> | <dl> <span data-ttu-id="f44f8-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f44f8-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44f8-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f44f8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44f8-117">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="f44f8-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




