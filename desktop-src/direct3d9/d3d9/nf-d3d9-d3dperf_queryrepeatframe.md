---
title: Функция D3DPERF_QueryRepeatFrame
description: Определите, запрашивает ли профилировщик производительности запрос о повторной отправке текущего кадра в Direct3D для анализа производительности. Эта функция в настоящее время не поддерживается PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "103789048"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="55dab-104">Функция D3DPERF_QueryRepeatFrame</span><span class="sxs-lookup"><span data-stu-id="55dab-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="55dab-105">Определите, запрашивает ли профилировщик производительности запрос о повторной отправке текущего кадра в Direct3D для анализа производительности.</span><span class="sxs-lookup"><span data-stu-id="55dab-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="55dab-106">Эта функция в настоящее время не поддерживается PIX.</span><span class="sxs-lookup"><span data-stu-id="55dab-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="55dab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55dab-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="55dab-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55dab-108">Return value</span></span>

<span data-ttu-id="55dab-109">Если возвращаемое значение равно TRUE, вызывающий объект должен повторить ту же последовательность вызовов.</span><span class="sxs-lookup"><span data-stu-id="55dab-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="55dab-110">Если значение равно FALSE, вызывающий объект должен продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="55dab-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="55dab-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55dab-111">Remarks</span></span>

<span data-ttu-id="55dab-112">Функция должна вызываться сразу после **IDirect3DDevice9::P** вызывается повторная отправка.</span><span class="sxs-lookup"><span data-stu-id="55dab-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="55dab-113">Требования</span><span class="sxs-lookup"><span data-stu-id="55dab-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="55dab-114">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="55dab-114">**Target Platform**</span></span> | <span data-ttu-id="55dab-115">Windows</span><span class="sxs-lookup"><span data-stu-id="55dab-115">Windows</span></span> |
| <span data-ttu-id="55dab-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="55dab-116">**Header**</span></span> | <span data-ttu-id="55dab-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="55dab-117">d3d9.h</span></span> |
| <span data-ttu-id="55dab-118">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="55dab-118">**Library**</span></span> | <span data-ttu-id="55dab-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="55dab-119">d3d9.lib</span></span> |
| <span data-ttu-id="55dab-120">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="55dab-120">**DLL**</span></span> | <span data-ttu-id="55dab-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="55dab-121">d3d9.dll</span></span> |