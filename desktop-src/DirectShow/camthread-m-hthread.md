---
description: Обработчик для потока.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Элемент Камсреад:: m_hThread (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689462"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="c270c-103">Элемент Камсреад:: m \_ хсреад</span><span class="sxs-lookup"><span data-stu-id="c270c-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="c270c-104">Обработчик для потока.</span><span class="sxs-lookup"><span data-stu-id="c270c-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c270c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c270c-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="c270c-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="c270c-106">Remarks</span></span>

<span data-ttu-id="c270c-107">Эта переменная инициализируется как **null**.</span><span class="sxs-lookup"><span data-stu-id="c270c-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="c270c-108">Метод [**камсреад:: Create**](camthread-create.md) присваивает этой переменной значение обработчика потока.</span><span class="sxs-lookup"><span data-stu-id="c270c-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="c270c-109">Чтобы определить, существует ли поток, вызовите метод [**камсреад:: среадексистс**](camthread-threadexists.md) .</span><span class="sxs-lookup"><span data-stu-id="c270c-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c270c-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c270c-110">Requirements</span></span>



| <span data-ttu-id="c270c-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c270c-111">Requirement</span></span> | <span data-ttu-id="c270c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c270c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c270c-113">Header</span><span class="sxs-lookup"><span data-stu-id="c270c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c270c-114"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c270c-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c270c-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c270c-115">Library</span></span><br/> | <dl> <span data-ttu-id="c270c-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c270c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c270c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c270c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c270c-118">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="c270c-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




