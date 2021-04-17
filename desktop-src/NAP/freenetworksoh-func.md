---
title: Функция Фринетворксох (Напутил. h)
description: Освобождает структуру данных Нетворксох.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- Фринетворксох функция NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea2b72011332939aa0c814203d0004949c8341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492345"
---
# <a name="freenetworksoh-function"></a><span data-ttu-id="cf7c1-104">Функция Фринетворксох</span><span class="sxs-lookup"><span data-stu-id="cf7c1-104">FreeNetworkSoH function</span></span>

> [!Note]  
> <span data-ttu-id="cf7c1-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="cf7c1-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cf7c1-106">Функция **фринетворксох** освобождает структуру данных [**нетворксох**](/windows/win32/api/naptypes/ns-naptypes-networksoh) .</span><span class="sxs-lookup"><span data-stu-id="cf7c1-106">The **FreeNetworkSoH** function frees a [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7c1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf7c1-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a><span data-ttu-id="cf7c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf7c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7c1-109">*нетворксох* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf7c1-109">*networkSoh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7c1-110">Указатель на структуру данных [**нетворксох**](/windows/win32/api/naptypes/ns-naptypes-networksoh) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="cf7c1-110">A pointer to the [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf7c1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf7c1-111">Remarks</span></span>

<span data-ttu-id="cf7c1-112">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="cf7c1-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="cf7c1-113">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="cf7c1-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="cf7c1-114">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="cf7c1-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="cf7c1-115">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="cf7c1-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="cf7c1-116">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="cf7c1-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7c1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cf7c1-117">Requirements</span></span>



| <span data-ttu-id="cf7c1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cf7c1-118">Requirement</span></span> | <span data-ttu-id="cf7c1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cf7c1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7c1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf7c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf7c1-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf7c1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cf7c1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf7c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf7c1-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf7c1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf7c1-124">Header</span><span class="sxs-lookup"><span data-stu-id="cf7c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf7c1-125"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c1-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="cf7c1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cf7c1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf7c1-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c1-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





