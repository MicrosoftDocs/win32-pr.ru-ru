---
description: Создает разницу между указанным исходным файлом и указанным целевым файлом.
title: Функция Креатепатчфиликса/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721009"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="56d7d-103">Функция Креатепатчфиликса/W</span><span class="sxs-lookup"><span data-stu-id="56d7d-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="56d7d-104">Функции **креатепатчфиликса** и **креатепатчфиликсв** создают разницу между указанным исходным файлом и указанным целевым файлом.</span><span class="sxs-lookup"><span data-stu-id="56d7d-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="56d7d-105">Исходные и целевые файлы предоставляются в виде путей.</span><span class="sxs-lookup"><span data-stu-id="56d7d-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="56d7d-106">Выходная Дельта также записывается в указанный путь.</span><span class="sxs-lookup"><span data-stu-id="56d7d-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="56d7d-107">Эти функции предоставляют отчеты о ходе выполнения в процессе создания.</span><span class="sxs-lookup"><span data-stu-id="56d7d-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d7d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56d7d-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="56d7d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="56d7d-109">Parameters</span></span>

<span data-ttu-id="56d7d-110">*олдфилекаунт*</span><span class="sxs-lookup"><span data-stu-id="56d7d-110">*OldFileCount*</span></span>

<span data-ttu-id="56d7d-111">Общее число исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="56d7d-111">The total number of source files.</span></span> <span data-ttu-id="56d7d-112">Используется для создания разностей к нескольким исходным файлам (максимум 255).</span><span class="sxs-lookup"><span data-stu-id="56d7d-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="56d7d-113">*олдфилеинфоаррай*</span><span class="sxs-lookup"><span data-stu-id="56d7d-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="56d7d-114">Указатель на массив сведений о исходном файле.</span><span class="sxs-lookup"><span data-stu-id="56d7d-114">Pointer to source file information array.</span></span>

<span data-ttu-id="56d7d-115">*невфиленаме*</span><span class="sxs-lookup"><span data-stu-id="56d7d-115">*NewFileName*</span></span>

<span data-ttu-id="56d7d-116">Имя конечного файла.</span><span class="sxs-lookup"><span data-stu-id="56d7d-116">The name of the target file.</span></span>

<span data-ttu-id="56d7d-117">*патчфиленаме*</span><span class="sxs-lookup"><span data-stu-id="56d7d-117">*PatchFileName*</span></span>

<span data-ttu-id="56d7d-118">Имя создаваемой разностной копии.</span><span class="sxs-lookup"><span data-stu-id="56d7d-118">The name of the delta that is created.</span></span>

<span data-ttu-id="56d7d-119">*оптионфлагс*</span><span class="sxs-lookup"><span data-stu-id="56d7d-119">*OptionFlags*</span></span>

<span data-ttu-id="56d7d-120">Флаги создания.</span><span class="sxs-lookup"><span data-stu-id="56d7d-120">Creation flags.</span></span>

<span data-ttu-id="56d7d-121">*прогресскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="56d7d-121">*ProgressCallback*</span></span>

<span data-ttu-id="56d7d-122">Указатель на обратный вызов, определяемый приложением.</span><span class="sxs-lookup"><span data-stu-id="56d7d-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="56d7d-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="56d7d-123">*CallbackContext*</span></span>

<span data-ttu-id="56d7d-124">Указатель на определяемый приложением контекст.</span><span class="sxs-lookup"><span data-stu-id="56d7d-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="56d7d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56d7d-125">Return value</span></span>

<span data-ttu-id="56d7d-126">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="56d7d-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d7d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="56d7d-127">Requirements</span></span>

| <span data-ttu-id="56d7d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="56d7d-128">Requirement</span></span> | <span data-ttu-id="56d7d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="56d7d-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56d7d-130">Header</span><span class="sxs-lookup"><span data-stu-id="56d7d-130">Header</span></span> | <span data-ttu-id="56d7d-131">патчапи. h</span><span class="sxs-lookup"><span data-stu-id="56d7d-131">patchapi.h</span></span> |
| <span data-ttu-id="56d7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="56d7d-132">DLL</span></span> | <span data-ttu-id="56d7d-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="56d7d-133">mspatchc.dll</span></span> |
| <span data-ttu-id="56d7d-134">Юникод</span><span class="sxs-lookup"><span data-stu-id="56d7d-134">Unicode</span></span> | <span data-ttu-id="56d7d-135">Реализовано как Креатепатчфиликсв (Юникод) и Креатепатчфиликса (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56d7d-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="56d7d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56d7d-136">See also</span></span>

[<span data-ttu-id="56d7d-137">патчапи</span><span class="sxs-lookup"><span data-stu-id="56d7d-137">PatchAPI</span></span>](patchapi.md)
