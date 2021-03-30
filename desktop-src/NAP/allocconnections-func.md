---
title: Функция Аллокконнектионс (Напутил. h)
description: Выделяет память для указанного числа структур соединений.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Аллокконнектионс функция NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804073"
---
# <a name="allocconnections-function"></a><span data-ttu-id="764d4-104">Функция Аллокконнектионс</span><span class="sxs-lookup"><span data-stu-id="764d4-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="764d4-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="764d4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="764d4-106">Функция **аллокконнектионс** выделяет память для указанного числа структур [**соединений**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="764d4-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="764d4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="764d4-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="764d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="764d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764d4-109">*подключения* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="764d4-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="764d4-110">Указатель на массив вновь выделенных структур [**соединений**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="764d4-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="764d4-111">*коннектионскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="764d4-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764d4-112">Число структур, выделяемых для *соединений*.</span><span class="sxs-lookup"><span data-stu-id="764d4-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764d4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="764d4-113">Return value</span></span>



| <span data-ttu-id="764d4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="764d4-114">Return code</span></span>                                                                                   | <span data-ttu-id="764d4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="764d4-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="764d4-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="764d4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="764d4-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="764d4-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="764d4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="764d4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="764d4-119">Передан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="764d4-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="764d4-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="764d4-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="764d4-121">В системе исчерпана виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="764d4-121">The system is out of virtual memory.</span></span> <span data-ttu-id="764d4-122">Не удалось выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="764d4-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="764d4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="764d4-123">Remarks</span></span>

<span data-ttu-id="764d4-124">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="764d4-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="764d4-125">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="764d4-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="764d4-126">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="764d4-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="764d4-127">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="764d4-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="764d4-128">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="764d4-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="764d4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="764d4-129">Requirements</span></span>



| <span data-ttu-id="764d4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="764d4-130">Requirement</span></span> | <span data-ttu-id="764d4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="764d4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="764d4-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="764d4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="764d4-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="764d4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="764d4-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="764d4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="764d4-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="764d4-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="764d4-136">Header</span><span class="sxs-lookup"><span data-stu-id="764d4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="764d4-137"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="764d4-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="764d4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="764d4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="764d4-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="764d4-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="764d4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="764d4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764d4-141">**фриконнектионс**</span><span class="sxs-lookup"><span data-stu-id="764d4-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





