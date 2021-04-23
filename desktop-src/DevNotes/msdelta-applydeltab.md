---
description: Использует разницу и источник (предоставленные в виде буферов) для создания новой копии целевых данных. Выходные данные возвращаются в буфер, выделенный Мсделта.
title: Функция ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721035"
---
# <a name="applydeltab-function"></a><span data-ttu-id="c8990-104">Функция ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="c8990-104">ApplyDeltaB function</span></span>

<span data-ttu-id="c8990-105">Использует разницу и источник (предоставленные в виде буферов) для создания новой копии целевых данных.</span><span class="sxs-lookup"><span data-stu-id="c8990-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="c8990-106">Выходные данные возвращаются в буфер, выделенный Мсделта.</span><span class="sxs-lookup"><span data-stu-id="c8990-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="c8990-107">Необходимо вызвать [делтафри](msdelta-deltafree.md) , чтобы освободить выходной буфер после завершения этой функции.</span><span class="sxs-lookup"><span data-stu-id="c8990-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="c8990-108">Если указанная Дельта была создана с помощью [патчапи](patchapi.md)и установлен флаг [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , мсделта будет вызывать патчапи для применения разницы.</span><span class="sxs-lookup"><span data-stu-id="c8990-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8990-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8990-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="c8990-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8990-110">Parameters</span></span>

<span data-ttu-id="c8990-111">*апплифлагс*</span><span class="sxs-lookup"><span data-stu-id="c8990-111">*ApplyFlags*</span></span>

<span data-ttu-id="c8990-112">окне Либо [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , либо [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="c8990-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="c8990-113">*Источник*</span><span class="sxs-lookup"><span data-stu-id="c8990-113">*Source*</span></span>

<span data-ttu-id="c8990-114">окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий исходные данные.</span><span class="sxs-lookup"><span data-stu-id="c8990-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="c8990-115">*Разностная версия*</span><span class="sxs-lookup"><span data-stu-id="c8990-115">*Delta*</span></span>

<span data-ttu-id="c8990-116">окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий разностные данные.</span><span class="sxs-lookup"><span data-stu-id="c8990-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="c8990-117">*лптаржет*</span><span class="sxs-lookup"><span data-stu-id="c8990-117">*lpTarget*</span></span>

<span data-ttu-id="c8990-118">заполняет Указатель на структуру [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) , в которой будет записан целевой объект.</span><span class="sxs-lookup"><span data-stu-id="c8990-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8990-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8990-119">Return value</span></span>

<span data-ttu-id="c8990-120">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c8990-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="c8990-121">Если функция возвращает **значение false**, можно вызвать [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить соответствующий код системной ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="c8990-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8990-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c8990-122">Requirements</span></span>

| <span data-ttu-id="c8990-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c8990-123">Requirement</span></span> | <span data-ttu-id="c8990-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c8990-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8990-125">Header</span><span class="sxs-lookup"><span data-stu-id="c8990-125">Header</span></span> | <span data-ttu-id="c8990-126">мсделта. h</span><span class="sxs-lookup"><span data-stu-id="c8990-126">msdelta.h</span></span> |
| <span data-ttu-id="c8990-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c8990-127">DLL</span></span> | <span data-ttu-id="c8990-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="c8990-128">msdelta.dll</span></span> |
| <span data-ttu-id="c8990-129">Юникод</span><span class="sxs-lookup"><span data-stu-id="c8990-129">Unicode</span></span> | <span data-ttu-id="c8990-130">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="c8990-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="c8990-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8990-131">See also</span></span>

[<span data-ttu-id="c8990-132">мсделта</span><span class="sxs-lookup"><span data-stu-id="c8990-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="c8990-133">делтафри</span><span class="sxs-lookup"><span data-stu-id="c8990-133">DeltaFree</span></span>](msdelta-deltafree.md)
