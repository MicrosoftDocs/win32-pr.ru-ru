---
title: Функция Глуневнурбсрендерер (GLU. h)
description: Функция Глуневнурбсрендерер создает неравномерный рациональный объект B-сплайна (НУРБС).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- Функция Глуневнурбсрендерер OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988884"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="5a3f4-104">Функция Глуневнурбсрендерер</span><span class="sxs-lookup"><span data-stu-id="5a3f4-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="5a3f4-105">Функция **глуневнурбсрендерер** создает неравномерный рациональный объект B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="5a3f4-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3f4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a3f4-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="5a3f4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a3f4-107">Parameters</span></span>

<span data-ttu-id="5a3f4-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a3f4-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a3f4-109">Remarks</span></span>

<span data-ttu-id="5a3f4-110">Функция **глуневнурбсрендерер** создает и возвращает указатель на новый объект нурбс.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="5a3f4-111">Используйте этот объект при вызове функций отрисовки НУРБС и управления.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="5a3f4-112">Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3f4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5a3f4-113">Requirements</span></span>



| <span data-ttu-id="5a3f4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5a3f4-114">Requirement</span></span> | <span data-ttu-id="5a3f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5a3f4-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3f4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a3f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3f4-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a3f4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5a3f4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a3f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3f4-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a3f4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a3f4-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5a3f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3f4-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f4-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5a3f4-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a3f4-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a3f4-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f4-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a3f4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5a3f4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3f4-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f4-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3f4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a3f4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3f4-127">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-128">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-129">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-130">**глуделетенурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-131">*глунурбскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="5a3f4-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-132">**глунурбспроперти**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





