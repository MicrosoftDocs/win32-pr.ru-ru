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
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414709"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="79cab-104">Функция gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="79cab-104">gluOrtho2D function</span></span>

<span data-ttu-id="79cab-105">Функция **gluOrtho2D** определяет матрицу двухмерной ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="79cab-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="79cab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79cab-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="79cab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79cab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79cab-108">*слева*</span><span class="sxs-lookup"><span data-stu-id="79cab-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="79cab-109">Координата для левой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="79cab-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="79cab-110">*Правильно*</span><span class="sxs-lookup"><span data-stu-id="79cab-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="79cab-111">Координата для правой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="79cab-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="79cab-112">*В начало*</span><span class="sxs-lookup"><span data-stu-id="79cab-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="79cab-113">Координата для верхней горизонтальной плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="79cab-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="79cab-114">*Нижний*</span><span class="sxs-lookup"><span data-stu-id="79cab-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="79cab-115">Координата для нижней горизонтальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="79cab-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79cab-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79cab-116">Return value</span></span>

<span data-ttu-id="79cab-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="79cab-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79cab-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79cab-118">Remarks</span></span>

<span data-ttu-id="79cab-119">Функция **gluOrtho2D** устанавливает двухмерную ортогональную область просмотра.</span><span class="sxs-lookup"><span data-stu-id="79cab-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="79cab-120">Это эквивалентно вызову [**глорсо**](glortho.md) с Near = 1 и FAR = 1.</span><span class="sxs-lookup"><span data-stu-id="79cab-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="79cab-121">Требования</span><span class="sxs-lookup"><span data-stu-id="79cab-121">Requirements</span></span>



| <span data-ttu-id="79cab-122">Требование</span><span class="sxs-lookup"><span data-stu-id="79cab-122">Requirement</span></span> | <span data-ttu-id="79cab-123">Значение</span><span class="sxs-lookup"><span data-stu-id="79cab-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79cab-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79cab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79cab-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79cab-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="79cab-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79cab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79cab-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79cab-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79cab-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="79cab-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79cab-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="79cab-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="79cab-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79cab-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="79cab-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79cab-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="79cab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="79cab-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79cab-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79cab-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79cab-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79cab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79cab-135">**глорсо**</span><span class="sxs-lookup"><span data-stu-id="79cab-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="79cab-136">**глуперспективе**</span><span class="sxs-lookup"><span data-stu-id="79cab-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





