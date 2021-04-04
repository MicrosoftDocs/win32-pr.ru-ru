---
title: Функция Фрикаунтедстринг (Напутил. h)
description: Освобождает структуру данных Каунтедстринг.
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- Фрикаунтедстринг функция NAP
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f732a069d19d6b8948854bd1fe2e23be070aa23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988216"
---
# <a name="freecountedstring-function"></a><span data-ttu-id="93094-104">Функция Фрикаунтедстринг</span><span class="sxs-lookup"><span data-stu-id="93094-104">FreeCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="93094-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="93094-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="93094-106">Функция **фрикаунтедстринг** освобождает структуру данных [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="93094-106">The **FreeCountedString** function frees a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="93094-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93094-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a><span data-ttu-id="93094-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="93094-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93094-109">*каунтедстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93094-109">*countedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93094-110">Указатель на структуру данных [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="93094-110">A pointer to the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93094-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93094-111">Remarks</span></span>

<span data-ttu-id="93094-112">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="93094-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="93094-113">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="93094-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="93094-114">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="93094-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="93094-115">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="93094-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="93094-116">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="93094-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="93094-117">Требования</span><span class="sxs-lookup"><span data-stu-id="93094-117">Requirements</span></span>



| <span data-ttu-id="93094-118">Требование</span><span class="sxs-lookup"><span data-stu-id="93094-118">Requirement</span></span> | <span data-ttu-id="93094-119">Значение</span><span class="sxs-lookup"><span data-stu-id="93094-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93094-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93094-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93094-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93094-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="93094-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93094-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93094-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93094-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="93094-124">Header</span><span class="sxs-lookup"><span data-stu-id="93094-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93094-125"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="93094-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="93094-126">DLL</span><span class="sxs-lookup"><span data-stu-id="93094-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93094-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93094-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93094-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93094-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93094-129">**аллоккаунтедстринг**</span><span class="sxs-lookup"><span data-stu-id="93094-129">**AllocCountedString**</span></span>](alloccountedstring-func.md)
</dt> </dl>

 

 





