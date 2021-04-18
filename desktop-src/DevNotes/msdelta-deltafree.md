---
description: Освобождает указанный блок памяти.
title: Функция DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721033"
---
# <a name="deltafree-function"></a><span data-ttu-id="19409-103">Функция DeltaFree</span><span class="sxs-lookup"><span data-stu-id="19409-103">DeltaFree function</span></span>

<span data-ttu-id="19409-104">Освобождает указанный блок памяти.</span><span class="sxs-lookup"><span data-stu-id="19409-104">Frees the specified memory block.</span></span> <span data-ttu-id="19409-105">Эту функцию необходимо вызвать после успешного вызова [креатеделтаб](msdelta-createdeltab.md) и [апплиделтаб](msdelta-applydeltab.md) , чтобы освободить буфер памяти, выделенный мсделта.</span><span class="sxs-lookup"><span data-stu-id="19409-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="19409-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19409-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="19409-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="19409-107">Parameters</span></span>

<span data-ttu-id="19409-108">*лпмемори*</span><span class="sxs-lookup"><span data-stu-id="19409-108">*lpMemory*</span></span>

<span data-ttu-id="19409-109">окне Блок памяти, который должен быть освобожден.</span><span class="sxs-lookup"><span data-stu-id="19409-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="19409-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19409-110">Return value</span></span>

<span data-ttu-id="19409-111">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="19409-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="19409-112">Если функция возвращает **значение false**, можно вызвать [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить соответствующий код системной ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="19409-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19409-113">Требования</span><span class="sxs-lookup"><span data-stu-id="19409-113">Requirements</span></span>

| <span data-ttu-id="19409-114">Требование</span><span class="sxs-lookup"><span data-stu-id="19409-114">Requirement</span></span> | <span data-ttu-id="19409-115">Значение</span><span class="sxs-lookup"><span data-stu-id="19409-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19409-116">Header</span><span class="sxs-lookup"><span data-stu-id="19409-116">Header</span></span> | <span data-ttu-id="19409-117">мсделта. h</span><span class="sxs-lookup"><span data-stu-id="19409-117">msdelta.h</span></span> |
| <span data-ttu-id="19409-118">DLL</span><span class="sxs-lookup"><span data-stu-id="19409-118">DLL</span></span> | <span data-ttu-id="19409-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="19409-119">msdelta.dll</span></span> |
| <span data-ttu-id="19409-120">Юникод</span><span class="sxs-lookup"><span data-stu-id="19409-120">Unicode</span></span> | <span data-ttu-id="19409-121">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="19409-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="19409-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19409-122">See also</span></span>

[<span data-ttu-id="19409-123">мсделта</span><span class="sxs-lookup"><span data-stu-id="19409-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="19409-124">креатеделтаб</span><span class="sxs-lookup"><span data-stu-id="19409-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="19409-125">апплиделтаб</span><span class="sxs-lookup"><span data-stu-id="19409-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
