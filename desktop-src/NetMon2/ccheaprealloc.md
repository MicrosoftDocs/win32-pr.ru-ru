---
description: Функция Кчеапреаллок перераспределяет память, выделенную функцией Кчеапаллок.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Функция Кчеапреаллок (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813625"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="2949f-103">Функция Кчеапреаллок</span><span class="sxs-lookup"><span data-stu-id="2949f-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="2949f-104">Функция **кчеапреаллок** перераспределяет память, выделенную функцией **кчеапаллок** .</span><span class="sxs-lookup"><span data-stu-id="2949f-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2949f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2949f-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="2949f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2949f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2949f-107">*лпмем*</span><span class="sxs-lookup"><span data-stu-id="2949f-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="2949f-108">Указатель на исходную выделенную память.</span><span class="sxs-lookup"><span data-stu-id="2949f-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="2949f-109">*двбитес*</span><span class="sxs-lookup"><span data-stu-id="2949f-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="2949f-110">Размер перераспределенной памяти, измеряемый в байтах.</span><span class="sxs-lookup"><span data-stu-id="2949f-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2949f-111">*бзероинит*</span><span class="sxs-lookup"><span data-stu-id="2949f-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="2949f-112">Признак инициализации повторно выделяемой памяти.</span><span class="sxs-lookup"><span data-stu-id="2949f-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="2949f-113">Если значение параметра равно **true**, то вновь выделенная память инициализируется нулем.</span><span class="sxs-lookup"><span data-stu-id="2949f-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2949f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2949f-114">Return value</span></span>

<span data-ttu-id="2949f-115">Если функция выполнена успешно, возвращаемое значение является указателем на перераспределенную память.</span><span class="sxs-lookup"><span data-stu-id="2949f-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="2949f-116">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2949f-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2949f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2949f-117">Requirements</span></span>



| <span data-ttu-id="2949f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2949f-118">Requirement</span></span> | <span data-ttu-id="2949f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2949f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2949f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2949f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2949f-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2949f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2949f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2949f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2949f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2949f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2949f-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2949f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2949f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2949f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2949f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2949f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2949f-127"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2949f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2949f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2949f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2949f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2949f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2949f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2949f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2949f-131">сеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="2949f-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="2949f-132">жеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="2949f-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="2949f-133">кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="2949f-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="2949f-134">кчеапфри</span><span class="sxs-lookup"><span data-stu-id="2949f-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="2949f-135">кчеапсизе</span><span class="sxs-lookup"><span data-stu-id="2949f-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




