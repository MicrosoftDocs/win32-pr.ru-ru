---
description: Функция Филтераддобжект добавляет один объект в фильтр просмотра.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Функция Филтераддобжект (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497001"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="bfa40-103">Функция Филтераддобжект</span><span class="sxs-lookup"><span data-stu-id="bfa40-103">FilterAddObject function</span></span>

<span data-ttu-id="bfa40-104">Функция **филтераддобжект** добавляет один объект в [*Фильтр просмотра*](d.md).</span><span class="sxs-lookup"><span data-stu-id="bfa40-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfa40-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="bfa40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfa40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa40-107">*хфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfa40-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa40-108">Маркер фильтра просмотра.</span><span class="sxs-lookup"><span data-stu-id="bfa40-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="bfa40-109">*лпфилтеробжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bfa40-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa40-110">Указатель на структуру [филтеробжект](filterobject.md) , определяющую объект, добавляемый в фильтр.</span><span class="sxs-lookup"><span data-stu-id="bfa40-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="bfa40-111">Каждый объект может быть оператором, значением или свойством.</span><span class="sxs-lookup"><span data-stu-id="bfa40-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa40-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfa40-112">Return value</span></span>

<span data-ttu-id="bfa40-113">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bfa40-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bfa40-114">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="bfa40-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="bfa40-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bfa40-115">Return code</span></span>                                                                                              | <span data-ttu-id="bfa40-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bfa40-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfa40-117"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa40-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="bfa40-118">Параметр *хфилтер* имеет недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="bfa40-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="bfa40-119"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa40-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="bfa40-120">Сетевой монитор не хватает памяти для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="bfa40-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfa40-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfa40-121">Remarks</span></span>

<span data-ttu-id="bfa40-122">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **филтераддобжект** .</span><span class="sxs-lookup"><span data-stu-id="bfa40-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="bfa40-123">Функция **филтераддобжект** вызывается каждый раз при добавлении объекта фильтра в фильтр просмотра.</span><span class="sxs-lookup"><span data-stu-id="bfa40-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="bfa40-124">Фильтр просмотра является постфиксным стеком объектов, которые могут быть оператором, значением или свойством.</span><span class="sxs-lookup"><span data-stu-id="bfa40-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa40-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bfa40-125">Requirements</span></span>



| <span data-ttu-id="bfa40-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bfa40-126">Requirement</span></span> | <span data-ttu-id="bfa40-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa40-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa40-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfa40-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa40-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfa40-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bfa40-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfa40-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa40-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfa40-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfa40-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bfa40-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa40-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa40-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bfa40-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bfa40-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfa40-135"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfa40-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bfa40-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa40-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa40-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfa40-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa40-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfa40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa40-139">филтеробжект</span><span class="sxs-lookup"><span data-stu-id="bfa40-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




