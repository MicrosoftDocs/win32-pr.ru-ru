---
title: Функция D3DPERF_BeginEvent
description: Помечает начало определяемого пользователем события. PIX может использовать это событие для активации действия.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412645"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="9e386-104">Функция D3DPERF_BeginEvent</span><span class="sxs-lookup"><span data-stu-id="9e386-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="9e386-105">Помечает начало определяемого пользователем события.</span><span class="sxs-lookup"><span data-stu-id="9e386-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="9e386-106">PIX может использовать это событие для активации действия.</span><span class="sxs-lookup"><span data-stu-id="9e386-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e386-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e386-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="9e386-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e386-108">Parameters</span></span>

`col`

<span data-ttu-id="9e386-109">Цвет события.</span><span class="sxs-lookup"><span data-stu-id="9e386-109">Event color.</span></span> <span data-ttu-id="9e386-110">Это цвет для отображения события в представлении событий.</span><span class="sxs-lookup"><span data-stu-id="9e386-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="9e386-111">Имя события.</span><span class="sxs-lookup"><span data-stu-id="9e386-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e386-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e386-112">Return value</span></span>

<span data-ttu-id="9e386-113">Отсчитываемый от нуля уровень иерархии, в которой начинается это событие.</span><span class="sxs-lookup"><span data-stu-id="9e386-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="9e386-114">При возникновении ошибки возвращаемое значение будет отрицательным.</span><span class="sxs-lookup"><span data-stu-id="9e386-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e386-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e386-115">Remarks</span></span>

<span data-ttu-id="9e386-116">Определяемые пользователем события группируют вместе другие события таким образом, чтобы их можно было лучше представить в средствах профилирования производительности.</span><span class="sxs-lookup"><span data-stu-id="9e386-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="9e386-117">Например, событие *прорисовки пробела* может быть заключено в скобки с несколькими вызовами Direct3D, которые обрисуют место игры.</span><span class="sxs-lookup"><span data-stu-id="9e386-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="9e386-118">События могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="9e386-118">Events can be nested.</span></span>

<span data-ttu-id="9e386-119">Каждый вызов **D3DPERF_BeginEvent** должен иметь соответствующий вызов **D3DPERF_EndEvent** .</span><span class="sxs-lookup"><span data-stu-id="9e386-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="9e386-120">Мгновенные события (которые не обозначают другие события) должны быть помечены с помощью **D3DPERF_SetMarker** , а не **D3DPERF_BeginEvent** и **D3DPERF_EndEvent**.</span><span class="sxs-lookup"><span data-stu-id="9e386-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e386-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9e386-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9e386-122">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="9e386-122">**Target Platform**</span></span> | <span data-ttu-id="9e386-123">Windows</span><span class="sxs-lookup"><span data-stu-id="9e386-123">Windows</span></span> |
| <span data-ttu-id="9e386-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="9e386-124">**Header**</span></span> | <span data-ttu-id="9e386-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="9e386-125">d3d9.h</span></span> |
| <span data-ttu-id="9e386-126">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="9e386-126">**Library**</span></span> | <span data-ttu-id="9e386-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="9e386-127">d3d9.lib</span></span> |
| <span data-ttu-id="9e386-128">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="9e386-128">**DLL**</span></span> | <span data-ttu-id="9e386-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="9e386-129">d3d9.dll</span></span> |