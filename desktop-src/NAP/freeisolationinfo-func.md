---
title: Функция Фриисолатионинфо (Напутил. h)
description: Освобождает структуру данных Исолатионинфо.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- Фриисолатионинфо функция NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672795"
---
# <a name="freeisolationinfo-function"></a><span data-ttu-id="7b095-104">Функция Фриисолатионинфо</span><span class="sxs-lookup"><span data-stu-id="7b095-104">FreeIsolationInfo function</span></span>

> [!Note]  
> <span data-ttu-id="7b095-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7b095-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7b095-106">Функция **фриисолатионинфо** освобождает структуру данных [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) .</span><span class="sxs-lookup"><span data-stu-id="7b095-106">The **FreeIsolationInfo** function frees an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b095-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b095-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7b095-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b095-109">*исолатионинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b095-109">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b095-110">Указатель на структуру данных [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="7b095-110">A pointer to the [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b095-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b095-111">Remarks</span></span>

<span data-ttu-id="7b095-112">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="7b095-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7b095-113">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="7b095-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7b095-114">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7b095-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7b095-115">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7b095-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7b095-116">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="7b095-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b095-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7b095-117">Requirements</span></span>



| <span data-ttu-id="7b095-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7b095-118">Requirement</span></span> | <span data-ttu-id="7b095-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7b095-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b095-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b095-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b095-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b095-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7b095-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b095-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b095-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b095-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7b095-124">Header</span><span class="sxs-lookup"><span data-stu-id="7b095-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b095-125"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b095-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7b095-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7b095-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b095-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b095-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





