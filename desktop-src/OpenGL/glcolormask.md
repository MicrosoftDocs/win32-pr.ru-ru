---
title: Функция Глколормаск (GL. h)
description: Функция Глколормаск включает и отключает запись цветовых компонентов буфера кадров.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- Функция Глколормаск OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891629"
---
# <a name="glcolormask-function"></a><span data-ttu-id="156bc-104">Функция Глколормаск</span><span class="sxs-lookup"><span data-stu-id="156bc-104">glColorMask function</span></span>

<span data-ttu-id="156bc-105">Функция **глколормаск** включает и отключает запись цветовых компонентов буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="156bc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="156bc-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="156bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="156bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156bc-108">*отмечен*</span><span class="sxs-lookup"><span data-stu-id="156bc-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-109">Укажите, может ли красный или не может быть записан в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="156bc-110">Значения по умолчанию — GL \_ true, что означает, что можно записать компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="156bc-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-111">*зеленого*</span><span class="sxs-lookup"><span data-stu-id="156bc-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-112">Укажите, может ли зеленый или не может быть записан в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="156bc-113">Значение по умолчанию — GL \_ true, указывающее, что можно записать компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="156bc-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-114">*выделен*</span><span class="sxs-lookup"><span data-stu-id="156bc-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-115">Укажите, может ли синий или не быть записан в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="156bc-116">Значение по умолчанию — GL \_ true, указывающее, что можно записать компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="156bc-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-117">*буквы*</span><span class="sxs-lookup"><span data-stu-id="156bc-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-118">Укажите, может ли альфа-канал быть записан в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="156bc-119">Значение по умолчанию — GL \_ true, указывающее, что можно записать компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="156bc-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156bc-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="156bc-120">Return value</span></span>

<span data-ttu-id="156bc-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="156bc-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="156bc-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="156bc-122">Error codes</span></span>

<span data-ttu-id="156bc-123">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="156bc-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="156bc-124">Имя</span><span class="sxs-lookup"><span data-stu-id="156bc-124">Name</span></span>                                                                                                  | <span data-ttu-id="156bc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="156bc-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="156bc-126"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="156bc-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="156bc-127">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="156bc-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="156bc-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="156bc-128">Remarks</span></span>

<span data-ttu-id="156bc-129">Функция **глколормаск** указывает, могут ли быть записаны отдельные компоненты цвета в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="156bc-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="156bc-130">Например, если *Red* имеет \_ значение «GL», то в красный компонент любого пикселя в любом из буферов цветов не вносится никаких изменений, независимо от попытки рисования.</span><span class="sxs-lookup"><span data-stu-id="156bc-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="156bc-131">Изменение отдельных битов компонентов невозможно контролировать.</span><span class="sxs-lookup"><span data-stu-id="156bc-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="156bc-132">Вместо этого изменения включаются или отключаются для всех компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="156bc-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="156bc-133">Следующие функции извлекают сведения, относящиеся к **глколормаск**:</span><span class="sxs-lookup"><span data-stu-id="156bc-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="156bc-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Color \_ вритемаск</span><span class="sxs-lookup"><span data-stu-id="156bc-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="156bc-135">**глжет** с аргументом \_ режим RGBA GL \_</span><span class="sxs-lookup"><span data-stu-id="156bc-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="156bc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="156bc-136">Requirements</span></span>



| <span data-ttu-id="156bc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="156bc-137">Requirement</span></span> | <span data-ttu-id="156bc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="156bc-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="156bc-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="156bc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="156bc-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="156bc-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="156bc-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="156bc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="156bc-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="156bc-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="156bc-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="156bc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="156bc-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="156bc-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="156bc-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="156bc-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="156bc-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="156bc-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="156bc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="156bc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="156bc-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="156bc-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="156bc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="156bc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156bc-150">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="156bc-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="156bc-151">**глколор**</span><span class="sxs-lookup"><span data-stu-id="156bc-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="156bc-152">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="156bc-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="156bc-153">**гленд**</span><span class="sxs-lookup"><span data-stu-id="156bc-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="156bc-154">**глжет**</span><span class="sxs-lookup"><span data-stu-id="156bc-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="156bc-155">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="156bc-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="156bc-156">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="156bc-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="156bc-157">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="156bc-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





