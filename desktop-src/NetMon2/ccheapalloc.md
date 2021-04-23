---
description: Функция Кчеапаллок выделяет память для каждого образа.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Функция Кчеапаллок (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909416"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="c351f-103">Функция Кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="c351f-103">CCHeapAlloc function</span></span>

<span data-ttu-id="c351f-104">Функция **кчеапаллок** выделяет память для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="c351f-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c351f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c351f-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="c351f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c351f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c351f-107">*двбитес*</span><span class="sxs-lookup"><span data-stu-id="c351f-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="c351f-108">Запрошенная Длина выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="c351f-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="c351f-109">*бзероинит*</span><span class="sxs-lookup"><span data-stu-id="c351f-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="c351f-110">Индикатор того, была ли инициализирована выделенная память.</span><span class="sxs-lookup"><span data-stu-id="c351f-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="c351f-111">Если значение параметра равно **true**, то выделенная память инициализируется нулем.</span><span class="sxs-lookup"><span data-stu-id="c351f-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c351f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c351f-112">Return value</span></span>

<span data-ttu-id="c351f-113">Если функция выполнена успешно, возвращаемое значение является указателем на выделенную память.</span><span class="sxs-lookup"><span data-stu-id="c351f-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="c351f-114">По завершении использования выделенной памяти освободите память, вызвав функцию [**кчеапфри**](ccheapfree.md) .</span><span class="sxs-lookup"><span data-stu-id="c351f-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="c351f-115">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c351f-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c351f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c351f-116">Requirements</span></span>



| <span data-ttu-id="c351f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c351f-117">Requirement</span></span> | <span data-ttu-id="c351f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c351f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c351f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c351f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c351f-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c351f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c351f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c351f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c351f-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c351f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c351f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c351f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c351f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c351f-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c351f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c351f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c351f-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c351f-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c351f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c351f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c351f-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c351f-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c351f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c351f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c351f-130">**сеткЦинстптр**</span><span class="sxs-lookup"><span data-stu-id="c351f-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="c351f-131">**жеткЦинстптр**</span><span class="sxs-lookup"><span data-stu-id="c351f-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="c351f-132">**кчеапфри**</span><span class="sxs-lookup"><span data-stu-id="c351f-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="c351f-133">**кчеапреаллок**</span><span class="sxs-lookup"><span data-stu-id="c351f-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="c351f-134">**кчеапсизе**</span><span class="sxs-lookup"><span data-stu-id="c351f-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




