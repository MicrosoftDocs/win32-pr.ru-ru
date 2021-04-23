---
title: Функция Глулукат (GLU. h)
description: Функция Глулукат определяет преобразование просмотра.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- Функция Глулукат OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892738"
---
# <a name="glulookat-function"></a><span data-ttu-id="fd841-104">Функция Глулукат</span><span class="sxs-lookup"><span data-stu-id="fd841-104">gluLookAt function</span></span>

<span data-ttu-id="fd841-105">Функция **глулукат** определяет преобразование просмотра.</span><span class="sxs-lookup"><span data-stu-id="fd841-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd841-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd841-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="fd841-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd841-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd841-108">*эйекс*</span><span class="sxs-lookup"><span data-stu-id="fd841-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-109">Расположение точки глаза.</span><span class="sxs-lookup"><span data-stu-id="fd841-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-110">*эйэй*</span><span class="sxs-lookup"><span data-stu-id="fd841-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-111">Расположение точки глаза.</span><span class="sxs-lookup"><span data-stu-id="fd841-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-112">*эйез*</span><span class="sxs-lookup"><span data-stu-id="fd841-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-113">Расположение точки глаза.</span><span class="sxs-lookup"><span data-stu-id="fd841-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-114">*CenterX*</span><span class="sxs-lookup"><span data-stu-id="fd841-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-115">Расположение точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="fd841-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="fd841-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-117">Расположение точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="fd841-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-118">*CenterZ*</span><span class="sxs-lookup"><span data-stu-id="fd841-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-119">Расположение точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="fd841-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-120">*упкс*</span><span class="sxs-lookup"><span data-stu-id="fd841-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-121">Направление вектора вверх.</span><span class="sxs-lookup"><span data-stu-id="fd841-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-122">*упи*</span><span class="sxs-lookup"><span data-stu-id="fd841-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-123">Направление вектора вверх.</span><span class="sxs-lookup"><span data-stu-id="fd841-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="fd841-124">*упз*</span><span class="sxs-lookup"><span data-stu-id="fd841-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="fd841-125">Направление вектора вверх.</span><span class="sxs-lookup"><span data-stu-id="fd841-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd841-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd841-126">Return value</span></span>

<span data-ttu-id="fd841-127">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fd841-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd841-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd841-128">Remarks</span></span>

<span data-ttu-id="fd841-129">Функция **глулукат** создает матрицу просмотра, производную от точки глаза, точку ссылки, указывающую центр сцены, и вектор вверх.</span><span class="sxs-lookup"><span data-stu-id="fd841-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="fd841-130">Матрица сопоставляет контрольную точку с отрицательной осью z и глаз до начала координат, поэтому при использовании типичной матрицы проекции центр сцены сопоставляется с центром окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="fd841-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="fd841-131">Аналогично, направление, описываемое вектором вверх, проецированным на плоскость просмотра, сопоставляется с положительной осью y, чтобы она указывала вверх в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="fd841-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="fd841-132">Вектор вверх не должен быть параллельным с линией зрения, от глаза до контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="fd841-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="fd841-133">Матрица, созданная с помощью **глулукат** , умножает текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="fd841-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd841-134">Требования</span><span class="sxs-lookup"><span data-stu-id="fd841-134">Requirements</span></span>



| <span data-ttu-id="fd841-135">Требование</span><span class="sxs-lookup"><span data-stu-id="fd841-135">Requirement</span></span> | <span data-ttu-id="fd841-136">Значение</span><span class="sxs-lookup"><span data-stu-id="fd841-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd841-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd841-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fd841-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fd841-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fd841-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd841-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fd841-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fd841-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd841-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fd841-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd841-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd841-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fd841-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd841-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd841-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd841-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd841-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fd841-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd841-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd841-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd841-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd841-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd841-148">**глфрустум**</span><span class="sxs-lookup"><span data-stu-id="fd841-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="fd841-149">**глуперспективе**</span><span class="sxs-lookup"><span data-stu-id="fd841-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





