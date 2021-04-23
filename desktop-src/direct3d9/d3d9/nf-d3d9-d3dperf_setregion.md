---
title: Функция D3DPERF_SetRegion
description: Пометьте ряд кадров с указанными цветом и именем в файле Пиксрун. Эта функция в настоящее время не поддерживается PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "105719115"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="ba4ee-104">Функция D3DPERF_SetRegion</span><span class="sxs-lookup"><span data-stu-id="ba4ee-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="ba4ee-105">Пометьте ряд кадров с указанными цветом и именем в файле Пиксрун.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="ba4ee-106">Эта функция в настоящее время не поддерживается PIX.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba4ee-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="ba4ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba4ee-108">Parameters</span></span>

`col`

<span data-ttu-id="ba4ee-109">Цвет события.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-109">Event color.</span></span> <span data-ttu-id="ba4ee-110">Это цвет для отображения события в представлении событий.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="ba4ee-111">Имя события.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba4ee-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba4ee-112">Return value</span></span>

<span data-ttu-id="ba4ee-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4ee-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba4ee-114">Remarks</span></span>

<span data-ttu-id="ba4ee-115">Чтобы упростить анализ, Целевая программа может использовать цвет для пометки каждого уровня целевой программы.</span><span class="sxs-lookup"><span data-stu-id="ba4ee-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba4ee-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ba4ee-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ba4ee-117">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-117">**Target Platform**</span></span> | <span data-ttu-id="ba4ee-118">Windows</span><span class="sxs-lookup"><span data-stu-id="ba4ee-118">Windows</span></span> |
| <span data-ttu-id="ba4ee-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-119">**Header**</span></span> | <span data-ttu-id="ba4ee-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="ba4ee-120">d3d9.h</span></span> |
| <span data-ttu-id="ba4ee-121">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-121">**Library**</span></span> | <span data-ttu-id="ba4ee-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="ba4ee-122">d3d9.lib</span></span> |
| <span data-ttu-id="ba4ee-123">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="ba4ee-123">**DLL**</span></span> | <span data-ttu-id="ba4ee-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="ba4ee-124">d3d9.dll</span></span> |