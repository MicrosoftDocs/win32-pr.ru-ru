---
title: Переменные состояния элемента управления буфера кадров
description: Переменные состояния элемента управления буфера кадров
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Переменные состояния элемента управления буфера кадров OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889308"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="9aedd-104">Переменные состояния элемента управления буфера кадров</span><span class="sxs-lookup"><span data-stu-id="9aedd-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="9aedd-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_буфер рисования \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="9aedd-106">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-106">Description:</span></span>     | <span data-ttu-id="9aedd-107">Буферы, выбранные для рисования</span><span class="sxs-lookup"><span data-stu-id="9aedd-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="9aedd-108">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-108">Attribute group:</span></span> | <span data-ttu-id="9aedd-109">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-109">color-buffer</span></span>                           |
| <span data-ttu-id="9aedd-110">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="9aedd-111">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-111">Get command:</span></span>     | [<span data-ttu-id="9aedd-112">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="9aedd-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_вритемаск индекса \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-114">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-114">Description:</span></span>     | <span data-ttu-id="9aedd-115">Цвет — индекс вритемаск</span><span class="sxs-lookup"><span data-stu-id="9aedd-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="9aedd-116">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-116">Attribute group:</span></span> | <span data-ttu-id="9aedd-117">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="9aedd-118">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-118">Initial value:</span></span>   | <span data-ttu-id="9aedd-119">1</span><span class="sxs-lookup"><span data-stu-id="9aedd-119">1's</span></span>                                                                              |
| <span data-ttu-id="9aedd-120">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-120">Get command:</span></span>     | [<span data-ttu-id="9aedd-121">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_вритемаск цвета \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-123">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-123">Description:</span></span>     | <span data-ttu-id="9aedd-124">Разрешение на запись цвета; R, G, B или A</span><span class="sxs-lookup"><span data-stu-id="9aedd-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="9aedd-125">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-125">Attribute group:</span></span> | <span data-ttu-id="9aedd-126">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="9aedd-127">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-127">Initial value:</span></span>   | <span data-ttu-id="9aedd-128">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="9aedd-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="9aedd-129">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-129">Get command:</span></span>     | [<span data-ttu-id="9aedd-130">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_вритемаск глубины \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-132">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-132">Description:</span></span>     | <span data-ttu-id="9aedd-133">Буфер глубины, включенный для записи</span><span class="sxs-lookup"><span data-stu-id="9aedd-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="9aedd-134">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-134">Attribute group:</span></span> | <span data-ttu-id="9aedd-135">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="9aedd-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="9aedd-136">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-136">Initial value:</span></span>   | <span data-ttu-id="9aedd-137">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="9aedd-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="9aedd-138">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-138">Get command:</span></span>     | [<span data-ttu-id="9aedd-139">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_вритемаск трафарета GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-141">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-141">Description:</span></span>     | <span data-ttu-id="9aedd-142">Набор элементов — буфер вритемаск</span><span class="sxs-lookup"><span data-stu-id="9aedd-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="9aedd-143">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-143">Attribute group:</span></span> | <span data-ttu-id="9aedd-144">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="9aedd-145">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-145">Initial value:</span></span>   | <span data-ttu-id="9aedd-146">1</span><span class="sxs-lookup"><span data-stu-id="9aedd-146">1's</span></span>                                                                              |
| <span data-ttu-id="9aedd-147">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-147">Get command:</span></span>     | [<span data-ttu-id="9aedd-148">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ ясное значение цвета GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-150">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-150">Description:</span></span>     | <span data-ttu-id="9aedd-151">Очистить значение буферного цвета (режим RGBA)</span><span class="sxs-lookup"><span data-stu-id="9aedd-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="9aedd-152">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-152">Attribute group:</span></span> | <span data-ttu-id="9aedd-153">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="9aedd-154">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-154">Initial value:</span></span>   | <span data-ttu-id="9aedd-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="9aedd-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="9aedd-156">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-156">Get command:</span></span>     | [<span data-ttu-id="9aedd-157">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ значение очистки индекса \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-159">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-159">Description:</span></span>     | <span data-ttu-id="9aedd-160">Очистить значение буфера цвета (режим индексирования цветов)</span><span class="sxs-lookup"><span data-stu-id="9aedd-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="9aedd-161">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-161">Attribute group:</span></span> | <span data-ttu-id="9aedd-162">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="9aedd-163">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-163">Initial value:</span></span>   | <span data-ttu-id="9aedd-164">0</span><span class="sxs-lookup"><span data-stu-id="9aedd-164">0</span></span>                                                                              |
| <span data-ttu-id="9aedd-165">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-165">Get command:</span></span>     | [<span data-ttu-id="9aedd-166">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ ясное значение глубины GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-168">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-168">Description:</span></span>     | <span data-ttu-id="9aedd-169">Значение очистки буфера глубины</span><span class="sxs-lookup"><span data-stu-id="9aedd-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="9aedd-170">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-170">Attribute group:</span></span> | <span data-ttu-id="9aedd-171">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="9aedd-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="9aedd-172">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-172">Initial value:</span></span>   | <span data-ttu-id="9aedd-173">1</span><span class="sxs-lookup"><span data-stu-id="9aedd-173">1</span></span>                                                                                |
| <span data-ttu-id="9aedd-174">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-174">Get command:</span></span>     | [<span data-ttu-id="9aedd-175">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ очистить значение ТРАФАРЕТа GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-177">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-177">Description:</span></span>     | <span data-ttu-id="9aedd-178">Набор элементов — очистить значение буфера</span><span class="sxs-lookup"><span data-stu-id="9aedd-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="9aedd-179">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-179">Attribute group:</span></span> | <span data-ttu-id="9aedd-180">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="9aedd-181">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-181">Initial value:</span></span>   | <span data-ttu-id="9aedd-182">0</span><span class="sxs-lookup"><span data-stu-id="9aedd-182">0</span></span>                                                                                |
| <span data-ttu-id="9aedd-183">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-183">Get command:</span></span>     | [<span data-ttu-id="9aedd-184">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="9aedd-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_ \_ ясное значение НАКОПЛЕНия GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="9aedd-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9aedd-186">Описание.</span><span class="sxs-lookup"><span data-stu-id="9aedd-186">Description:</span></span>     | <span data-ttu-id="9aedd-187">Накопление-значение очистки буфера</span><span class="sxs-lookup"><span data-stu-id="9aedd-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="9aedd-188">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="9aedd-188">Attribute group:</span></span> | <span data-ttu-id="9aedd-189">накопленный буфер</span><span class="sxs-lookup"><span data-stu-id="9aedd-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="9aedd-190">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="9aedd-190">Initial value:</span></span>   | <span data-ttu-id="9aedd-191">0</span><span class="sxs-lookup"><span data-stu-id="9aedd-191">0</span></span>                                                                              |
| <span data-ttu-id="9aedd-192">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="9aedd-192">Get command:</span></span>     | [<span data-ttu-id="9aedd-193">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="9aedd-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




