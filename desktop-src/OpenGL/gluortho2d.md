---
title: Функция gluOrtho2D (GLU. h)
description: Функция gluOrtho2D определяет матрицу двухмерной ортогональной проекции.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Функция gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153557"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="f156e-104">Функция gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="f156e-104">gluOrtho2D function</span></span>

<span data-ttu-id="f156e-105">Функция **gluOrtho2D** определяет матрицу двухмерной ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="f156e-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f156e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f156e-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="f156e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f156e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f156e-108">*Левое*</span><span class="sxs-lookup"><span data-stu-id="f156e-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="f156e-109">Координата для левой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="f156e-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="f156e-110">*Правильно*</span><span class="sxs-lookup"><span data-stu-id="f156e-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="f156e-111">Координата для правой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="f156e-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="f156e-112">*В начало*</span><span class="sxs-lookup"><span data-stu-id="f156e-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="f156e-113">Координата для верхней горизонтальной плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="f156e-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="f156e-114">*Нижний*</span><span class="sxs-lookup"><span data-stu-id="f156e-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="f156e-115">Координата для нижней горизонтальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="f156e-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f156e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f156e-116">Return value</span></span>

<span data-ttu-id="f156e-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f156e-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f156e-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="f156e-118">Remarks</span></span>

<span data-ttu-id="f156e-119">Функция **gluOrtho2D** устанавливает двухмерную ортогональную область просмотра.</span><span class="sxs-lookup"><span data-stu-id="f156e-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="f156e-120">Это эквивалентно вызову [**глорсо**](glortho.md) с знеар =-1 и зфар = 1.</span><span class="sxs-lookup"><span data-stu-id="f156e-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f156e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f156e-121">Requirements</span></span>



| <span data-ttu-id="f156e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f156e-122">Requirement</span></span> | <span data-ttu-id="f156e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f156e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f156e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f156e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f156e-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f156e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f156e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f156e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f156e-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f156e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f156e-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f156e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f156e-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f156e-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f156e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f156e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f156e-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f156e-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f156e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f156e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f156e-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f156e-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f156e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f156e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f156e-135">**глорсо**</span><span class="sxs-lookup"><span data-stu-id="f156e-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="f156e-136">**глуперспективе**</span><span class="sxs-lookup"><span data-stu-id="f156e-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





