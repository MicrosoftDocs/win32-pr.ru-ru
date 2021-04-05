---
title: Функция Глупиккматрикс (GLU. h)
description: Функция Глупиккматрикс определяет регион комплектации.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- Функция Глупиккматрикс OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988168"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="8ea18-104">Функция Глупиккматрикс</span><span class="sxs-lookup"><span data-stu-id="8ea18-104">gluPickMatrix function</span></span>

<span data-ttu-id="8ea18-105">Функция **глупиккматрикс** определяет регион комплектации.</span><span class="sxs-lookup"><span data-stu-id="8ea18-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea18-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ea18-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="8ea18-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ea18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea18-108">*x*</span><span class="sxs-lookup"><span data-stu-id="8ea18-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea18-109">Координата окна x области комплектации.</span><span class="sxs-lookup"><span data-stu-id="8ea18-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="8ea18-110">*y*</span><span class="sxs-lookup"><span data-stu-id="8ea18-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea18-111">Координата окна y области комплектации.</span><span class="sxs-lookup"><span data-stu-id="8ea18-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="8ea18-112">*height*</span><span class="sxs-lookup"><span data-stu-id="8ea18-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea18-113">Высота области комплектации в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="8ea18-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8ea18-114">*width*</span><span class="sxs-lookup"><span data-stu-id="8ea18-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea18-115">Ширина области комплектации в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="8ea18-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8ea18-116">*просмотра*</span><span class="sxs-lookup"><span data-stu-id="8ea18-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea18-117">Текущее окно просмотра (как в вызове [**глжетинтежерв**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="8ea18-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea18-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ea18-118">Return value</span></span>

<span data-ttu-id="8ea18-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8ea18-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea18-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ea18-120">Remarks</span></span>

<span data-ttu-id="8ea18-121">Функция **глупиккматрикс** создает матрицу проекции, которую можно использовать для ограничения рисования в небольшой области окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="8ea18-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="8ea18-122">Используйте **глупиккматрикс** , чтобы ограничить рисование в небольшой области вокруг курсора.</span><span class="sxs-lookup"><span data-stu-id="8ea18-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="8ea18-123">Перейдите в режим выбора (с [**глрендермоде**](glrendermode.md)), а затем Воссоздайте сцену.</span><span class="sxs-lookup"><span data-stu-id="8ea18-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="8ea18-124">Все примитивы, которые были бы прорисованы рядом с курсором, идентифицируются и сохраняются в буфере выбора.</span><span class="sxs-lookup"><span data-stu-id="8ea18-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="8ea18-125">Матрица, созданная с помощью **глупиккматрикс** , умножается на текущую матрицу так же, как если бы [**глмултматрикс**](glmultmatrix.md) вызывалась с созданной матрицей.</span><span class="sxs-lookup"><span data-stu-id="8ea18-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="8ea18-126">Вызовите [**гллоадидентити**](glloadidentity.md) , чтобы загрузить матрицу Identity в стек матрицы перспективы.</span><span class="sxs-lookup"><span data-stu-id="8ea18-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="8ea18-127">Вызовите **глупиккматрикс**.</span><span class="sxs-lookup"><span data-stu-id="8ea18-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="8ea18-128">Вызовите функцию (например, [**глуперспективе**](gluperspective.md)), чтобы умножить матрицу перспективы на матрицу подбора.</span><span class="sxs-lookup"><span data-stu-id="8ea18-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="8ea18-129">При использовании **глупиккматрикс** для выбора неравномерного рационального B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)) следует избегать отключения свойства нурбс, Glu \_ автоматической \_ загрузки \_ матрицы.</span><span class="sxs-lookup"><span data-stu-id="8ea18-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="8ea18-130">Если \_ \_ Матрица автоматической загрузки Glu не отключена \_ , то все отображаемые нурбс поверхности разделяются по-разному, с матрицей выбора, от ее деления до матрицы подбора.</span><span class="sxs-lookup"><span data-stu-id="8ea18-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="8ea18-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="8ea18-131">Examples</span></span>

<span data-ttu-id="8ea18-132">При отрисовке сцены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8ea18-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="8ea18-133">Следующий код выбирает часть окна просмотра:</span><span class="sxs-lookup"><span data-stu-id="8ea18-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="8ea18-134">Требования</span><span class="sxs-lookup"><span data-stu-id="8ea18-134">Requirements</span></span>



| <span data-ttu-id="8ea18-135">Требование</span><span class="sxs-lookup"><span data-stu-id="8ea18-135">Requirement</span></span> | <span data-ttu-id="8ea18-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8ea18-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea18-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ea18-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea18-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ea18-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ea18-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ea18-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea18-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ea18-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ea18-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ea18-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea18-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea18-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8ea18-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ea18-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ea18-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ea18-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ea18-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea18-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea18-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ea18-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea18-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ea18-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea18-148">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="8ea18-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8ea18-149">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="8ea18-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="8ea18-150">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="8ea18-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="8ea18-151">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="8ea18-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="8ea18-152">**глуперспективе**</span><span class="sxs-lookup"><span data-stu-id="8ea18-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





