---
title: Функция Глкалллист (GL. h)
description: Функция Глкалллист выполняет список отображений.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- Функция Глкалллист OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136199"
---
# <a name="glcalllist-function"></a><span data-ttu-id="2b4d6-104">Функция Глкалллист</span><span class="sxs-lookup"><span data-stu-id="2b4d6-104">glCallList function</span></span>

<span data-ttu-id="2b4d6-105">Функция **глкалллист** выполняет список отображений.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4d6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b4d6-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="2b4d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b4d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b4d6-108">*list*</span><span class="sxs-lookup"><span data-stu-id="2b4d6-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="2b4d6-109">Целочисленное имя выполняемого списка отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b4d6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b4d6-110">Return value</span></span>

<span data-ttu-id="2b4d6-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b4d6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b4d6-112">Remarks</span></span>

<span data-ttu-id="2b4d6-113">Вызов функции **глкалллист** начинает выполнение именованного списка экранов.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="2b4d6-114">Функции, сохраненные в списке отображений, выполняются по порядку, как если бы они были вызваны без использования списка вывода.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="2b4d6-115">Если *список* не был определен как список вывода, **глкалллист** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="2b4d6-116">Функция **глкалллист** может отображаться в списке отображения.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="2b4d6-117">Чтобы избежать возможности бесконечной рекурсии, полученной в результате вызова друг друга из списков вывода, на уровне вложенности списков отображаемых данных во время выполнения списка отображений размещается ограничение.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="2b4d6-118">Это ограничение по крайней мере 64, но зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="2b4d6-119">Состояние OpenGL не сохраняется и не восстанавливается в результате вызова **глкалллист**.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="2b4d6-120">Поэтому изменения, внесенные в состояние OpenGL во время выполнения списка отображения, остаются после завершения выполнения списка отображения.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="2b4d6-121">Чтобы сохранить состояние OpenGL в вызовах **глкалллист** , используйте [**глпушаттриб**](glpushattrib.md), [**глпопаттриб**](glpopattrib.md), [**глпушматрикс**](glpushmatrix.md)и [**глпопматрикс**](glpopmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d6-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="2b4d6-122">Вы можете выполнять списки вывода между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md), если в списке отображаются только те функции, которые разрешены в этом интервале.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="2b4d6-123">Следующие функции извлекают сведения, относящиеся к **глкалллист**:</span><span class="sxs-lookup"><span data-stu-id="2b4d6-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="2b4d6-124">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ , \_ вложенным в параметр GL Max List \_</span><span class="sxs-lookup"><span data-stu-id="2b4d6-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="2b4d6-125">**глислист**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="2b4d6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2b4d6-126">Requirements</span></span>



| <span data-ttu-id="2b4d6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2b4d6-127">Requirement</span></span> | <span data-ttu-id="2b4d6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2b4d6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4d6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b4d6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b4d6-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b4d6-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b4d6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b4d6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b4d6-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b4d6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b4d6-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b4d6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b4d6-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b4d6-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2b4d6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b4d6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b4d6-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b4d6-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b4d6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2b4d6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b4d6-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b4d6-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b4d6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b4d6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4d6-140">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-141">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-142">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-143">**гленд**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-144">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-145">**глжет**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-146">**глислист**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-147">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-148">**глпопаттриб**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-149">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-150">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="2b4d6-151">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="2b4d6-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





