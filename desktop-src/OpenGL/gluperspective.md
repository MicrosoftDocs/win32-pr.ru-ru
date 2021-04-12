---
title: Функция Глуперспективе (GLU. h)
description: Функция Глуперспективе настраивает матрицу перспективной проекции.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- Функция Глуперспективе OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415928"
---
# <a name="gluperspective-function"></a><span data-ttu-id="ca07a-104">Функция Глуперспективе</span><span class="sxs-lookup"><span data-stu-id="ca07a-104">gluPerspective function</span></span>

<span data-ttu-id="ca07a-105">Функция **глуперспективе** настраивает матрицу перспективной проекции.</span><span class="sxs-lookup"><span data-stu-id="ca07a-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca07a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca07a-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="ca07a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca07a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca07a-108">*фови*</span><span class="sxs-lookup"><span data-stu-id="ca07a-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="ca07a-109">Поле угла представления (в градусах) в направлении по оси y.</span><span class="sxs-lookup"><span data-stu-id="ca07a-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="ca07a-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="ca07a-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="ca07a-111">Пропорции, определяющие поле представления в направлении по оси x.</span><span class="sxs-lookup"><span data-stu-id="ca07a-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="ca07a-112">Пропорции — это отношение *x* (ширина) к *y* (высота).</span><span class="sxs-lookup"><span data-stu-id="ca07a-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="ca07a-113">*знеар*</span><span class="sxs-lookup"><span data-stu-id="ca07a-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="ca07a-114">Расстояние от средства просмотра до ближайшей плоскости обрезки (всегда положительное).</span><span class="sxs-lookup"><span data-stu-id="ca07a-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="ca07a-115">*зфар*</span><span class="sxs-lookup"><span data-stu-id="ca07a-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="ca07a-116">Расстояние от средства просмотра до дальней плоскости (всегда положительное).</span><span class="sxs-lookup"><span data-stu-id="ca07a-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca07a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca07a-117">Return value</span></span>

<span data-ttu-id="ca07a-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ca07a-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca07a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca07a-119">Remarks</span></span>

<span data-ttu-id="ca07a-120">Функция **глуперспективе** задает Просмотр фрустум в мировой системе координат.</span><span class="sxs-lookup"><span data-stu-id="ca07a-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="ca07a-121">Как правило, пропорции в **глуперспективе** должны соответствовать пропорциям связанного окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="ca07a-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="ca07a-122">Например, *аспект* = 2,0 означает, что угол окна просмотра в два раза шире, чем в *x* , как и в *y*.</span><span class="sxs-lookup"><span data-stu-id="ca07a-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="ca07a-123">Если окно просмотра в два раза шире, чем высота, оно отображает изображение без искажений.</span><span class="sxs-lookup"><span data-stu-id="ca07a-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="ca07a-124">Матрица, созданная функцией **глуперспективе** , умножается на текущую матрицу, точно так же, как если бы [**глмултматрикс**](glmultmatrix.md) вызывалась с созданной матрицей.</span><span class="sxs-lookup"><span data-stu-id="ca07a-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="ca07a-125">Чтобы загрузить матрицу перспективы на текущий стек матриц, перед вызовом **глуперспективе** с вызовом [**гллоадидентити**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="ca07a-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca07a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ca07a-126">Requirements</span></span>



| <span data-ttu-id="ca07a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ca07a-127">Requirement</span></span> | <span data-ttu-id="ca07a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ca07a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca07a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca07a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ca07a-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca07a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ca07a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca07a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ca07a-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca07a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ca07a-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ca07a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca07a-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca07a-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ca07a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca07a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca07a-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca07a-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca07a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ca07a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca07a-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca07a-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca07a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca07a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca07a-140">**глфрустум**</span><span class="sxs-lookup"><span data-stu-id="ca07a-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="ca07a-141">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="ca07a-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="ca07a-142">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="ca07a-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="ca07a-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="ca07a-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





