---
description: Функция Експертреаллокмемори увеличивает или уменьшает объем памяти, выделенной сетевой монитор.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Функция Експертреаллокмемори (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650482"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="ac5b2-103">Функция Експертреаллокмемори</span><span class="sxs-lookup"><span data-stu-id="ac5b2-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="ac5b2-104">Функция **експертреаллокмемори** увеличивает или уменьшает объем памяти, выделенной сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac5b2-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="ac5b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac5b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5b2-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b2-108">Уникальный идентификатор, передаваемый эксперту при [**запуске**](run.md) или [**настройке**](configure.md).</span><span class="sxs-lookup"><span data-stu-id="ac5b2-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac5b2-109">*поригиналмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b2-110">Указатель на память, выделенную сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="ac5b2-111">Указатель *поригиналмемори* может возвращаться предыдущим вызовом [**експерталлокмемори**](expertallocmemory.md) или **експертреаллокмемори**.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="ac5b2-112">*nBytes* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b2-113">Размер перераспределенной памяти.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="ac5b2-114">*perror* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b2-115">При возвращении — код ошибки, если функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="ac5b2-116">Если код ошибки НМЕРР \_ эксперта \_ , эксперт должен выполнить очистку и возвратить немедленно.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5b2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac5b2-117">Return value</span></span>

<span data-ttu-id="ac5b2-118">Если функция выполнена успешно, возвращаемое значение является указателем на выделенную память.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="ac5b2-119">Если функция завершается неудачно, возвращается значение **null**, а *perror* (если значение не **равно NULL** ) указывает причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5b2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac5b2-120">Remarks</span></span>

<span data-ttu-id="ac5b2-121">Важно отметить, что эксперт должен использовать сетевой монитор функции выделения памяти для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="ac5b2-122">Если во время выполнения эксперт не работает, использование этих функций позволит сетевой монитор освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="ac5b2-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5b2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ac5b2-123">Requirements</span></span>



| <span data-ttu-id="ac5b2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ac5b2-124">Requirement</span></span> | <span data-ttu-id="ac5b2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5b2-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5b2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac5b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5b2-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ac5b2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac5b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5b2-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac5b2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ac5b2-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ac5b2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5b2-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b2-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ac5b2-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac5b2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac5b2-133"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b2-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac5b2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5b2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5b2-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b2-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




