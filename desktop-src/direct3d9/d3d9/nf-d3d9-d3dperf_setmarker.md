---
title: Функция D3DPERF_SetMarker
description: Отметить мгновенное событие. PIX может использовать это событие для активации действия.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412646"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="98d22-104">Функция D3DPERF_SetMarker</span><span class="sxs-lookup"><span data-stu-id="98d22-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="98d22-105">Отметить мгновенное событие.</span><span class="sxs-lookup"><span data-stu-id="98d22-105">Mark an instantaneous event.</span></span> <span data-ttu-id="98d22-106">PIX может использовать это событие для активации действия.</span><span class="sxs-lookup"><span data-stu-id="98d22-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d22-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98d22-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="98d22-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="98d22-108">Parameters</span></span>

`col`

<span data-ttu-id="98d22-109">Цвет события.</span><span class="sxs-lookup"><span data-stu-id="98d22-109">Event color.</span></span> <span data-ttu-id="98d22-110">Это цвет для отображения события в представлении событий.</span><span class="sxs-lookup"><span data-stu-id="98d22-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="98d22-111">Имя события.</span><span class="sxs-lookup"><span data-stu-id="98d22-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="98d22-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98d22-112">Return value</span></span>

<span data-ttu-id="98d22-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="98d22-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d22-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d22-114">Remarks</span></span>

<span data-ttu-id="98d22-115">Мгновенные события пользователя не имеют круглых скобок и не группируют другие события.</span><span class="sxs-lookup"><span data-stu-id="98d22-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="98d22-116">Например, когда пользователь запускает оружия в игре, событие « *снимок* » может быть создано **D3DPERF_SetMarkerным** вызовом.</span><span class="sxs-lookup"><span data-stu-id="98d22-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="98d22-117">Чтобы сгруппировать несколько событий под одним, определяемым пользователем именем, используйте **D3DPERF_BeginEvent** и **D3DPERF_EndEvent** , а не **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="98d22-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d22-118">Требования</span><span class="sxs-lookup"><span data-stu-id="98d22-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="98d22-119">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="98d22-119">**Target Platform**</span></span> | <span data-ttu-id="98d22-120">Windows</span><span class="sxs-lookup"><span data-stu-id="98d22-120">Windows</span></span> |
| <span data-ttu-id="98d22-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="98d22-121">**Header**</span></span> | <span data-ttu-id="98d22-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="98d22-122">d3d9.h</span></span> |
| <span data-ttu-id="98d22-123">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="98d22-123">**Library**</span></span> | <span data-ttu-id="98d22-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="98d22-124">d3d9.lib</span></span> |
| <span data-ttu-id="98d22-125">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="98d22-125">**DLL**</span></span> | <span data-ttu-id="98d22-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="98d22-126">d3d9.dll</span></span> |