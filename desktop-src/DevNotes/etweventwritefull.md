---
description: Записывает полное событие в сеанс.
title: етвевентвритефулл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990678"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="d17bf-103">Функция Етвевентвритефулл</span><span class="sxs-lookup"><span data-stu-id="d17bf-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="d17bf-104">[Функция Етвевентвритефулл и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут быть изменены с одного выпуска Windows на другой.]</span><span class="sxs-lookup"><span data-stu-id="d17bf-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="d17bf-105">Записывает полное событие в сеанс.</span><span class="sxs-lookup"><span data-stu-id="d17bf-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17bf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d17bf-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="d17bf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d17bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17bf-108">*регхандле*</span><span class="sxs-lookup"><span data-stu-id="d17bf-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-109">Регхандле для поставщика.</span><span class="sxs-lookup"><span data-stu-id="d17bf-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="d17bf-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="d17bf-111">Дескриптор события для записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="d17bf-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="d17bf-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-113">Флаг, заданный пользователем.</span><span class="sxs-lookup"><span data-stu-id="d17bf-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="d17bf-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-115">Идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="d17bf-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="d17bf-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-117">Идентификатор связанного действия.</span><span class="sxs-lookup"><span data-stu-id="d17bf-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-118">*усердатакаунт*</span><span class="sxs-lookup"><span data-stu-id="d17bf-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-119">Число элементов данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d17bf-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="d17bf-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="d17bf-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="d17bf-121">Указатель на массив элементов данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d17bf-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17bf-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d17bf-122">Return value</span></span>

<span data-ttu-id="d17bf-123">Код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="d17bf-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d17bf-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d17bf-124">Remarks</span></span>

<span data-ttu-id="d17bf-125">Функция Етвевентвритефулл и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому.</span><span class="sxs-lookup"><span data-stu-id="d17bf-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="d17bf-126">Чтобы обеспечить совместимость приложения, лучше использовать открытые функции.</span><span class="sxs-lookup"><span data-stu-id="d17bf-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="d17bf-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d17bf-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d17bf-128">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="d17bf-128">**Target Platform**</span></span> | <span data-ttu-id="d17bf-129">Windows</span><span class="sxs-lookup"><span data-stu-id="d17bf-129">Windows</span></span> |
| <span data-ttu-id="d17bf-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="d17bf-130">**Header**</span></span> | <span data-ttu-id="d17bf-131">нтетв. h</span><span class="sxs-lookup"><span data-stu-id="d17bf-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="d17bf-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d17bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17bf-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="d17bf-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="d17bf-134">евентвритикс</span><span class="sxs-lookup"><span data-stu-id="d17bf-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
