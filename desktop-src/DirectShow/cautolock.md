---
description: Класс Каутолокк содержит критическую секцию для области действия блока кода.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Класс Каутолокк (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668491"
---
# <a name="cautolock-class"></a><span data-ttu-id="b93dd-103">Класс Каутолокк</span><span class="sxs-lookup"><span data-stu-id="b93dd-103">CAutoLock class</span></span>

<span data-ttu-id="b93dd-104">`CAutoLock`Класс содержит критическую секцию для области действия блока кода.</span><span class="sxs-lookup"><span data-stu-id="b93dd-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="b93dd-105">Этот класс работает совместно с классом [**ккритсек**](ccritsec.md) , который является оболочкой для объектов критических секций.</span><span class="sxs-lookup"><span data-stu-id="b93dd-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="b93dd-106">`CAutoLock`Конструктор блокирует критическую секцию, а деструктор разблокирует его.</span><span class="sxs-lookup"><span data-stu-id="b93dd-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="b93dd-107">Используя объект в `CAutoLock` качестве локальной переменной, можно заблокировать критическую секцию с гарантией того, что все пути кода будут разблокировать критический раздел.</span><span class="sxs-lookup"><span data-stu-id="b93dd-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="b93dd-108">В следующем примере кода показано, как использовать этот класс:</span><span class="sxs-lookup"><span data-stu-id="b93dd-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="b93dd-109">Методы в этом классе не предназначены для переопределения.</span><span class="sxs-lookup"><span data-stu-id="b93dd-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="b93dd-110">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="b93dd-110">Protected Member Variables</span></span>                 | <span data-ttu-id="b93dd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b93dd-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b93dd-112">**m \_ плокк**</span><span class="sxs-lookup"><span data-stu-id="b93dd-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="b93dd-113">Критическая секция для этой блокировки.</span><span class="sxs-lookup"><span data-stu-id="b93dd-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="b93dd-114">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="b93dd-114">Public Methods</span></span>                             | <span data-ttu-id="b93dd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b93dd-115">Description</span></span>                                                      |
| [<span data-ttu-id="b93dd-116">**каутолокк**</span><span class="sxs-lookup"><span data-stu-id="b93dd-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="b93dd-117">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="b93dd-117">Constructor method.</span></span> <span data-ttu-id="b93dd-118">Блокирует указанный объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="b93dd-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="b93dd-119">**~ Каутолокк**</span><span class="sxs-lookup"><span data-stu-id="b93dd-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="b93dd-120">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="b93dd-120">Destructor method.</span></span> <span data-ttu-id="b93dd-121">Разблокирует объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="b93dd-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="b93dd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b93dd-122">Requirements</span></span>



| <span data-ttu-id="b93dd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b93dd-123">Requirement</span></span> | <span data-ttu-id="b93dd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b93dd-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b93dd-125">Header</span><span class="sxs-lookup"><span data-stu-id="b93dd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b93dd-126"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b93dd-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b93dd-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b93dd-127">Library</span></span><br/> | <dl> <span data-ttu-id="b93dd-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b93dd-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




