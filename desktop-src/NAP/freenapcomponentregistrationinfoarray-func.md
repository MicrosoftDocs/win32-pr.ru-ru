---
title: Функция Фринапкомпонентрегистратионинфоаррай (Напутил. h)
description: Освобождает указанное число структур данных Напкомпонентрегистратионинфо из массива.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Фринапкомпонентрегистратионинфоаррай функция NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137058"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="851e3-104">Функция Фринапкомпонентрегистратионинфоаррай</span><span class="sxs-lookup"><span data-stu-id="851e3-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="851e3-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="851e3-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="851e3-106">Функция **фринапкомпонентрегистратионинфоаррай** освобождает указанное число структур данных [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) из массива.</span><span class="sxs-lookup"><span data-stu-id="851e3-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="851e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="851e3-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="851e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="851e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="851e3-109">*количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="851e3-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851e3-110">Количество [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) структур в *info* , которые должны быть свободны.</span><span class="sxs-lookup"><span data-stu-id="851e3-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="851e3-111">*сведения о* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="851e3-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851e3-112">Указатель на массив структур данных [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , которые должны быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="851e3-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="851e3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="851e3-113">Remarks</span></span>

<span data-ttu-id="851e3-114">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="851e3-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="851e3-115">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="851e3-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="851e3-116">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="851e3-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="851e3-117">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="851e3-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="851e3-118">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="851e3-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="851e3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="851e3-119">Requirements</span></span>



| <span data-ttu-id="851e3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="851e3-120">Requirement</span></span> | <span data-ttu-id="851e3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="851e3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="851e3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="851e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="851e3-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="851e3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="851e3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="851e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="851e3-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="851e3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="851e3-126">Header</span><span class="sxs-lookup"><span data-stu-id="851e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="851e3-127"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="851e3-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="851e3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="851e3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="851e3-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="851e3-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





