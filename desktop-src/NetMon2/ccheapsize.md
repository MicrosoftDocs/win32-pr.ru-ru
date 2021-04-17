---
description: Функция Кчеапсизе возвращает размер памяти, выделенной функцией Кчеапаллок.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Функция Кчеапсизе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663646"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="4dda6-103">Функция Кчеапсизе</span><span class="sxs-lookup"><span data-stu-id="4dda6-103">CCHeapSize function</span></span>

<span data-ttu-id="4dda6-104">Функция **кчеапсизе** возвращает размер памяти, выделенной функцией **кчеапаллок** .</span><span class="sxs-lookup"><span data-stu-id="4dda6-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dda6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dda6-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="4dda6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dda6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dda6-107">*лпмем*</span><span class="sxs-lookup"><span data-stu-id="4dda6-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="4dda6-108">Указатель на выделенную область памяти.</span><span class="sxs-lookup"><span data-stu-id="4dda6-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dda6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dda6-109">Return value</span></span>

<span data-ttu-id="4dda6-110">Если функция выполнена успешно, возвращаемое значение равно размеру запрошенного блока памяти, измеряемого в байтах.</span><span class="sxs-lookup"><span data-stu-id="4dda6-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="4dda6-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4dda6-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dda6-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4dda6-112">Requirements</span></span>



| <span data-ttu-id="4dda6-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4dda6-113">Requirement</span></span> | <span data-ttu-id="4dda6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4dda6-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4dda6-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dda6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4dda6-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4dda6-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4dda6-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dda6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4dda6-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4dda6-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4dda6-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4dda6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dda6-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dda6-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4dda6-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4dda6-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dda6-122"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dda6-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4dda6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4dda6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dda6-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dda6-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dda6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dda6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dda6-126">сеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="4dda6-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4dda6-127">жеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="4dda6-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="4dda6-128">кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="4dda6-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="4dda6-129">кчеапфри</span><span class="sxs-lookup"><span data-stu-id="4dda6-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="4dda6-130">кчеапреаллок</span><span class="sxs-lookup"><span data-stu-id="4dda6-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




