---
title: Функция ГлсЦиссор (GL. h)
description: Функция ГлсЦиссор определяет прямоугольный прямоугольник.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- Функция ГлсЦиссор OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493023"
---
# <a name="glscissor-function"></a><span data-ttu-id="2c52e-104">Функция ГлсЦиссор</span><span class="sxs-lookup"><span data-stu-id="2c52e-104">glScissor function</span></span>

<span data-ttu-id="2c52e-105">Функция **глсЦиссор** определяет прямоугольный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="2c52e-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c52e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c52e-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="2c52e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c52e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c52e-108">*x*</span><span class="sxs-lookup"><span data-stu-id="2c52e-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="2c52e-109">Координата x (вертикальная ось) для левого нижнего угла прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="2c52e-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="2c52e-110">*y*</span><span class="sxs-lookup"><span data-stu-id="2c52e-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="2c52e-111">Координата y (горизонтальная ось) для левого нижнего угла прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="2c52e-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="2c52e-112">Вместе, x и y указывают левый нижний угол прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="2c52e-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="2c52e-113">Изначально (0, 0).</span><span class="sxs-lookup"><span data-stu-id="2c52e-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="2c52e-114">*width*</span><span class="sxs-lookup"><span data-stu-id="2c52e-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="2c52e-115">Ширина прямоугольной рамки.</span><span class="sxs-lookup"><span data-stu-id="2c52e-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="2c52e-116">*height*</span><span class="sxs-lookup"><span data-stu-id="2c52e-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="2c52e-117">Высота прямоугольной рамки.</span><span class="sxs-lookup"><span data-stu-id="2c52e-117">The height of the scissor box.</span></span> <span data-ttu-id="2c52e-118">При *первом* присоединении контекста OpenGL к окну *Ширина* и *Высота* устанавливаются в размеры этого окна.</span><span class="sxs-lookup"><span data-stu-id="2c52e-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c52e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c52e-119">Return value</span></span>

<span data-ttu-id="2c52e-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2c52e-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c52e-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2c52e-121">Error codes</span></span>

<span data-ttu-id="2c52e-122">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2c52e-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2c52e-123">Имя</span><span class="sxs-lookup"><span data-stu-id="2c52e-123">Name</span></span>                                                                                                  | <span data-ttu-id="2c52e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2c52e-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c52e-125"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c52e-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2c52e-126">Либо *Ширина* , либо *Высота* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="2c52e-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="2c52e-127"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c52e-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2c52e-128">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2c52e-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c52e-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c52e-129">Remarks</span></span>

<span data-ttu-id="2c52e-130">Функция **глсЦиссор** определяет прямоугольник, называемый прямоугольной рамкой, в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="2c52e-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="2c52e-131">Первые два параметра, *x* и *y*, указывают нижний левый угол бокса.</span><span class="sxs-lookup"><span data-stu-id="2c52e-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="2c52e-132">Параметры *Width* и *Height* определяют ширину и высоту поля.</span><span class="sxs-lookup"><span data-stu-id="2c52e-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="2c52e-133">Ножницы включаются и отключаются с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом "GL- \_ ножницный \_ Тест".</span><span class="sxs-lookup"><span data-stu-id="2c52e-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="2c52e-134">Пока ножницы включены, команды рисования могут изменять только пиксели, находящиеся внутри прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="2c52e-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="2c52e-135">Координаты окон имеют целочисленные значения в общих углах буфера кадров пикселей, поэтому **глсЦиссор**(0, 0, 1, 1) позволяет изменять только нижний левый пиксел в окне, а **глсЦиссор**(0, 0, 0, 0) запрещает изменение во всех пикселях окна.</span><span class="sxs-lookup"><span data-stu-id="2c52e-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="2c52e-136">Если ножницы отключены, то это так, как если бы прямоугольная рамка включала все окно.</span><span class="sxs-lookup"><span data-stu-id="2c52e-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="2c52e-137">Следующие функции извлекают сведения, относящиеся к **глсЦиссор**:</span><span class="sxs-lookup"><span data-stu-id="2c52e-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="2c52e-138">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ "прямоугольная распашная \_ "</span><span class="sxs-lookup"><span data-stu-id="2c52e-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="2c52e-139">[**глисенаблед**](glisenabled.md) с аргументом, выполнив \_ \_ пробное вырезание</span><span class="sxs-lookup"><span data-stu-id="2c52e-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="2c52e-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2c52e-140">Requirements</span></span>



| <span data-ttu-id="2c52e-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2c52e-141">Requirement</span></span> | <span data-ttu-id="2c52e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2c52e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c52e-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c52e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2c52e-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c52e-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c52e-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c52e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2c52e-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c52e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c52e-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c52e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c52e-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c52e-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c52e-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c52e-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c52e-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c52e-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c52e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2c52e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c52e-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c52e-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c52e-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c52e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c52e-154">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="2c52e-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2c52e-155">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="2c52e-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="2c52e-156">**гленд**</span><span class="sxs-lookup"><span data-stu-id="2c52e-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2c52e-157">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="2c52e-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="2c52e-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="2c52e-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





