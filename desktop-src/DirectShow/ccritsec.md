---
description: Класс Ккритсек обеспечивает блокировку потока.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Класс Ккритсек (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675306"
---
# <a name="ccritsec-class"></a><span data-ttu-id="094c1-103">Класс Ккритсек</span><span class="sxs-lookup"><span data-stu-id="094c1-103">CCritSec class</span></span>

<span data-ttu-id="094c1-104">Класс **ккритсек** обеспечивает блокировку потока.</span><span class="sxs-lookup"><span data-stu-id="094c1-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="094c1-105">Этот класс является тонкой оболочкой для объекта **критического \_ раздела** Windows.</span><span class="sxs-lookup"><span data-stu-id="094c1-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="094c1-106">Вы можете заблокировать и разблокировать поток, вызвав методы [**ккритсек:: Lock**](ccritsec-lock.md) и [**Ккритсек:: Unlock**](ccritsec-unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="094c1-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="094c1-107">Однако безопаснее использовать этот класс в сочетании с классом [**каутолокк**](cautolock.md) .</span><span class="sxs-lookup"><span data-stu-id="094c1-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="094c1-108">Когда класс **каутолокк** выходит из области действия, он автоматически разблокирует объект **ккритсек** .</span><span class="sxs-lookup"><span data-stu-id="094c1-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="094c1-109">Более того, он компилируется в эффективный встроенный код.</span><span class="sxs-lookup"><span data-stu-id="094c1-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="094c1-110">Открытые переменные члена</span><span class="sxs-lookup"><span data-stu-id="094c1-110">Public Member Variables</span></span>                            | <span data-ttu-id="094c1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="094c1-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="094c1-112">**m \_ куррентовнер**</span><span class="sxs-lookup"><span data-stu-id="094c1-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="094c1-113">Идентификатор потока владеющего потока.</span><span class="sxs-lookup"><span data-stu-id="094c1-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="094c1-114">**m \_ локккаунт**</span><span class="sxs-lookup"><span data-stu-id="094c1-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="094c1-115">Количество невыполненных блокировок для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="094c1-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="094c1-116">**m \_ фтраце**</span><span class="sxs-lookup"><span data-stu-id="094c1-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="094c1-117">Логическое значение, указывающее, следует ли отслеживать эту блокировку.</span><span class="sxs-lookup"><span data-stu-id="094c1-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="094c1-118">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="094c1-118">Public Methods</span></span>                                     | <span data-ttu-id="094c1-119">Описание</span><span class="sxs-lookup"><span data-stu-id="094c1-119">Description</span></span>                                              |
| [<span data-ttu-id="094c1-120">**ккритсек**</span><span class="sxs-lookup"><span data-stu-id="094c1-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="094c1-121">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="094c1-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="094c1-122">**~ Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="094c1-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="094c1-123">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="094c1-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="094c1-124">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="094c1-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="094c1-125">Блокирует объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="094c1-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="094c1-126">**Блокирован**</span><span class="sxs-lookup"><span data-stu-id="094c1-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="094c1-127">Разблокирует объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="094c1-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="094c1-128">Требования</span><span class="sxs-lookup"><span data-stu-id="094c1-128">Requirements</span></span>



| <span data-ttu-id="094c1-129">Требование</span><span class="sxs-lookup"><span data-stu-id="094c1-129">Requirement</span></span> | <span data-ttu-id="094c1-130">Значение</span><span class="sxs-lookup"><span data-stu-id="094c1-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094c1-131">Header</span><span class="sxs-lookup"><span data-stu-id="094c1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="094c1-132"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="094c1-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="094c1-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="094c1-133">Library</span></span><br/> | <dl> <span data-ttu-id="094c1-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="094c1-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094c1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="094c1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094c1-136">Объекты критических секций</span><span class="sxs-lookup"><span data-stu-id="094c1-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="094c1-137">Справочник по базовому классу DirectShow</span><span class="sxs-lookup"><span data-stu-id="094c1-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

