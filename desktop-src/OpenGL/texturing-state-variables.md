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
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661663"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="03aff-104">Текстурирование переменных состояния</span><span class="sxs-lookup"><span data-stu-id="03aff-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="03aff-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Текстура GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="03aff-106">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-106">Description:</span></span>     | <span data-ttu-id="03aff-107">True    , если включено текстурирование x-d (*x* — 1-d или 2-d)</span><span class="sxs-lookup"><span data-stu-id="03aff-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="03aff-108">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-108">Attribute group:</span></span> | <span data-ttu-id="03aff-109">Текстура и включение</span><span class="sxs-lookup"><span data-stu-id="03aff-109">texture/enable</span></span>                                        |
| <span data-ttu-id="03aff-110">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-110">Initial value:</span></span>   | <span data-ttu-id="03aff-111">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="03aff-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="03aff-112">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-112">Get command:</span></span>     | [<span data-ttu-id="03aff-113">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="03aff-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="03aff-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_текстура GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="03aff-115">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-115">Description:</span></span>     | <span data-ttu-id="03aff-116">*x*   -D изображение текстуры на уровне сведений *i*</span><span class="sxs-lookup"><span data-stu-id="03aff-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="03aff-117">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="03aff-118">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="03aff-119">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-119">Get command:</span></span>     | [<span data-ttu-id="03aff-120">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="03aff-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="03aff-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_Ширина текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="03aff-122">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-122">Description:</span></span>     | <span data-ttu-id="03aff-123">*x*   -D. ширина *изображения текстуры*  </span><span class="sxs-lookup"><span data-stu-id="03aff-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="03aff-124">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="03aff-125">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-125">Initial value:</span></span>   | <span data-ttu-id="03aff-126">0</span><span class="sxs-lookup"><span data-stu-id="03aff-126">0</span></span>                                                        |
| <span data-ttu-id="03aff-127">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-127">Get command:</span></span>     | [<span data-ttu-id="03aff-128">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="03aff-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_Высота текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="03aff-130">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-130">Description:</span></span>     | <span data-ttu-id="03aff-131">*x*   -D. Высота *изображения текстуры*  </span><span class="sxs-lookup"><span data-stu-id="03aff-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="03aff-132">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="03aff-133">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-133">Initial value:</span></span>   | <span data-ttu-id="03aff-134">0</span><span class="sxs-lookup"><span data-stu-id="03aff-134">0</span></span>                                                        |
| <span data-ttu-id="03aff-135">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-135">Get command:</span></span>     | [<span data-ttu-id="03aff-136">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="03aff-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_граница текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="03aff-138">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-138">Description:</span></span>     | <span data-ttu-id="03aff-139">*x*   - *Мерная изображение с*   границей</span><span class="sxs-lookup"><span data-stu-id="03aff-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="03aff-140">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="03aff-141">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-141">Initial value:</span></span>   | <span data-ttu-id="03aff-142">0</span><span class="sxs-lookup"><span data-stu-id="03aff-142">0</span></span>                                                        |
| <span data-ttu-id="03aff-143">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-143">Get command:</span></span>     | [<span data-ttu-id="03aff-144">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="03aff-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_компоненты текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="03aff-146">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-146">Description:</span></span>     | <span data-ttu-id="03aff-147">Компоненты изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="03aff-147">Texture image components</span></span>                                 |
| <span data-ttu-id="03aff-148">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="03aff-149">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-149">Initial value:</span></span>   | <span data-ttu-id="03aff-150">1</span><span class="sxs-lookup"><span data-stu-id="03aff-150">1</span></span>                                                        |
| <span data-ttu-id="03aff-151">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-151">Get command:</span></span>     | [<span data-ttu-id="03aff-152">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="03aff-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_ \_ Цвет границы текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="03aff-154">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-154">Description:</span></span>     | <span data-ttu-id="03aff-155">Цвет границы текстуры</span><span class="sxs-lookup"><span data-stu-id="03aff-155">Texture border color</span></span>                           |
| <span data-ttu-id="03aff-156">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-156">Attribute group:</span></span> | <span data-ttu-id="03aff-157">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-157">texture</span></span>                                        |
| <span data-ttu-id="03aff-158">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-158">Initial value:</span></span>   | <span data-ttu-id="03aff-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="03aff-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="03aff-160">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-160">Get command:</span></span>     | [<span data-ttu-id="03aff-161">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="03aff-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ Фильтр min текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="03aff-163">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-163">Description:</span></span>     | <span data-ttu-id="03aff-164">Функция минификации текстуры</span><span class="sxs-lookup"><span data-stu-id="03aff-164">Texture minification function</span></span>                  |
| <span data-ttu-id="03aff-165">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-165">Attribute group:</span></span> | <span data-ttu-id="03aff-166">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-166">texture</span></span>                                        |
| <span data-ttu-id="03aff-167">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-167">Initial value:</span></span>   | <span data-ttu-id="03aff-168">\_Ближайшая \_ Линейная MIPMAPа GL \_</span><span class="sxs-lookup"><span data-stu-id="03aff-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="03aff-169">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-169">Get command:</span></span>     | [<span data-ttu-id="03aff-170">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="03aff-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ Фильтр MAG текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="03aff-172">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-172">Description:</span></span>     | <span data-ttu-id="03aff-173">Функция увеличения текстуры</span><span class="sxs-lookup"><span data-stu-id="03aff-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="03aff-174">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-174">Attribute group:</span></span> | <span data-ttu-id="03aff-175">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-175">texture</span></span>                                        |
| <span data-ttu-id="03aff-176">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-176">Initial value:</span></span>   | <span data-ttu-id="03aff-177">Линейная (GL) \_</span><span class="sxs-lookup"><span data-stu-id="03aff-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="03aff-178">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-178">Get command:</span></span>     | [<span data-ttu-id="03aff-179">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="03aff-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>\_Заносится текстура GL \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="03aff-181">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-181">Description:</span></span>     | <span data-ttu-id="03aff-182">Режим переноса текстур (*x*   — S или T)</span><span class="sxs-lookup"><span data-stu-id="03aff-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="03aff-183">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-183">Attribute group:</span></span> | <span data-ttu-id="03aff-184">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-184">texture</span></span>                                        |
| <span data-ttu-id="03aff-185">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-185">Initial value:</span></span>   | <span data-ttu-id="03aff-186">\_повторение GL</span><span class="sxs-lookup"><span data-stu-id="03aff-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="03aff-187">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-187">Get command:</span></span>     | [<span data-ttu-id="03aff-188">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="03aff-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="03aff-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_режим текстуры \_ в главной модели \_</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="03aff-190">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-190">Description:</span></span>     | <span data-ttu-id="03aff-191">Функция текстуры приложения</span><span class="sxs-lookup"><span data-stu-id="03aff-191">Texture application function</span></span>         |
| <span data-ttu-id="03aff-192">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-192">Attribute group:</span></span> | <span data-ttu-id="03aff-193">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-193">texture</span></span>                              |
| <span data-ttu-id="03aff-194">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-194">Initial value:</span></span>   | <span data-ttu-id="03aff-195">GL для \_ модуляции</span><span class="sxs-lookup"><span data-stu-id="03aff-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="03aff-196">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-196">Get command:</span></span>     | [<span data-ttu-id="03aff-197">**глжеттексенвив**</span><span class="sxs-lookup"><span data-stu-id="03aff-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="03aff-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_Цвет текстуры в главной \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="03aff-199">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-199">Description:</span></span>     | <span data-ttu-id="03aff-200">Цвет текстурной среды</span><span class="sxs-lookup"><span data-stu-id="03aff-200">Texture environment color</span></span>            |
| <span data-ttu-id="03aff-201">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-201">Attribute group:</span></span> | <span data-ttu-id="03aff-202">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-202">texture</span></span>                              |
| <span data-ttu-id="03aff-203">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-203">Initial value:</span></span>   | <span data-ttu-id="03aff-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="03aff-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="03aff-205">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-205">Get command:</span></span>     | [<span data-ttu-id="03aff-206">**глжеттексенвфв**</span><span class="sxs-lookup"><span data-stu-id="03aff-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="03aff-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>\_Gen текстура GL \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="03aff-208">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-208">Description:</span></span>     | <span data-ttu-id="03aff-209">Тексжен включен (*x*   — S, T, R или Q)</span><span class="sxs-lookup"><span data-stu-id="03aff-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="03aff-210">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-210">Attribute group:</span></span> | <span data-ttu-id="03aff-211">Текстура и включение</span><span class="sxs-lookup"><span data-stu-id="03aff-211">texture/enable</span></span>                           |
| <span data-ttu-id="03aff-212">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-212">Initial value:</span></span>   | <span data-ttu-id="03aff-213">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="03aff-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="03aff-214">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-214">Get command:</span></span>     | [<span data-ttu-id="03aff-215">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="03aff-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="03aff-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_плоскость для глаз в ГК \_</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="03aff-217">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-217">Description:</span></span>     | <span data-ttu-id="03aff-218">Коэффициенты уравнений в тексжен плоскости</span><span class="sxs-lookup"><span data-stu-id="03aff-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="03aff-219">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-219">Attribute group:</span></span> | <span data-ttu-id="03aff-220">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-220">texture</span></span>                              |
| <span data-ttu-id="03aff-221">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="03aff-222">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-222">Get command:</span></span>     | [<span data-ttu-id="03aff-223">**глжеттексженфв**</span><span class="sxs-lookup"><span data-stu-id="03aff-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="03aff-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_плоскость объектов \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="03aff-225">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-225">Description:</span></span>     | <span data-ttu-id="03aff-226">Линейные Коэффициенты объектного объекта тексжен</span><span class="sxs-lookup"><span data-stu-id="03aff-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="03aff-227">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-227">Attribute group:</span></span> | <span data-ttu-id="03aff-228">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-228">texture</span></span>                              |
| <span data-ttu-id="03aff-229">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="03aff-230">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-230">Get command:</span></span>     | [<span data-ttu-id="03aff-231">**глжеттексженфв**</span><span class="sxs-lookup"><span data-stu-id="03aff-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="03aff-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_ \_ режим ГЕНЕРАЦИИ текстуры \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="03aff-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="03aff-233">Описание.</span><span class="sxs-lookup"><span data-stu-id="03aff-233">Description:</span></span>     | <span data-ttu-id="03aff-234">Функция, используемая для тексжен</span><span class="sxs-lookup"><span data-stu-id="03aff-234">Function used for texgen</span></span>             |
| <span data-ttu-id="03aff-235">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="03aff-235">Attribute group:</span></span> | <span data-ttu-id="03aff-236">текстура</span><span class="sxs-lookup"><span data-stu-id="03aff-236">texture</span></span>                              |
| <span data-ttu-id="03aff-237">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="03aff-237">Initial value:</span></span>   | <span data-ttu-id="03aff-238">\_линейный глаз в ГК \_</span><span class="sxs-lookup"><span data-stu-id="03aff-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="03aff-239">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="03aff-239">Get command:</span></span>     | [<span data-ttu-id="03aff-240">**глжеттексженив**</span><span class="sxs-lookup"><span data-stu-id="03aff-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




