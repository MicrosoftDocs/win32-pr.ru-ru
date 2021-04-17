---
title: Функция Глвиевпорт (GL. h)
description: Функция Глвиевпорт задает окно просмотра.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- Функция Глвиевпорт OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567303"
---
# <a name="glviewport-function"></a><span data-ttu-id="20cea-104">Функция Глвиевпорт</span><span class="sxs-lookup"><span data-stu-id="20cea-104">glViewport function</span></span>

<span data-ttu-id="20cea-105">Функция **глвиевпорт** задает окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="20cea-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="20cea-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20cea-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="20cea-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20cea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20cea-108">*x*</span><span class="sxs-lookup"><span data-stu-id="20cea-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="20cea-109">Нижний левый угол прямоугольника окна просмотра в пикселях.</span><span class="sxs-lookup"><span data-stu-id="20cea-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="20cea-110">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="20cea-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="20cea-111">*y*</span><span class="sxs-lookup"><span data-stu-id="20cea-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="20cea-112">Нижний левый угол прямоугольника окна просмотра в пикселях.</span><span class="sxs-lookup"><span data-stu-id="20cea-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="20cea-113">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="20cea-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="20cea-114">*width*</span><span class="sxs-lookup"><span data-stu-id="20cea-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="20cea-115">Ширина окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="20cea-115">The width of the viewport.</span></span> <span data-ttu-id="20cea-116">При первом присоединении контекста OpenGL к окну *Ширина* и *Высота* устанавливаются в размеры этого окна.</span><span class="sxs-lookup"><span data-stu-id="20cea-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="20cea-117">*height*</span><span class="sxs-lookup"><span data-stu-id="20cea-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="20cea-118">Высота окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="20cea-118">The height of the viewport.</span></span> <span data-ttu-id="20cea-119">При первом присоединении контекста OpenGL к окну *Ширина* и *Высота* устанавливаются в размеры этого окна.</span><span class="sxs-lookup"><span data-stu-id="20cea-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20cea-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20cea-120">Return value</span></span>

<span data-ttu-id="20cea-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="20cea-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20cea-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="20cea-122">Error codes</span></span>

<span data-ttu-id="20cea-123">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="20cea-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="20cea-124">Имя</span><span class="sxs-lookup"><span data-stu-id="20cea-124">Name</span></span>                                                                                                  | <span data-ttu-id="20cea-125">Значение</span><span class="sxs-lookup"><span data-stu-id="20cea-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20cea-126"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="20cea-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="20cea-127">Либо *Ширина* , либо *Высота* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="20cea-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="20cea-128"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="20cea-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="20cea-129">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="20cea-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20cea-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20cea-130">Remarks</span></span>

<span data-ttu-id="20cea-131">Функция **глвиевпорт** указывает аффинное преобразование *x* и *y* из нормализованных координат устройства в координаты окна.</span><span class="sxs-lookup"><span data-stu-id="20cea-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="20cea-132">Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) должны быть нормализованными координатами устройства.</span><span class="sxs-lookup"><span data-stu-id="20cea-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="20cea-133">Затем вычисляются координаты окна (*x*<sub>w</sub> , *y*<sub>w</sub> ) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20cea-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Уравнение, показывающее вычисления координат окна.](images/view01.png)

<span data-ttu-id="20cea-135">Ширина и высота окна просмотра автоматически заносятся в диапазон, зависящий от реализации.</span><span class="sxs-lookup"><span data-stu-id="20cea-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="20cea-136">Запрос к этому диапазону осуществляется путем вызова **глжет** с аргументом GL \_ Max \_ окна просмотра \_ .</span><span class="sxs-lookup"><span data-stu-id="20cea-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="20cea-137">Следующие функции извлекают сведения, относящиеся к **глвиевпорт**:</span><span class="sxs-lookup"><span data-stu-id="20cea-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="20cea-138">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ окна просмотра аргументов GL</span><span class="sxs-lookup"><span data-stu-id="20cea-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="20cea-139">**глжет** с аргументом " \_ Максимальное \_ окно просмотра" \_</span><span class="sxs-lookup"><span data-stu-id="20cea-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="20cea-140">Требования</span><span class="sxs-lookup"><span data-stu-id="20cea-140">Requirements</span></span>



| <span data-ttu-id="20cea-141">Требование</span><span class="sxs-lookup"><span data-stu-id="20cea-141">Requirement</span></span> | <span data-ttu-id="20cea-142">Значение</span><span class="sxs-lookup"><span data-stu-id="20cea-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20cea-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20cea-143">Minimum supported client</span></span><br/> | <span data-ttu-id="20cea-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20cea-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20cea-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20cea-145">Minimum supported server</span></span><br/> | <span data-ttu-id="20cea-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20cea-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20cea-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20cea-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cea-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20cea-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20cea-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20cea-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="20cea-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20cea-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20cea-151">DLL</span><span class="sxs-lookup"><span data-stu-id="20cea-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20cea-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20cea-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cea-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20cea-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cea-154">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="20cea-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20cea-155">**глдепсранже**</span><span class="sxs-lookup"><span data-stu-id="20cea-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





