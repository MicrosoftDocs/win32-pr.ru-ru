---
title: Функция Фрификсупинфо (Напутил. h)
description: Освобождает структуру данных Фиксупинфо.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Фрификсупинфо функция NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672796"
---
# <a name="freefixupinfo-function"></a><span data-ttu-id="805a6-104">Функция Фрификсупинфо</span><span class="sxs-lookup"><span data-stu-id="805a6-104">FreeFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="805a6-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="805a6-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="805a6-106">Функция **фрификсупинфо** освобождает структуру данных [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .</span><span class="sxs-lookup"><span data-stu-id="805a6-106">The **FreeFixupInfo** function frees a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="805a6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="805a6-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="805a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="805a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805a6-109">*фиксупинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="805a6-109">*fixupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805a6-110">Указатель на структуру данных [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="805a6-110">A pointer to the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="805a6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="805a6-111">Remarks</span></span>

<span data-ttu-id="805a6-112">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="805a6-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="805a6-113">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="805a6-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="805a6-114">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="805a6-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="805a6-115">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="805a6-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="805a6-116">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="805a6-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="805a6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="805a6-117">Requirements</span></span>



| <span data-ttu-id="805a6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="805a6-118">Requirement</span></span> | <span data-ttu-id="805a6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="805a6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="805a6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="805a6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="805a6-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="805a6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="805a6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="805a6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="805a6-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="805a6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="805a6-124">Header</span><span class="sxs-lookup"><span data-stu-id="805a6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="805a6-125"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="805a6-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="805a6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="805a6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805a6-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805a6-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805a6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="805a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805a6-129">**аллокфиксупинфо**</span><span class="sxs-lookup"><span data-stu-id="805a6-129">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
</dt> </dl>

 

 





