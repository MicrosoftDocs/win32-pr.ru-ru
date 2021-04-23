---
description: Перечисление, используемое для указания типа события.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416637"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span data-ttu-id="e5e5b-103"><span id="vspixengine.eventtype"></span>Перечисление EVENTTYPE</span><span class="sxs-lookup"><span data-stu-id="e5e5b-103"><span id="vspixengine.eventtype"></span>EVENTTYPE enumeration</span></span>

<span data-ttu-id="e5e5b-104">Перечисление, используемое для указания типа события.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-104">An enum used to indicate the type of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e5b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5e5b-105">Syntax</span></span>

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a><span data-ttu-id="e5e5b-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e5e5b-106">Constants</span></span>

<span data-ttu-id="e5e5b-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET \_ нет**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET\_NONE**</span></span>  
<span data-ttu-id="e5e5b-108">Значение, соответствующее отсутствию события.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-108">A value that corresponds to no event.</span></span>

<span data-ttu-id="e5e5b-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="e5e5b-110">Значение, соответствующее событию запуска сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-110">A value that corresponds to a session start event.</span></span>

<span data-ttu-id="e5e5b-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET \_ сессионенд**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET\_SESSIONEND**</span></span>  
<span data-ttu-id="e5e5b-112">Значение, соответствующее событию конца сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-112">A value that corresponds to a session end event.</span></span>

<span data-ttu-id="e5e5b-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET \_ процессстарт**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="e5e5b-114">Значение, соответствующее событию запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-114">A value that corresponds to a process start event.</span></span>

<span data-ttu-id="e5e5b-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET \_ процессенд**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET\_PROCESSEND**</span></span>  
<span data-ttu-id="e5e5b-116">Значение, соответствующее событию завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-116">A value that corresponds to a process end event.</span></span>

<span data-ttu-id="e5e5b-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET \_ фрамебегин**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="e5e5b-118">Значение, соответствующее событию начала кадра.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-118">A value that corresponds to a frame begin event.</span></span>

<span data-ttu-id="e5e5b-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET \_ фраминд**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET\_FRAMEEND**</span></span>  
<span data-ttu-id="e5e5b-120">Значение, соответствующее событию конца кадра.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-120">A value that corresponds to a frame end event.</span></span> <span data-ttu-id="e5e5b-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-121">Not used.</span></span>

<span data-ttu-id="e5e5b-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ усеревентбегин**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="e5e5b-123">Значение, соответствующее событию начала пользовательского события.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-123">A value that corresponds to a user-event begin event.</span></span>

<span data-ttu-id="e5e5b-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ усеревентенд**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="e5e5b-125">Значение, соответствующее событию окончания события пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-125">A value that corresponds to a user-event end event.</span></span> <span data-ttu-id="e5e5b-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-126">Not used.</span></span>

<span data-ttu-id="e5e5b-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET \_ усермаркер**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET\_USERMARKER**</span></span>  
<span data-ttu-id="e5e5b-128">Значение, соответствующее событию маркера пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-128">A value that corresponds to a user-marker event.</span></span>

<span data-ttu-id="e5e5b-129"><span id="ET_CALL"></span><span id="et_call"></span>**\_вызов et**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET\_CALL**</span></span>  
<span data-ttu-id="e5e5b-130">Значение, соответствующее событию вызова.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-130">A value that corresponds to a call event.</span></span>

<span data-ttu-id="e5e5b-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ обжекткреатион**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="e5e5b-132">Значение, соответствующее событию создания объекта.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-132">A value that corresponds to an object creation event.</span></span>

<span data-ttu-id="e5e5b-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ обжектпопулатион**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="e5e5b-134">Значение, соответствующее событию заполнения объекта.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-134">A value that corresponds to an object population event.</span></span>

<span data-ttu-id="e5e5b-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ каллсинк**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET\_CALLSYNC**</span></span>  

<span data-ttu-id="e5e5b-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**\_Рисование et**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET\_DRAW**</span></span>  
<span data-ttu-id="e5e5b-137">Значение, соответствующее событию вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-137">A value that corresponds to a draw call event.</span></span>

<span data-ttu-id="e5e5b-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**\_Диспетчер et**</span><span class="sxs-lookup"><span data-stu-id="e5e5b-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET\_DISPATCH**</span></span>  
<span data-ttu-id="e5e5b-139">Значение, соответствующее событию диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-139">A value that corresponds to a dispatch event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e5b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e5e5b-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e5e5b-141">Header</span><span class="sxs-lookup"><span data-stu-id="e5e5b-141">Header</span></span></p></td><td><span data-ttu-id="e5e5b-142">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="e5e5b-142">Vspixengine.h</span></span></td></tr></tbody></table>
