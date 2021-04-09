---
title: Переменные состояния освещения
description: Переменные состояния освещения
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Переменные состояния освещения OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889635"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="c000a-104">Переменные состояния освещения</span><span class="sxs-lookup"><span data-stu-id="c000a-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="c000a-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>освещение в ГК \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-106">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-106">Description:</span></span>     | <span data-ttu-id="c000a-107">True, если освещение включено</span><span class="sxs-lookup"><span data-stu-id="c000a-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="c000a-108">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-108">Attribute group:</span></span> | <span data-ttu-id="c000a-109">освещение/включить</span><span class="sxs-lookup"><span data-stu-id="c000a-109">lighting/enable</span></span>                    |
| <span data-ttu-id="c000a-110">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-110">Initial value:</span></span>   | <span data-ttu-id="c000a-111">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="c000a-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="c000a-112">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-112">Get command:</span></span>     | [<span data-ttu-id="c000a-113">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="c000a-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="c000a-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_цветовой \_ материал GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-115">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-115">Description:</span></span>     | <span data-ttu-id="c000a-116">True, если включено отслеживание цветов</span><span class="sxs-lookup"><span data-stu-id="c000a-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="c000a-117">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-117">Attribute group:</span></span> | <span data-ttu-id="c000a-118">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-118">lighting</span></span>                           |
| <span data-ttu-id="c000a-119">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-119">Initial value:</span></span>   | <span data-ttu-id="c000a-120">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="c000a-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="c000a-121">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-121">Get command:</span></span>     | [<span data-ttu-id="c000a-122">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="c000a-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="c000a-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_параметр цветового \_ материала GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-124">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-124">Description:</span></span>     | <span data-ttu-id="c000a-125">Свойства материала, отслеживающие текущий цвет</span><span class="sxs-lookup"><span data-stu-id="c000a-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="c000a-126">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-126">Attribute group:</span></span> | <span data-ttu-id="c000a-127">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-127">lighting</span></span>                                                                         |
| <span data-ttu-id="c000a-128">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-128">Initial value:</span></span>   | <span data-ttu-id="c000a-129">\_внешняя \_ и \_ РАССЕЯНная среды GL</span><span class="sxs-lookup"><span data-stu-id="c000a-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="c000a-130">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-130">Get command:</span></span>     | [<span data-ttu-id="c000a-131">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="c000a-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c000a-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_цветовой \_ материал \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-133">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-133">Description:</span></span>     | <span data-ttu-id="c000a-134">Лица, затрагиваемые отслеживанием цветов</span><span class="sxs-lookup"><span data-stu-id="c000a-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="c000a-135">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-135">Attribute group:</span></span> | <span data-ttu-id="c000a-136">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-136">lighting</span></span>                                                                         |
| <span data-ttu-id="c000a-137">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-137">Initial value:</span></span>   | <span data-ttu-id="c000a-138">\_Передняя \_ и \_ задняя части GL</span><span class="sxs-lookup"><span data-stu-id="c000a-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="c000a-139">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-139">Get command:</span></span>     | [<span data-ttu-id="c000a-140">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="c000a-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c000a-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_окружение GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c000a-142">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-142">Description:</span></span>     | <span data-ttu-id="c000a-143">Цвет окружающих материалов</span><span class="sxs-lookup"><span data-stu-id="c000a-143">Ambient material color</span></span>                   |
| <span data-ttu-id="c000a-144">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-144">Attribute group:</span></span> | <span data-ttu-id="c000a-145">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-145">lighting</span></span>                                 |
| <span data-ttu-id="c000a-146">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-146">Initial value:</span></span>   | <span data-ttu-id="c000a-147">(0,2, 0,2, 0,2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="c000a-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="c000a-148">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-148">Get command:</span></span>     | [<span data-ttu-id="c000a-149">**глжетматериалфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="c000a-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>Рассеивание GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c000a-151">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-151">Description:</span></span>     | <span data-ttu-id="c000a-152">Цвет рассеянного материала</span><span class="sxs-lookup"><span data-stu-id="c000a-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="c000a-153">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-153">Attribute group:</span></span> | <span data-ttu-id="c000a-154">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-154">lighting</span></span>                                 |
| <span data-ttu-id="c000a-155">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-155">Initial value:</span></span>   | <span data-ttu-id="c000a-156">(0,8, 0,8, 0,8, 1,0)</span><span class="sxs-lookup"><span data-stu-id="c000a-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="c000a-157">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-157">Get command:</span></span>     | [<span data-ttu-id="c000a-158">**глжетматериалфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="c000a-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_отражающий GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c000a-160">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-160">Description:</span></span>     | <span data-ttu-id="c000a-161">Цвет отражающих материалов</span><span class="sxs-lookup"><span data-stu-id="c000a-161">Specular material color</span></span>                  |
| <span data-ttu-id="c000a-162">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-162">Attribute group:</span></span> | <span data-ttu-id="c000a-163">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-163">lighting</span></span>                                 |
| <span data-ttu-id="c000a-164">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-164">Initial value:</span></span>   | <span data-ttu-id="c000a-165">(0,0, 0,0, 0.0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="c000a-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="c000a-166">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-166">Get command:</span></span>     | [<span data-ttu-id="c000a-167">**глжетматериалфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="c000a-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_эмиссия GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c000a-169">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-169">Description:</span></span>     | <span data-ttu-id="c000a-170">Цвет материала эмиссионный</span><span class="sxs-lookup"><span data-stu-id="c000a-170">Emissive material color</span></span>                  |
| <span data-ttu-id="c000a-171">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-171">Attribute group:</span></span> | <span data-ttu-id="c000a-172">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-172">lighting</span></span>                                 |
| <span data-ttu-id="c000a-173">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-173">Initial value:</span></span>   | <span data-ttu-id="c000a-174">(0,0, 0,0, 0.0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="c000a-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="c000a-175">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-175">Get command:</span></span>     | [<span data-ttu-id="c000a-176">**глжетматериалфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="c000a-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_коэффициента БЛЕСКА GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c000a-178">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-178">Description:</span></span>     | <span data-ttu-id="c000a-179">Отражающая экспонента материала</span><span class="sxs-lookup"><span data-stu-id="c000a-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="c000a-180">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-180">Attribute group:</span></span> | <span data-ttu-id="c000a-181">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-181">lighting</span></span>                                 |
| <span data-ttu-id="c000a-182">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-182">Initial value:</span></span>   | <span data-ttu-id="c000a-183">0,0</span><span class="sxs-lookup"><span data-stu-id="c000a-183">0.0</span></span>                                      |
| <span data-ttu-id="c000a-184">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-184">Get command:</span></span>     | [<span data-ttu-id="c000a-185">**глжетматериалфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="c000a-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ \_ Наружная модель освещения GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-187">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-187">Description:</span></span>     | <span data-ttu-id="c000a-188">Цвет окружающей сцены</span><span class="sxs-lookup"><span data-stu-id="c000a-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="c000a-189">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-189">Attribute group:</span></span> | <span data-ttu-id="c000a-190">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-190">lighting</span></span>                                                                       |
| <span data-ttu-id="c000a-191">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-191">Initial value:</span></span>   | <span data-ttu-id="c000a-192">(0,2, 0,2, 0,2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="c000a-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="c000a-193">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-193">Get command:</span></span>     | [<span data-ttu-id="c000a-194">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="c000a-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c000a-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ Локальное \_ средство просмотра модели освещения GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-196">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-196">Description:</span></span>     | <span data-ttu-id="c000a-197">Средство просмотра является локальным</span><span class="sxs-lookup"><span data-stu-id="c000a-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="c000a-198">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-198">Attribute group:</span></span> | <span data-ttu-id="c000a-199">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-199">lighting</span></span>                                                                         |
| <span data-ttu-id="c000a-200">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-200">Initial value:</span></span>   | <span data-ttu-id="c000a-201">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="c000a-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="c000a-202">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-202">Get command:</span></span>     | [<span data-ttu-id="c000a-203">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="c000a-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c000a-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_простая модель GL на \_ \_ две \_ стороны</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-205">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-205">Description:</span></span>     | <span data-ttu-id="c000a-206">Использование двустороннего освещения</span><span class="sxs-lookup"><span data-stu-id="c000a-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="c000a-207">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-207">Attribute group:</span></span> | <span data-ttu-id="c000a-208">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-208">lighting</span></span>                                                                         |
| <span data-ttu-id="c000a-209">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-209">Initial value:</span></span>   | <span data-ttu-id="c000a-210">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="c000a-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="c000a-211">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-211">Get command:</span></span>     | [<span data-ttu-id="c000a-212">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="c000a-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c000a-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_окружение GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-214">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-214">Description:</span></span>     | <span data-ttu-id="c000a-215">Интенсивность окружающей среды светлого *i*</span><span class="sxs-lookup"><span data-stu-id="c000a-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="c000a-216">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-216">Attribute group:</span></span> | <span data-ttu-id="c000a-217">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-217">lighting</span></span>                           |
| <span data-ttu-id="c000a-218">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-218">Initial value:</span></span>   | <span data-ttu-id="c000a-219">(0,0, 0,0, 0.0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="c000a-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="c000a-220">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-220">Get command:</span></span>     | [<span data-ttu-id="c000a-221">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>Рассеивание GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-223">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-223">Description:</span></span>     | <span data-ttu-id="c000a-224">Интенсивность диффузии света </span><span class="sxs-lookup"><span data-stu-id="c000a-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="c000a-225">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-225">Attribute group:</span></span> | <span data-ttu-id="c000a-226">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-226">lighting</span></span>                           |
| <span data-ttu-id="c000a-227">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="c000a-228">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-228">Get command:</span></span>     | [<span data-ttu-id="c000a-229">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_отражающий GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-231">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-231">Description:</span></span>     | <span data-ttu-id="c000a-232">Интенсивность *отражения светлой*</span><span class="sxs-lookup"><span data-stu-id="c000a-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="c000a-233">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-233">Attribute group:</span></span> | <span data-ttu-id="c000a-234">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-234">lighting</span></span>                           |
| <span data-ttu-id="c000a-235">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="c000a-236">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-236">Get command:</span></span>     | [<span data-ttu-id="c000a-237">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_Расположение GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-239">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-239">Description:</span></span>     | <span data-ttu-id="c000a-240">Расположение светлого *i*</span><span class="sxs-lookup"><span data-stu-id="c000a-240">Position of light *i*</span></span>              |
| <span data-ttu-id="c000a-241">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-241">Attribute group:</span></span> | <span data-ttu-id="c000a-242">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-242">lighting</span></span>                           |
| <span data-ttu-id="c000a-243">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-243">Initial value:</span></span>   | <span data-ttu-id="c000a-244">(0,0, 0,0, 1,0, 0.0)</span><span class="sxs-lookup"><span data-stu-id="c000a-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="c000a-245">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-245">Get command:</span></span>     | [<span data-ttu-id="c000a-246">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_затухание константы GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-248">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-248">Description:</span></span>     | <span data-ttu-id="c000a-249">Константный коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="c000a-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="c000a-250">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-250">Attribute group:</span></span> | <span data-ttu-id="c000a-251">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-251">lighting</span></span>                           |
| <span data-ttu-id="c000a-252">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-252">Initial value:</span></span>   | <span data-ttu-id="c000a-253">1.0</span><span class="sxs-lookup"><span data-stu-id="c000a-253">1.0</span></span>                                |
| <span data-ttu-id="c000a-254">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-254">Get command:</span></span>     | [<span data-ttu-id="c000a-255">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_линейное \_ затухание в ГК</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-257">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-257">Description:</span></span>     | <span data-ttu-id="c000a-258">Линейный коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="c000a-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="c000a-259">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-259">Attribute group:</span></span> | <span data-ttu-id="c000a-260">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-260">lighting</span></span>                           |
| <span data-ttu-id="c000a-261">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-261">Initial value:</span></span>   | <span data-ttu-id="c000a-262">0,0</span><span class="sxs-lookup"><span data-stu-id="c000a-262">0.0</span></span>                                |
| <span data-ttu-id="c000a-263">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-263">Get command:</span></span>     | [<span data-ttu-id="c000a-264">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_затухание по квадрату GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-266">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-266">Description:</span></span>     | <span data-ttu-id="c000a-267">Квадратический коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="c000a-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="c000a-268">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-268">Attribute group:</span></span> | <span data-ttu-id="c000a-269">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-269">lighting</span></span>                           |
| <span data-ttu-id="c000a-270">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-270">Initial value:</span></span>   | <span data-ttu-id="c000a-271">0,0</span><span class="sxs-lookup"><span data-stu-id="c000a-271">0.0</span></span>                                |
| <span data-ttu-id="c000a-272">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-272">Get command:</span></span>     | [<span data-ttu-id="c000a-273">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_направление плашечного цвета GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-275">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-275">Description:</span></span>     | <span data-ttu-id="c000a-276">Направление прожектора, светло- *я*</span><span class="sxs-lookup"><span data-stu-id="c000a-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="c000a-277">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-277">Attribute group:</span></span> | <span data-ttu-id="c000a-278">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-278">lighting</span></span>                           |
| <span data-ttu-id="c000a-279">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-279">Initial value:</span></span>   | <span data-ttu-id="c000a-280">(0,0, 0,0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="c000a-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="c000a-281">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-281">Get command:</span></span>     | [<span data-ttu-id="c000a-282">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>\_показатель степени для точки GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-284">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-284">Description:</span></span>     | <span data-ttu-id="c000a-285">Прожектор, экспонента *света*</span><span class="sxs-lookup"><span data-stu-id="c000a-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="c000a-286">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-286">Attribute group:</span></span> | <span data-ttu-id="c000a-287">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-287">lighting</span></span>                           |
| <span data-ttu-id="c000a-288">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-288">Initial value:</span></span>   | <span data-ttu-id="c000a-289">0,0</span><span class="sxs-lookup"><span data-stu-id="c000a-289">0.0</span></span>                                |
| <span data-ttu-id="c000a-290">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-290">Get command:</span></span>     | [<span data-ttu-id="c000a-291">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>\_отсечение точки GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-293">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-293">Description:</span></span>     | <span data-ttu-id="c000a-294">Угол прожектора светлого *i*</span><span class="sxs-lookup"><span data-stu-id="c000a-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="c000a-295">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-295">Attribute group:</span></span> | <span data-ttu-id="c000a-296">освещение;</span><span class="sxs-lookup"><span data-stu-id="c000a-296">lighting</span></span>                           |
| <span data-ttu-id="c000a-297">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-297">Initial value:</span></span>   | <span data-ttu-id="c000a-298">180,0</span><span class="sxs-lookup"><span data-stu-id="c000a-298">180.0</span></span>                              |
| <span data-ttu-id="c000a-299">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-299">Get command:</span></span>     | [<span data-ttu-id="c000a-300">**глжетлигхтфв**</span><span class="sxs-lookup"><span data-stu-id="c000a-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="c000a-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>\_Непростая  GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="c000a-302">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-302">Description:</span></span>     | <span data-ttu-id="c000a-303">Значение true, *Если включено освещение*</span><span class="sxs-lookup"><span data-stu-id="c000a-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="c000a-304">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-304">Attribute group:</span></span> | <span data-ttu-id="c000a-305">освещение/включить</span><span class="sxs-lookup"><span data-stu-id="c000a-305">lighting/enable</span></span>                    |
| <span data-ttu-id="c000a-306">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-306">Initial value:</span></span>   | <span data-ttu-id="c000a-307">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="c000a-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="c000a-308">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-308">Get command:</span></span>     | [<span data-ttu-id="c000a-309">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="c000a-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="c000a-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_ \_ индексы цвета GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c000a-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c000a-311">Описание.</span><span class="sxs-lookup"><span data-stu-id="c000a-311">Description:</span></span>     | <span data-ttu-id="c000a-312">*C (a)*, *C (d)* и *C (s)* для освещения цветового индекса</span><span class="sxs-lookup"><span data-stu-id="c000a-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="c000a-313">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="c000a-313">Attribute group:</span></span> | <span data-ttu-id="c000a-314">освещение/включить</span><span class="sxs-lookup"><span data-stu-id="c000a-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="c000a-315">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="c000a-315">Initial value:</span></span>   | <span data-ttu-id="c000a-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="c000a-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="c000a-317">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="c000a-317">Get command:</span></span>     | [<span data-ttu-id="c000a-318">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="c000a-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




