---
title: Функция D3DPERF_EndEvent
description: Помечает конец определяемого пользователем события. PIX может использовать это событие для активации действия.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412647"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="85347-104">Функция D3DPERF_EndEvent</span><span class="sxs-lookup"><span data-stu-id="85347-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="85347-105">Помечает конец определяемого пользователем события.</span><span class="sxs-lookup"><span data-stu-id="85347-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="85347-106">PIX может использовать это событие для активации действия.</span><span class="sxs-lookup"><span data-stu-id="85347-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="85347-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85347-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="85347-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85347-108">Return value</span></span>

<span data-ttu-id="85347-109">Уровень иерархии, в которой событие завершается.</span><span class="sxs-lookup"><span data-stu-id="85347-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="85347-110">Если возникает ошибка, это значение отрицательно.</span><span class="sxs-lookup"><span data-stu-id="85347-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="85347-111">Требования</span><span class="sxs-lookup"><span data-stu-id="85347-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="85347-112">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="85347-112">**Target Platform**</span></span> | <span data-ttu-id="85347-113">Windows</span><span class="sxs-lookup"><span data-stu-id="85347-113">Windows</span></span> |
| <span data-ttu-id="85347-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="85347-114">**Header**</span></span> | <span data-ttu-id="85347-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="85347-115">d3d9.h</span></span> |
| <span data-ttu-id="85347-116">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="85347-116">**Library**</span></span> | <span data-ttu-id="85347-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="85347-117">d3d9.lib</span></span> |
| <span data-ttu-id="85347-118">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="85347-118">**DLL**</span></span> | <span data-ttu-id="85347-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="85347-119">d3d9.dll</span></span> |