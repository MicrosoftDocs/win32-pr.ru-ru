---
title: Переменные состояния преобразования
description: Переменные состояния преобразования
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Переменные состояния преобразования OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908832"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="23dd9-104">Переменные состояния преобразования</span><span class="sxs-lookup"><span data-stu-id="23dd9-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="23dd9-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_ \_ Матрица моделвиев GL</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-106">Property</span></span> | <span data-ttu-id="23dd9-107">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="23dd9-108">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-108">Description:</span></span>     | <span data-ttu-id="23dd9-109">Стек матриц моделвиев</span><span class="sxs-lookup"><span data-stu-id="23dd9-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="23dd9-110">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="23dd9-111">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-111">Initial value:</span></span>   | <span data-ttu-id="23dd9-112">Идентификация</span><span class="sxs-lookup"><span data-stu-id="23dd9-112">Identity</span></span>                           |
| <span data-ttu-id="23dd9-113">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-113">Get command:</span></span>     | [<span data-ttu-id="23dd9-114">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="23dd9-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_матрица проекции GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-116">Property</span></span> | <span data-ttu-id="23dd9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-118">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-118">Description:</span></span>     | <span data-ttu-id="23dd9-119">Стек матриц проекции</span><span class="sxs-lookup"><span data-stu-id="23dd9-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="23dd9-120">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="23dd9-121">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-121">Initial value:</span></span>   | <span data-ttu-id="23dd9-122">Идентификация</span><span class="sxs-lookup"><span data-stu-id="23dd9-122">Identity</span></span>                                                                       |
| <span data-ttu-id="23dd9-123">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-123">Get command:</span></span>     | [<span data-ttu-id="23dd9-124">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_ \_ Матрица текстур GL</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-126">Property</span></span> | <span data-ttu-id="23dd9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-128">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-128">Description:</span></span>     | <span data-ttu-id="23dd9-129">Стек матриц текстуры</span><span class="sxs-lookup"><span data-stu-id="23dd9-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="23dd9-130">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="23dd9-131">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-131">Initial value:</span></span>   | <span data-ttu-id="23dd9-132">Идентификация</span><span class="sxs-lookup"><span data-stu-id="23dd9-132">Identity</span></span>                                                                       |
| <span data-ttu-id="23dd9-133">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-133">Get command:</span></span>     | [<span data-ttu-id="23dd9-134">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_окно просмотра GL</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-136">Property</span></span> | <span data-ttu-id="23dd9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-138">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-138">Description:</span></span>     | <span data-ttu-id="23dd9-139">Источник и экстент окна просмотра</span><span class="sxs-lookup"><span data-stu-id="23dd9-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="23dd9-140">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-140">Attribute group:</span></span> | <span data-ttu-id="23dd9-141">окно просмотра</span><span class="sxs-lookup"><span data-stu-id="23dd9-141">viewport</span></span>                                                                         |
| <span data-ttu-id="23dd9-142">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="23dd9-143">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-143">Get command:</span></span>     | [<span data-ttu-id="23dd9-144">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_диапазон глубины \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-146">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-146">Property</span></span> | <span data-ttu-id="23dd9-147">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-148">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-148">Description:</span></span>     | <span data-ttu-id="23dd9-149">Диапазон глубины почти и далеко</span><span class="sxs-lookup"><span data-stu-id="23dd9-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="23dd9-150">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-150">Attribute group:</span></span> | <span data-ttu-id="23dd9-151">окно просмотра</span><span class="sxs-lookup"><span data-stu-id="23dd9-151">viewport</span></span>                                                                       |
| <span data-ttu-id="23dd9-152">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-152">Initial value:</span></span>   | <span data-ttu-id="23dd9-153">0, 1</span><span class="sxs-lookup"><span data-stu-id="23dd9-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="23dd9-154">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-154">Get command:</span></span>     | [<span data-ttu-id="23dd9-155">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_ \_ глубина стека моделвиев GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-157">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-157">Property</span></span> | <span data-ttu-id="23dd9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-159">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-159">Description:</span></span>     | <span data-ttu-id="23dd9-160">Указатель стека матрицы моделвиев</span><span class="sxs-lookup"><span data-stu-id="23dd9-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="23dd9-161">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="23dd9-162">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-162">Initial value:</span></span>   | <span data-ttu-id="23dd9-163">1</span><span class="sxs-lookup"><span data-stu-id="23dd9-163">1</span></span>                                                                                |
| <span data-ttu-id="23dd9-164">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-164">Get command:</span></span>     | [<span data-ttu-id="23dd9-165">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ глубина стека ПРОЕЦИРОВАНия GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-167">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-167">Property</span></span> | <span data-ttu-id="23dd9-168">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-169">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-169">Description:</span></span>     | <span data-ttu-id="23dd9-170">Указатель стека матрицы проекции</span><span class="sxs-lookup"><span data-stu-id="23dd9-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="23dd9-171">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="23dd9-172">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-172">Initial value:</span></span>   | <span data-ttu-id="23dd9-173">1</span><span class="sxs-lookup"><span data-stu-id="23dd9-173">1</span></span>                                                                                |
| <span data-ttu-id="23dd9-174">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-174">Get command:</span></span>     | [<span data-ttu-id="23dd9-175">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_ \_ глубина стека текстур GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-177">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-177">Property</span></span> | <span data-ttu-id="23dd9-178">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-179">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-179">Description:</span></span>     | <span data-ttu-id="23dd9-180">Указатель стека матрицы текстуры</span><span class="sxs-lookup"><span data-stu-id="23dd9-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="23dd9-181">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="23dd9-182">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-182">Initial value:</span></span>   | <span data-ttu-id="23dd9-183">1</span><span class="sxs-lookup"><span data-stu-id="23dd9-183">1</span></span>                                                                                |
| <span data-ttu-id="23dd9-184">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-184">Get command:</span></span>     | [<span data-ttu-id="23dd9-185">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_режим матрицы GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-187">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-187">Property</span></span> | <span data-ttu-id="23dd9-188">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23dd9-189">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-189">Description:</span></span>     | <span data-ttu-id="23dd9-190">Текущий режим матрицы</span><span class="sxs-lookup"><span data-stu-id="23dd9-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="23dd9-191">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-191">Attribute group:</span></span> | <span data-ttu-id="23dd9-192">преобразование</span><span class="sxs-lookup"><span data-stu-id="23dd9-192">transform</span></span>                                                                        |
| <span data-ttu-id="23dd9-193">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-193">Initial value:</span></span>   | <span data-ttu-id="23dd9-194">\_МОДЕЛВИЕВ GL</span><span class="sxs-lookup"><span data-stu-id="23dd9-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="23dd9-195">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-195">Get command:</span></span>     | [<span data-ttu-id="23dd9-196">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="23dd9-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="23dd9-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_нормализация GL</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-198">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-198">Property</span></span> | <span data-ttu-id="23dd9-199">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="23dd9-200">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-200">Description:</span></span>     | <span data-ttu-id="23dd9-201">Текущее нормальное нормализация</span><span class="sxs-lookup"><span data-stu-id="23dd9-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="23dd9-202">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-202">Attribute group:</span></span> | <span data-ttu-id="23dd9-203">Преобразование или включение</span><span class="sxs-lookup"><span data-stu-id="23dd9-203">transform/enable</span></span>                    |
| <span data-ttu-id="23dd9-204">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-204">Initial value:</span></span>   | <span data-ttu-id="23dd9-205">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="23dd9-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="23dd9-206">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-206">Get command:</span></span>     | [<span data-ttu-id="23dd9-207">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="23dd9-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="23dd9-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>В \_ главной \_ плоскости Clip, *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-209">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-209">Property</span></span> | <span data-ttu-id="23dd9-210">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="23dd9-211">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-211">Description:</span></span>     | <span data-ttu-id="23dd9-212">Коэффициенты для пользовательской плоскости вырезки</span><span class="sxs-lookup"><span data-stu-id="23dd9-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="23dd9-213">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-213">Attribute group:</span></span> | <span data-ttu-id="23dd9-214">преобразование</span><span class="sxs-lookup"><span data-stu-id="23dd9-214">transform</span></span>                                |
| <span data-ttu-id="23dd9-215">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-215">Initial value:</span></span>   | <span data-ttu-id="23dd9-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="23dd9-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="23dd9-217">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-217">Get command:</span></span>     | [<span data-ttu-id="23dd9-218">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="23dd9-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="23dd9-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>В \_ главной \_ плоскости Clip, *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="23dd9-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="23dd9-220">Свойство</span><span class="sxs-lookup"><span data-stu-id="23dd9-220">Property</span></span> | <span data-ttu-id="23dd9-221">Значение</span><span class="sxs-lookup"><span data-stu-id="23dd9-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="23dd9-222">Описание.</span><span class="sxs-lookup"><span data-stu-id="23dd9-222">Description:</span></span>     | <span data-ttu-id="23dd9-223">*i* . включена плоскость обрезки пользователя</span><span class="sxs-lookup"><span data-stu-id="23dd9-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="23dd9-224">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="23dd9-224">Attribute group:</span></span> | <span data-ttu-id="23dd9-225">Преобразование или включение</span><span class="sxs-lookup"><span data-stu-id="23dd9-225">transform/enable</span></span>                   |
| <span data-ttu-id="23dd9-226">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="23dd9-226">Initial value:</span></span>   | <span data-ttu-id="23dd9-227">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="23dd9-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="23dd9-228">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="23dd9-228">Get command:</span></span>     | [<span data-ttu-id="23dd9-229">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="23dd9-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




