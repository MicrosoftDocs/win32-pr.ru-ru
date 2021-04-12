---
title: Функция D3DPERF_GetStatus
description: Определите текущее состояние профилировщика из целевой программы.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104336583"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="fce22-103">Функция D3DPERF_GetStatus</span><span class="sxs-lookup"><span data-stu-id="fce22-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="fce22-104">Определите текущее состояние профилировщика из целевой программы.</span><span class="sxs-lookup"><span data-stu-id="fce22-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce22-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fce22-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="fce22-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fce22-106">Return value</span></span>

<span data-ttu-id="fce22-107">Ненулевое значение, когда PIX проведет профилирование целевой программы; в противном случае — нуль.</span><span class="sxs-lookup"><span data-stu-id="fce22-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce22-108">Требования</span><span class="sxs-lookup"><span data-stu-id="fce22-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fce22-109">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="fce22-109">**Target Platform**</span></span> | <span data-ttu-id="fce22-110">Windows</span><span class="sxs-lookup"><span data-stu-id="fce22-110">Windows</span></span> |
| <span data-ttu-id="fce22-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="fce22-111">**Header**</span></span> | <span data-ttu-id="fce22-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="fce22-112">d3d9.h</span></span> |
| <span data-ttu-id="fce22-113">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="fce22-113">**Library**</span></span> | <span data-ttu-id="fce22-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="fce22-114">d3d9.lib</span></span> |
| <span data-ttu-id="fce22-115">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="fce22-115">**DLL**</span></span> | <span data-ttu-id="fce22-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="fce22-116">d3d9.dll</span></span> |