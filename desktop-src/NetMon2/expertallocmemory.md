---
description: Функция Експерталлокмемори выделяет память для эксперта.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Функция Експерталлокмемори (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808729"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="16cfa-103">Функция Експерталлокмемори</span><span class="sxs-lookup"><span data-stu-id="16cfa-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="16cfa-104">Функция **експерталлокмемори** выделяет память для эксперта.</span><span class="sxs-lookup"><span data-stu-id="16cfa-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cfa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16cfa-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="16cfa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16cfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16cfa-107">*хексперткэй*</span><span class="sxs-lookup"><span data-stu-id="16cfa-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="16cfa-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="16cfa-108">Unique expert identifier.</span></span> <span data-ttu-id="16cfa-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="16cfa-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="16cfa-110">*nBytes* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16cfa-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cfa-111">Выделенная память, измеряемая в байтах.</span><span class="sxs-lookup"><span data-stu-id="16cfa-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="16cfa-112">*perror* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16cfa-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16cfa-113">Индикатор ошибки.</span><span class="sxs-lookup"><span data-stu-id="16cfa-113">Error indicator.</span></span> <span data-ttu-id="16cfa-114">Если функция завершается ошибкой, параметр *nBytes* содержит код ошибки.</span><span class="sxs-lookup"><span data-stu-id="16cfa-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="16cfa-115">Если код ошибки НМЕРР \_ эксперта \_ , эксперт должен выполнить очистку и возвратить сообщение немедленно.</span><span class="sxs-lookup"><span data-stu-id="16cfa-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16cfa-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16cfa-116">Return value</span></span>

<span data-ttu-id="16cfa-117">Если функция выполнена успешно, возвращаемое значение является указателем на выделенную память.</span><span class="sxs-lookup"><span data-stu-id="16cfa-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="16cfa-118">Если функция завершается неудачно, возвращается значение **null**, а *perror* — код ошибки, указывающий причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="16cfa-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="16cfa-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16cfa-119">Remarks</span></span>

<span data-ttu-id="16cfa-120">Важно отметить, что эксперт должен использовать функции выделения памяти сетевой монитор (включая [експертреаллокмемори](expertreallocmemory.md)) для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="16cfa-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="16cfa-121">Если во время выполнения эксперт не работает, использование этих функций позволит сетевой монитор освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="16cfa-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="16cfa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="16cfa-122">Requirements</span></span>



| <span data-ttu-id="16cfa-123">Требование</span><span class="sxs-lookup"><span data-stu-id="16cfa-123">Requirement</span></span> | <span data-ttu-id="16cfa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="16cfa-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16cfa-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16cfa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="16cfa-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16cfa-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="16cfa-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16cfa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="16cfa-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16cfa-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="16cfa-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="16cfa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="16cfa-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="16cfa-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="16cfa-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16cfa-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="16cfa-132"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16cfa-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="16cfa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="16cfa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16cfa-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16cfa-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




