---
title: Функция Глуделетенурбсрендерер (GLU. h)
description: Функция Глуделетенурбсрендерер уничтожает неравномерный рациональный объект B-сплайна (НУРБС).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- Функция Глуделетенурбсрендерер OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802213"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="3c547-104">Функция Глуделетенурбсрендерер</span><span class="sxs-lookup"><span data-stu-id="3c547-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="3c547-105">Функция **глуделетенурбсрендерер** уничтожает неравномерный рациональный объект B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="3c547-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c547-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c547-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="3c547-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c547-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c547-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="3c547-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="3c547-109">Объект НУРБС для уничтожения (созданный с помощью **глуневнурбсрендерер**).</span><span class="sxs-lookup"><span data-stu-id="3c547-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c547-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c547-110">Return value</span></span>

<span data-ttu-id="3c547-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3c547-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c547-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c547-112">Remarks</span></span>

<span data-ttu-id="3c547-113">Функция **глуделетенурбсрендерер** уничтожает объект нурбс и освобождает используемую память.</span><span class="sxs-lookup"><span data-stu-id="3c547-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="3c547-114">После вызова **глуделетенурбсрендерер** нельзя использовать *нобж* повторно.</span><span class="sxs-lookup"><span data-stu-id="3c547-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c547-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3c547-115">Requirements</span></span>



| <span data-ttu-id="3c547-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3c547-116">Requirement</span></span> | <span data-ttu-id="3c547-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3c547-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c547-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c547-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c547-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c547-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3c547-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c547-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c547-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c547-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c547-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c547-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c547-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c547-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c547-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c547-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c547-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c547-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c547-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3c547-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c547-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c547-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c547-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c547-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c547-129">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="3c547-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





