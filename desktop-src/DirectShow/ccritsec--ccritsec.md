---
description: Метод деструктора.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Деструктор Ккритсек. ~ Ккритсек (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676067"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="748f7-103">Деструктор Ккритсек. ~ Ккритсек</span><span class="sxs-lookup"><span data-stu-id="748f7-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="748f7-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="748f7-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="748f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="748f7-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="748f7-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="748f7-106">Remarks</span></span>

<span data-ttu-id="748f7-107">Этот метод вызывает функцию [**делетекритикалсектион**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) для удаления критической секции.</span><span class="sxs-lookup"><span data-stu-id="748f7-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="748f7-108">Требования</span><span class="sxs-lookup"><span data-stu-id="748f7-108">Requirements</span></span>



| <span data-ttu-id="748f7-109">Требование</span><span class="sxs-lookup"><span data-stu-id="748f7-109">Requirement</span></span> | <span data-ttu-id="748f7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="748f7-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="748f7-111">Header</span><span class="sxs-lookup"><span data-stu-id="748f7-111">Header</span></span><br/>  | <dl> <span data-ttu-id="748f7-112"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="748f7-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="748f7-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="748f7-113">Library</span></span><br/> | <dl> <span data-ttu-id="748f7-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="748f7-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748f7-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="748f7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748f7-116">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="748f7-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

