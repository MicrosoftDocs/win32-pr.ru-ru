---
title: Текстурирование переменных состояния
description: Текстурирование переменных состояния
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Текстурирование переменных состояния OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff468c701100cc598a519ed3aa290913016a559e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908652"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="bd5bf-104">Текстурирование переменных состояния</span><span class="sxs-lookup"><span data-stu-id="bd5bf-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="bd5bf-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Текстура GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-106">Property</span></span> | <span data-ttu-id="bd5bf-107">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-107">Value</span></span> |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="bd5bf-108">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-108">Description:</span></span>     | <span data-ttu-id="bd5bf-109">True, если включено текстурирование *x* -d (*x* — 1-D или 2-d)</span><span class="sxs-lookup"><span data-stu-id="bd5bf-109">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="bd5bf-110">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-110">Attribute group:</span></span> | <span data-ttu-id="bd5bf-111">Текстура и включение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-111">texture/enable</span></span>                                        |
| <span data-ttu-id="bd5bf-112">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-112">Initial value:</span></span>   | <span data-ttu-id="bd5bf-113">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="bd5bf-113">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="bd5bf-114">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-114">Get command:</span></span>     | [<span data-ttu-id="bd5bf-115">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-115">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="bd5bf-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_текстура GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-117">Property</span></span> | <span data-ttu-id="bd5bf-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-118">Value</span></span> |
|------------------|----------------------------------------------|
| <span data-ttu-id="bd5bf-119">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-119">Description:</span></span>     | <span data-ttu-id="bd5bf-120">изображение текстуры *x* -D на *уровне детализации*</span><span class="sxs-lookup"><span data-stu-id="bd5bf-120">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="bd5bf-121">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-121">Attribute group:</span></span> |                                              |
| <span data-ttu-id="bd5bf-122">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-122">Initial value:</span></span>   |                                              |
| <span data-ttu-id="bd5bf-123">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-123">Get command:</span></span>     | [<span data-ttu-id="bd5bf-124">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-124">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="bd5bf-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_Ширина текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-126">Property</span></span> | <span data-ttu-id="bd5bf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-127">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="bd5bf-128">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-128">Description:</span></span>     | <span data-ttu-id="bd5bf-129">ширина *изображения текстуры* *x* -D</span><span class="sxs-lookup"><span data-stu-id="bd5bf-129">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="bd5bf-130">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-130">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="bd5bf-131">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-131">Initial value:</span></span>   | <span data-ttu-id="bd5bf-132">0</span><span class="sxs-lookup"><span data-stu-id="bd5bf-132">0</span></span>                                                        |
| <span data-ttu-id="bd5bf-133">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-133">Get command:</span></span>     | [<span data-ttu-id="bd5bf-134">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-134">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="bd5bf-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_Высота текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-136">Property</span></span> | <span data-ttu-id="bd5bf-137">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-137">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="bd5bf-138">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-138">Description:</span></span>     | <span data-ttu-id="bd5bf-139">Высота *изображения текстуры* *x* -D</span><span class="sxs-lookup"><span data-stu-id="bd5bf-139">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="bd5bf-140">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="bd5bf-141">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-141">Initial value:</span></span>   | <span data-ttu-id="bd5bf-142">0</span><span class="sxs-lookup"><span data-stu-id="bd5bf-142">0</span></span>                                                        |
| <span data-ttu-id="bd5bf-143">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-143">Get command:</span></span>     | [<span data-ttu-id="bd5bf-144">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="bd5bf-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_граница текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-146">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-146">Property</span></span> | <span data-ttu-id="bd5bf-147">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-147">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="bd5bf-148">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-148">Description:</span></span>     | <span data-ttu-id="bd5bf-149">*рисунок текстуры* *x* -D граница</span><span class="sxs-lookup"><span data-stu-id="bd5bf-149">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="bd5bf-150">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-150">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="bd5bf-151">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-151">Initial value:</span></span>   | <span data-ttu-id="bd5bf-152">0</span><span class="sxs-lookup"><span data-stu-id="bd5bf-152">0</span></span>                                                        |
| <span data-ttu-id="bd5bf-153">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-153">Get command:</span></span>     | [<span data-ttu-id="bd5bf-154">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-154">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="bd5bf-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_компоненты текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-156">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-156">Property</span></span> | <span data-ttu-id="bd5bf-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-157">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="bd5bf-158">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-158">Description:</span></span>     | <span data-ttu-id="bd5bf-159">Компоненты изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="bd5bf-159">Texture image components</span></span>                                 |
| <span data-ttu-id="bd5bf-160">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-160">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="bd5bf-161">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-161">Initial value:</span></span>   | <span data-ttu-id="bd5bf-162">1</span><span class="sxs-lookup"><span data-stu-id="bd5bf-162">1</span></span>                                                        |
| <span data-ttu-id="bd5bf-163">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-163">Get command:</span></span>     | [<span data-ttu-id="bd5bf-164">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-164">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="bd5bf-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_ \_ Цвет границы текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-166">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-166">Property</span></span> | <span data-ttu-id="bd5bf-167">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-167">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="bd5bf-168">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-168">Description:</span></span>     | <span data-ttu-id="bd5bf-169">Цвет границы текстуры</span><span class="sxs-lookup"><span data-stu-id="bd5bf-169">Texture border color</span></span>                           |
| <span data-ttu-id="bd5bf-170">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-170">Attribute group:</span></span> | <span data-ttu-id="bd5bf-171">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-171">texture</span></span>                                        |
| <span data-ttu-id="bd5bf-172">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-172">Initial value:</span></span>   | <span data-ttu-id="bd5bf-173">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="bd5bf-173">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="bd5bf-174">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-174">Get command:</span></span>     | [<span data-ttu-id="bd5bf-175">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-175">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="bd5bf-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ Фильтр min текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-177">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-177">Property</span></span> | <span data-ttu-id="bd5bf-178">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-178">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="bd5bf-179">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-179">Description:</span></span>     | <span data-ttu-id="bd5bf-180">Функция минификации текстуры</span><span class="sxs-lookup"><span data-stu-id="bd5bf-180">Texture minification function</span></span>                  |
| <span data-ttu-id="bd5bf-181">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-181">Attribute group:</span></span> | <span data-ttu-id="bd5bf-182">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-182">texture</span></span>                                        |
| <span data-ttu-id="bd5bf-183">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-183">Initial value:</span></span>   | <span data-ttu-id="bd5bf-184">\_Ближайшая \_ Линейная MIPMAPа GL \_</span><span class="sxs-lookup"><span data-stu-id="bd5bf-184">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="bd5bf-185">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-185">Get command:</span></span>     | [<span data-ttu-id="bd5bf-186">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-186">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="bd5bf-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ Фильтр MAG текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-188">Property</span></span> | <span data-ttu-id="bd5bf-189">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-189">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="bd5bf-190">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-190">Description:</span></span>     | <span data-ttu-id="bd5bf-191">Функция увеличения текстуры</span><span class="sxs-lookup"><span data-stu-id="bd5bf-191">Texture magnification function</span></span>                 |
| <span data-ttu-id="bd5bf-192">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-192">Attribute group:</span></span> | <span data-ttu-id="bd5bf-193">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-193">texture</span></span>                                        |
| <span data-ttu-id="bd5bf-194">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-194">Initial value:</span></span>   | <span data-ttu-id="bd5bf-195">Линейная (GL) \_</span><span class="sxs-lookup"><span data-stu-id="bd5bf-195">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="bd5bf-196">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-196">Get command:</span></span>     | [<span data-ttu-id="bd5bf-197">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-197">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="bd5bf-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>\_Заносится текстура GL \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-199">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-199">Property</span></span> | <span data-ttu-id="bd5bf-200">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-200">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="bd5bf-201">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-201">Description:</span></span>     | <span data-ttu-id="bd5bf-202">Режим переноса текстур (*x* — S или T)</span><span class="sxs-lookup"><span data-stu-id="bd5bf-202">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="bd5bf-203">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-203">Attribute group:</span></span> | <span data-ttu-id="bd5bf-204">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-204">texture</span></span>                                        |
| <span data-ttu-id="bd5bf-205">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-205">Initial value:</span></span>   | <span data-ttu-id="bd5bf-206">\_повторение GL</span><span class="sxs-lookup"><span data-stu-id="bd5bf-206">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="bd5bf-207">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-207">Get command:</span></span>     | [<span data-ttu-id="bd5bf-208">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-208">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="bd5bf-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_режим текстуры \_ в главной модели \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-210">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-210">Property</span></span> | <span data-ttu-id="bd5bf-211">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-211">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="bd5bf-212">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-212">Description:</span></span>     | <span data-ttu-id="bd5bf-213">Функция текстуры приложения</span><span class="sxs-lookup"><span data-stu-id="bd5bf-213">Texture application function</span></span>         |
| <span data-ttu-id="bd5bf-214">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-214">Attribute group:</span></span> | <span data-ttu-id="bd5bf-215">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-215">texture</span></span>                              |
| <span data-ttu-id="bd5bf-216">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-216">Initial value:</span></span>   | <span data-ttu-id="bd5bf-217">GL для \_ модуляции</span><span class="sxs-lookup"><span data-stu-id="bd5bf-217">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="bd5bf-218">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-218">Get command:</span></span>     | [<span data-ttu-id="bd5bf-219">**глжеттексенвив**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-219">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="bd5bf-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_Цвет текстуры в главной \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-221">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-221">Property</span></span> | <span data-ttu-id="bd5bf-222">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-222">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="bd5bf-223">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-223">Description:</span></span>     | <span data-ttu-id="bd5bf-224">Цвет текстурной среды</span><span class="sxs-lookup"><span data-stu-id="bd5bf-224">Texture environment color</span></span>            |
| <span data-ttu-id="bd5bf-225">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-225">Attribute group:</span></span> | <span data-ttu-id="bd5bf-226">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-226">texture</span></span>                              |
| <span data-ttu-id="bd5bf-227">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-227">Initial value:</span></span>   | <span data-ttu-id="bd5bf-228">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="bd5bf-228">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="bd5bf-229">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-229">Get command:</span></span>     | [<span data-ttu-id="bd5bf-230">**глжеттексенвфв**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-230">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="bd5bf-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>\_Gen текстура GL \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-232">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-232">Property</span></span> | <span data-ttu-id="bd5bf-233">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-233">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="bd5bf-234">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-234">Description:</span></span>     | <span data-ttu-id="bd5bf-235">Тексжен включен (*x* — S, T, R или Q)</span><span class="sxs-lookup"><span data-stu-id="bd5bf-235">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="bd5bf-236">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-236">Attribute group:</span></span> | <span data-ttu-id="bd5bf-237">Текстура и включение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-237">texture/enable</span></span>                           |
| <span data-ttu-id="bd5bf-238">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-238">Initial value:</span></span>   | <span data-ttu-id="bd5bf-239">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="bd5bf-239">GL\_FALSE</span></span>                                |
| <span data-ttu-id="bd5bf-240">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-240">Get command:</span></span>     | [<span data-ttu-id="bd5bf-241">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-241">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="bd5bf-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_плоскость для глаз в ГК \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-243">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-243">Property</span></span> | <span data-ttu-id="bd5bf-244">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-244">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="bd5bf-245">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-245">Description:</span></span>     | <span data-ttu-id="bd5bf-246">Коэффициенты уравнений в тексжен плоскости</span><span class="sxs-lookup"><span data-stu-id="bd5bf-246">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="bd5bf-247">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-247">Attribute group:</span></span> | <span data-ttu-id="bd5bf-248">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-248">texture</span></span>                              |
| <span data-ttu-id="bd5bf-249">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-249">Initial value:</span></span>   |                                      |
| <span data-ttu-id="bd5bf-250">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-250">Get command:</span></span>     | [<span data-ttu-id="bd5bf-251">**глжеттексженфв**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-251">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="bd5bf-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_плоскость объектов \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-253">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-253">Property</span></span> | <span data-ttu-id="bd5bf-254">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-254">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="bd5bf-255">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-255">Description:</span></span>     | <span data-ttu-id="bd5bf-256">Линейные Коэффициенты объектного объекта тексжен</span><span class="sxs-lookup"><span data-stu-id="bd5bf-256">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="bd5bf-257">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-257">Attribute group:</span></span> | <span data-ttu-id="bd5bf-258">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-258">texture</span></span>                              |
| <span data-ttu-id="bd5bf-259">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-259">Initial value:</span></span>   |                                      |
| <span data-ttu-id="bd5bf-260">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-260">Get command:</span></span>     | [<span data-ttu-id="bd5bf-261">**глжеттексженфв**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-261">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="bd5bf-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_ \_ режим ГЕНЕРАЦИИ текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bd5bf-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="bd5bf-263">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd5bf-263">Property</span></span> | <span data-ttu-id="bd5bf-264">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5bf-264">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="bd5bf-265">Описание.</span><span class="sxs-lookup"><span data-stu-id="bd5bf-265">Description:</span></span>     | <span data-ttu-id="bd5bf-266">Функция, используемая для тексжен</span><span class="sxs-lookup"><span data-stu-id="bd5bf-266">Function used for texgen</span></span>             |
| <span data-ttu-id="bd5bf-267">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-267">Attribute group:</span></span> | <span data-ttu-id="bd5bf-268">текстура</span><span class="sxs-lookup"><span data-stu-id="bd5bf-268">texture</span></span>                              |
| <span data-ttu-id="bd5bf-269">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-269">Initial value:</span></span>   | <span data-ttu-id="bd5bf-270">\_линейный глаз в ГК \_</span><span class="sxs-lookup"><span data-stu-id="bd5bf-270">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="bd5bf-271">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="bd5bf-271">Get command:</span></span>     | [<span data-ttu-id="bd5bf-272">**глжеттексженив**</span><span class="sxs-lookup"><span data-stu-id="bd5bf-272">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




