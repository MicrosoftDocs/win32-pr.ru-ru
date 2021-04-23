---
description: Функция СеткЦинстптр захватывает указатель экземпляра контекста.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Функция СеткЦинстптр (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542362"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="b7e80-103">Функция СеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="b7e80-103">SetCCInstPtr function</span></span>

<span data-ttu-id="b7e80-104">Функция **сеткЦинстптр** захватывает указатель экземпляра контекста.</span><span class="sxs-lookup"><span data-stu-id="b7e80-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7e80-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="b7e80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7e80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e80-107">*лпкуркаптуреинст*</span><span class="sxs-lookup"><span data-stu-id="b7e80-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e80-108">Указатель на данные экземпляра, добавленные в запись.</span><span class="sxs-lookup"><span data-stu-id="b7e80-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e80-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7e80-109">Return value</span></span>

<span data-ttu-id="b7e80-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7e80-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e80-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b7e80-111">Remarks</span></span>

<span data-ttu-id="b7e80-112">Эта функция используется для сохранения указателя на блок, который был выделен с помощью функции **кчеапаллок** .</span><span class="sxs-lookup"><span data-stu-id="b7e80-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="b7e80-113">Каждый синтаксический анализатор может устанавливать один экземпляр данных для записи.</span><span class="sxs-lookup"><span data-stu-id="b7e80-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e80-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7e80-114">Requirements</span></span>



| <span data-ttu-id="b7e80-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7e80-115">Requirement</span></span> | <span data-ttu-id="b7e80-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7e80-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e80-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7e80-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e80-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7e80-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b7e80-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7e80-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e80-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7e80-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7e80-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b7e80-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e80-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e80-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b7e80-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7e80-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7e80-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7e80-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7e80-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e80-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e80-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e80-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e80-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7e80-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e80-128">жеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="b7e80-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b7e80-129">кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="b7e80-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="b7e80-130">кчеапфри</span><span class="sxs-lookup"><span data-stu-id="b7e80-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="b7e80-131">кчеапреаллок</span><span class="sxs-lookup"><span data-stu-id="b7e80-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="b7e80-132">кчеапсизе</span><span class="sxs-lookup"><span data-stu-id="b7e80-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




