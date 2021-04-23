---
description: Функция ЖеткЦинстптр возвращает указатель на данные экземпляра, добавленные в контекст записи.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Функция ЖеткЦинстптр (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808717"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="def26-103">Функция ЖеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="def26-103">GetCCInstPtr function</span></span>

<span data-ttu-id="def26-104">Функция **жеткЦинстптр** возвращает указатель на данные экземпляра, добавленные в контекст записи.</span><span class="sxs-lookup"><span data-stu-id="def26-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="def26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="def26-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="def26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="def26-106">Parameters</span></span>

<span data-ttu-id="def26-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="def26-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="def26-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="def26-108">Return value</span></span>

<span data-ttu-id="def26-109">Если функция выполнена успешно, возвращаемое значение является указателем на данные экземпляра определенной записи.</span><span class="sxs-lookup"><span data-stu-id="def26-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="def26-110">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="def26-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="def26-111">Требования</span><span class="sxs-lookup"><span data-stu-id="def26-111">Requirements</span></span>



| <span data-ttu-id="def26-112">Требование</span><span class="sxs-lookup"><span data-stu-id="def26-112">Requirement</span></span> | <span data-ttu-id="def26-113">Значение</span><span class="sxs-lookup"><span data-stu-id="def26-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="def26-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="def26-114">Minimum supported client</span></span><br/> | <span data-ttu-id="def26-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="def26-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="def26-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="def26-116">Minimum supported server</span></span><br/> | <span data-ttu-id="def26-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="def26-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="def26-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="def26-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="def26-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="def26-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="def26-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="def26-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="def26-121"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="def26-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="def26-122">DLL</span><span class="sxs-lookup"><span data-stu-id="def26-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def26-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def26-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def26-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="def26-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def26-125">сеткЦинстптр</span><span class="sxs-lookup"><span data-stu-id="def26-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="def26-126">кчеапаллок</span><span class="sxs-lookup"><span data-stu-id="def26-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="def26-127">кчеапфри</span><span class="sxs-lookup"><span data-stu-id="def26-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="def26-128">кчеапреаллок</span><span class="sxs-lookup"><span data-stu-id="def26-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="def26-129">кчеапсизе</span><span class="sxs-lookup"><span data-stu-id="def26-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




