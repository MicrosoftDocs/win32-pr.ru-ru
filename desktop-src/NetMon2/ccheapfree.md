---
description: Функция Кчеапфри освобождает память, выделенную функцией Кчеапаллок.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Функция Кчеапфри (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156706"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="55bd3-103">Функция Кчеапфри</span><span class="sxs-lookup"><span data-stu-id="55bd3-103">CCHeapFree function</span></span>

<span data-ttu-id="55bd3-104">Функция **кчеапфри** освобождает память, выделенную функцией **кчеапаллок** .</span><span class="sxs-lookup"><span data-stu-id="55bd3-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55bd3-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="55bd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bd3-107">*лпмем*</span><span class="sxs-lookup"><span data-stu-id="55bd3-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="55bd3-108">Указатель на память, которую выпустит эта функция.</span><span class="sxs-lookup"><span data-stu-id="55bd3-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55bd3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55bd3-109">Return value</span></span>

<span data-ttu-id="55bd3-110">Если функция **кчеапфри** выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="55bd3-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="55bd3-111">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="55bd3-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bd3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="55bd3-112">Requirements</span></span>



| <span data-ttu-id="55bd3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="55bd3-113">Requirement</span></span> | <span data-ttu-id="55bd3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="55bd3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55bd3-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55bd3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="55bd3-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55bd3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55bd3-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55bd3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="55bd3-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55bd3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55bd3-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55bd3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bd3-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55bd3-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="55bd3-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55bd3-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="55bd3-122"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55bd3-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="55bd3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="55bd3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bd3-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bd3-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bd3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55bd3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bd3-126">сеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="55bd3-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="55bd3-127">жеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="55bd3-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="55bd3-128">кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="55bd3-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="55bd3-129">кчеапреаллок</span><span class="sxs-lookup"><span data-stu-id="55bd3-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="55bd3-130">кчеапсизе</span><span class="sxs-lookup"><span data-stu-id="55bd3-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




