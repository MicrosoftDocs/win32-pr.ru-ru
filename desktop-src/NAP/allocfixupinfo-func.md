---
title: Функция Аллокфиксупинфо (Напутил. h)
description: Выделяет память для структуры Фиксупинфо указанного размера.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Аллокфиксупинфо функция NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891537"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="7bb8e-104">Функция Аллокфиксупинфо</span><span class="sxs-lookup"><span data-stu-id="7bb8e-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="7bb8e-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7bb8e-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7bb8e-106">Функция **аллокфиксупинфо** выделяет память для структуры [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) указанного размера.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bb8e-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="7bb8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bb8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb8e-109">*фиксупинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7bb8e-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb8e-110">Указатель на адрес вновь выделенной структуры [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .</span><span class="sxs-lookup"><span data-stu-id="7bb8e-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7bb8e-111">*каунтресулткодес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7bb8e-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb8e-112">Число кодов результата для выделения в *фиксупинфо*.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb8e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bb8e-113">Return value</span></span>



| <span data-ttu-id="7bb8e-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7bb8e-114">Return code</span></span>                                                                                   | <span data-ttu-id="7bb8e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7bb8e-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bb8e-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7bb8e-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="7bb8e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7bb8e-119">Передан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7bb8e-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7bb8e-121">В системе исчерпана виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-121">The system is out of virtual memory.</span></span> <span data-ttu-id="7bb8e-122">Не удалось выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7bb8e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bb8e-123">Remarks</span></span>

<span data-ttu-id="7bb8e-124">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="7bb8e-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7bb8e-125">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7bb8e-126">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7bb8e-127">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7bb8e-128">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="7bb8e-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb8e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7bb8e-129">Requirements</span></span>



| <span data-ttu-id="7bb8e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7bb8e-130">Requirement</span></span> | <span data-ttu-id="7bb8e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7bb8e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb8e-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bb8e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb8e-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7bb8e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7bb8e-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bb8e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb8e-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7bb8e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7bb8e-136">Header</span><span class="sxs-lookup"><span data-stu-id="7bb8e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb8e-137"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8e-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7bb8e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb8e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb8e-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8e-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb8e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bb8e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb8e-141">**фрификсупинфо**</span><span class="sxs-lookup"><span data-stu-id="7bb8e-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





