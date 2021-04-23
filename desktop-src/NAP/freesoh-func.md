---
title: Функция Фрисох (Напутил. h)
description: Освобождает структуру данных SoH.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- Фрисох функция NAP
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28409c18bf9f673c78d6df2a224cb936223edddb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137510"
---
# <a name="freesoh-function"></a><span data-ttu-id="7a577-104">Функция Фрисох</span><span class="sxs-lookup"><span data-stu-id="7a577-104">FreeSoH function</span></span>

> [!Note]  
> <span data-ttu-id="7a577-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a577-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a577-106">Функция **фрисох** освобождает структуру данных **SoH** .</span><span class="sxs-lookup"><span data-stu-id="7a577-106">The **FreeSoH** function frees a **SoH** data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a577-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a577-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a><span data-ttu-id="7a577-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a577-109">*состояние работоспособности* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a577-109">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a577-110">Указатель на структуру данных [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="7a577-110">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a577-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a577-111">Remarks</span></span>

<span data-ttu-id="7a577-112">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="7a577-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7a577-113">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="7a577-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7a577-114">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7a577-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7a577-115">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7a577-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7a577-116">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="7a577-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a577-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7a577-117">Requirements</span></span>



| <span data-ttu-id="7a577-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7a577-118">Requirement</span></span> | <span data-ttu-id="7a577-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7a577-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a577-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a577-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a577-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a577-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7a577-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a577-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a577-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a577-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a577-124">Header</span><span class="sxs-lookup"><span data-stu-id="7a577-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a577-125"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a577-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7a577-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7a577-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a577-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a577-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





