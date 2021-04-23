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
ms.openlocfilehash: 998414271956de44710e9ef456722d7499adb862
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910082"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="a2856-104">Переменные состояния элемента управления буфера кадров</span><span class="sxs-lookup"><span data-stu-id="a2856-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="a2856-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_буфер рисования \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

| <span data-ttu-id="a2856-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-106">Property</span></span> | <span data-ttu-id="a2856-107">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-107">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="a2856-108">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-108">Description:</span></span>     | <span data-ttu-id="a2856-109">Буферы, выбранные для рисования</span><span class="sxs-lookup"><span data-stu-id="a2856-109">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="a2856-110">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-110">Attribute group:</span></span> | <span data-ttu-id="a2856-111">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-111">color-buffer</span></span>                           |
| <span data-ttu-id="a2856-112">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-112">Initial value:</span></span>   |                                        |
| <span data-ttu-id="a2856-113">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-113">Get command:</span></span>     | [<span data-ttu-id="a2856-114">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="a2856-114">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="a2856-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_вритемаск индекса \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="a2856-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-116">Property</span></span> | <span data-ttu-id="a2856-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-117">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-118">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-118">Description:</span></span>     | <span data-ttu-id="a2856-119">Цвет — индекс вритемаск</span><span class="sxs-lookup"><span data-stu-id="a2856-119">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="a2856-120">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-120">Attribute group:</span></span> | <span data-ttu-id="a2856-121">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-121">color-buffer</span></span>                                                                     |
| <span data-ttu-id="a2856-122">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-122">Initial value:</span></span>   | <span data-ttu-id="a2856-123">1</span><span class="sxs-lookup"><span data-stu-id="a2856-123">1's</span></span>                                                                              |
| <span data-ttu-id="a2856-124">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-124">Get command:</span></span>     | [<span data-ttu-id="a2856-125">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="a2856-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_вритемаск цвета \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="a2856-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-127">Property</span></span> | <span data-ttu-id="a2856-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-128">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-129">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-129">Description:</span></span>     | <span data-ttu-id="a2856-130">Разрешение на запись цвета; R, G, B или A</span><span class="sxs-lookup"><span data-stu-id="a2856-130">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="a2856-131">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-131">Attribute group:</span></span> | <span data-ttu-id="a2856-132">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-132">color-buffer</span></span>                                                                     |
| <span data-ttu-id="a2856-133">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-133">Initial value:</span></span>   | <span data-ttu-id="a2856-134">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="a2856-134">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="a2856-135">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-135">Get command:</span></span>     | [<span data-ttu-id="a2856-136">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="a2856-136">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_вритемаск глубины \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="a2856-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-138">Property</span></span> | <span data-ttu-id="a2856-139">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-140">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-140">Description:</span></span>     | <span data-ttu-id="a2856-141">Буфер глубины, включенный для записи</span><span class="sxs-lookup"><span data-stu-id="a2856-141">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="a2856-142">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-142">Attribute group:</span></span> | <span data-ttu-id="a2856-143">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="a2856-143">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="a2856-144">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-144">Initial value:</span></span>   | <span data-ttu-id="a2856-145">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="a2856-145">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="a2856-146">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-146">Get command:</span></span>     | [<span data-ttu-id="a2856-147">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="a2856-147">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_вритемаск трафарета GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="a2856-149">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-149">Property</span></span> | <span data-ttu-id="a2856-150">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-151">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-151">Description:</span></span>     | <span data-ttu-id="a2856-152">Набор элементов — буфер вритемаск</span><span class="sxs-lookup"><span data-stu-id="a2856-152">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="a2856-153">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-153">Attribute group:</span></span> | <span data-ttu-id="a2856-154">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="a2856-155">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-155">Initial value:</span></span>   | <span data-ttu-id="a2856-156">1</span><span class="sxs-lookup"><span data-stu-id="a2856-156">1's</span></span>                                                                              |
| <span data-ttu-id="a2856-157">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-157">Get command:</span></span>     | [<span data-ttu-id="a2856-158">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="a2856-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ ясное значение цвета GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="a2856-160">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-160">Property</span></span> | <span data-ttu-id="a2856-161">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-161">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-162">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-162">Description:</span></span>     | <span data-ttu-id="a2856-163">Очистить значение буферного цвета (режим RGBA)</span><span class="sxs-lookup"><span data-stu-id="a2856-163">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="a2856-164">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-164">Attribute group:</span></span> | <span data-ttu-id="a2856-165">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-165">color-buffer</span></span>                                                                   |
| <span data-ttu-id="a2856-166">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-166">Initial value:</span></span>   | <span data-ttu-id="a2856-167">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="a2856-167">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="a2856-168">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-168">Get command:</span></span>     | [<span data-ttu-id="a2856-169">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="a2856-169">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ значение очистки индекса \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="a2856-171">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-171">Property</span></span> | <span data-ttu-id="a2856-172">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-172">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-173">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-173">Description:</span></span>     | <span data-ttu-id="a2856-174">Очистить значение буфера цвета (режим индексирования цветов)</span><span class="sxs-lookup"><span data-stu-id="a2856-174">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="a2856-175">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-175">Attribute group:</span></span> | <span data-ttu-id="a2856-176">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-176">color-buffer</span></span>                                                                   |
| <span data-ttu-id="a2856-177">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-177">Initial value:</span></span>   | <span data-ttu-id="a2856-178">0</span><span class="sxs-lookup"><span data-stu-id="a2856-178">0</span></span>                                                                              |
| <span data-ttu-id="a2856-179">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-179">Get command:</span></span>     | [<span data-ttu-id="a2856-180">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="a2856-180">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ ясное значение глубины GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="a2856-182">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-182">Property</span></span> | <span data-ttu-id="a2856-183">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-184">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-184">Description:</span></span>     | <span data-ttu-id="a2856-185">Значение очистки буфера глубины</span><span class="sxs-lookup"><span data-stu-id="a2856-185">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="a2856-186">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-186">Attribute group:</span></span> | <span data-ttu-id="a2856-187">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="a2856-187">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="a2856-188">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-188">Initial value:</span></span>   | <span data-ttu-id="a2856-189">1</span><span class="sxs-lookup"><span data-stu-id="a2856-189">1</span></span>                                                                                |
| <span data-ttu-id="a2856-190">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-190">Get command:</span></span>     | [<span data-ttu-id="a2856-191">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="a2856-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ очистить значение ТРАФАРЕТа GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="a2856-193">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-193">Property</span></span> | <span data-ttu-id="a2856-194">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-195">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-195">Description:</span></span>     | <span data-ttu-id="a2856-196">Набор элементов — очистить значение буфера</span><span class="sxs-lookup"><span data-stu-id="a2856-196">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="a2856-197">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-197">Attribute group:</span></span> | <span data-ttu-id="a2856-198">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="a2856-199">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-199">Initial value:</span></span>   | <span data-ttu-id="a2856-200">0</span><span class="sxs-lookup"><span data-stu-id="a2856-200">0</span></span>                                                                                |
| <span data-ttu-id="a2856-201">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-201">Get command:</span></span>     | [<span data-ttu-id="a2856-202">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="a2856-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a2856-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_ \_ ясное значение НАКОПЛЕНия GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a2856-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="a2856-204">Свойство</span><span class="sxs-lookup"><span data-stu-id="a2856-204">Property</span></span> | <span data-ttu-id="a2856-205">Значение</span><span class="sxs-lookup"><span data-stu-id="a2856-205">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2856-206">Описание.</span><span class="sxs-lookup"><span data-stu-id="a2856-206">Description:</span></span>     | <span data-ttu-id="a2856-207">Накопление-значение очистки буфера</span><span class="sxs-lookup"><span data-stu-id="a2856-207">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="a2856-208">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="a2856-208">Attribute group:</span></span> | <span data-ttu-id="a2856-209">накопленный буфер</span><span class="sxs-lookup"><span data-stu-id="a2856-209">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="a2856-210">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="a2856-210">Initial value:</span></span>   | <span data-ttu-id="a2856-211">0</span><span class="sxs-lookup"><span data-stu-id="a2856-211">0</span></span>                                                                              |
| <span data-ttu-id="a2856-212">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="a2856-212">Get command:</span></span>     | [<span data-ttu-id="a2856-213">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="a2856-213">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




