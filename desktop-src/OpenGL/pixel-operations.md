---
title: Операции с пикселами
description: Операции с пикселами
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Точечные операции OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889511"
---
# <a name="pixel-operations"></a><span data-ttu-id="f3999-104">Операции с пикселами</span><span class="sxs-lookup"><span data-stu-id="f3999-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="f3999-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_тест вырезание GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-106">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-106">Description:</span></span>     | <span data-ttu-id="f3999-107">Ножницы включены</span><span class="sxs-lookup"><span data-stu-id="f3999-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="f3999-108">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-108">Attribute group:</span></span> | <span data-ttu-id="f3999-109">Распашная/включенная</span><span class="sxs-lookup"><span data-stu-id="f3999-109">scissor/enable</span></span>                     |
| <span data-ttu-id="f3999-110">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-110">Initial value:</span></span>   | <span data-ttu-id="f3999-111">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-112">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-112">Get command:</span></span>     | [<span data-ttu-id="f3999-113">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_прямоугольная \_ раскрывающийся список</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-115">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-115">Description:</span></span>     | <span data-ttu-id="f3999-116">Прямоугольная рамка</span><span class="sxs-lookup"><span data-stu-id="f3999-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="f3999-117">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-117">Attribute group:</span></span> | <span data-ttu-id="f3999-118">распашн</span><span class="sxs-lookup"><span data-stu-id="f3999-118">scissor</span></span>                                                                          |
| <span data-ttu-id="f3999-119">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="f3999-120">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-120">Get command:</span></span>     | [<span data-ttu-id="f3999-121">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_тест шаблона \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-123">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-123">Description:</span></span>     | <span data-ttu-id="f3999-124">Набор элементов включен</span><span class="sxs-lookup"><span data-stu-id="f3999-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="f3999-125">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-125">Attribute group:</span></span> | <span data-ttu-id="f3999-126">набор элементов — буфер/включить</span><span class="sxs-lookup"><span data-stu-id="f3999-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="f3999-127">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-127">Initial value:</span></span>   | <span data-ttu-id="f3999-128">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-129">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-129">Get command:</span></span>     | [<span data-ttu-id="f3999-130">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>\_набор элементов GL, \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-132">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-132">Description:</span></span>     | <span data-ttu-id="f3999-133">Функция набора элементов</span><span class="sxs-lookup"><span data-stu-id="f3999-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="f3999-134">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-134">Attribute group:</span></span> | <span data-ttu-id="f3999-135">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-136">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-136">Initial value:</span></span>   | <span data-ttu-id="f3999-137">GL \_ всегда</span><span class="sxs-lookup"><span data-stu-id="f3999-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="f3999-138">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-138">Get command:</span></span>     | [<span data-ttu-id="f3999-139">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_Маска значения трафарета GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-141">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-141">Description:</span></span>     | <span data-ttu-id="f3999-142">Маска набора элементов</span><span class="sxs-lookup"><span data-stu-id="f3999-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="f3999-143">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-143">Attribute group:</span></span> | <span data-ttu-id="f3999-144">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-145">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-145">Initial value:</span></span>   | <span data-ttu-id="f3999-146">1</span><span class="sxs-lookup"><span data-stu-id="f3999-146">1's</span></span>                                                                              |
| <span data-ttu-id="f3999-147">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-147">Get command:</span></span>     | [<span data-ttu-id="f3999-148">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_ссылка на набор элементов GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-150">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-150">Description:</span></span>     | <span data-ttu-id="f3999-151">Значение ссылки на набор элементов</span><span class="sxs-lookup"><span data-stu-id="f3999-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="f3999-152">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-152">Attribute group:</span></span> | <span data-ttu-id="f3999-153">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-154">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-154">Initial value:</span></span>   | <span data-ttu-id="f3999-155">0</span><span class="sxs-lookup"><span data-stu-id="f3999-155">0</span></span>                                                                                |
| <span data-ttu-id="f3999-156">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-156">Get command:</span></span>     | [<span data-ttu-id="f3999-157">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_сбой шаблона \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-159">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-159">Description:</span></span>     | <span data-ttu-id="f3999-160">Действие при сбое шаблона</span><span class="sxs-lookup"><span data-stu-id="f3999-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="f3999-161">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-161">Attribute group:</span></span> | <span data-ttu-id="f3999-162">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-163">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-163">Initial value:</span></span>   | <span data-ttu-id="f3999-164">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f3999-165">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-165">Get command:</span></span>     | [<span data-ttu-id="f3999-166">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_ \_ \_ \_ не пройдена глубина этапа шаблона GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-168">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-168">Description:</span></span>     | <span data-ttu-id="f3999-169">Действие сбоя буфера глубины набора элементов</span><span class="sxs-lookup"><span data-stu-id="f3999-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="f3999-170">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-170">Attribute group:</span></span> | <span data-ttu-id="f3999-171">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-172">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-172">Initial value:</span></span>   | <span data-ttu-id="f3999-173">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f3999-174">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-174">Get command:</span></span>     | [<span data-ttu-id="f3999-175">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_ \_ этап глубины пройденного набора элементов GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-177">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-177">Description:</span></span>     | <span data-ttu-id="f3999-178">Действие передачи буфера глубины набора элементов</span><span class="sxs-lookup"><span data-stu-id="f3999-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="f3999-179">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-179">Attribute group:</span></span> | <span data-ttu-id="f3999-180">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f3999-181">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-181">Initial value:</span></span>   | <span data-ttu-id="f3999-182">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f3999-183">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-183">Get command:</span></span>     | [<span data-ttu-id="f3999-184">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_альфа- \_ тест GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-186">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-186">Description:</span></span>     | <span data-ttu-id="f3999-187">Альфа-тестирование включено</span><span class="sxs-lookup"><span data-stu-id="f3999-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="f3999-188">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-188">Attribute group:</span></span> | <span data-ttu-id="f3999-189">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="f3999-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="f3999-190">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-190">Initial value:</span></span>   | <span data-ttu-id="f3999-191">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-192">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-192">Get command:</span></span>     | [<span data-ttu-id="f3999-193">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>некоторая альфа-проверка в ГК \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-195">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-195">Description:</span></span>     | <span data-ttu-id="f3999-196">Функция теста Alpha</span><span class="sxs-lookup"><span data-stu-id="f3999-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="f3999-197">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-197">Attribute group:</span></span> | <span data-ttu-id="f3999-198">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-199">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-199">Initial value:</span></span>   | <span data-ttu-id="f3999-200">GL \_ всегда</span><span class="sxs-lookup"><span data-stu-id="f3999-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="f3999-201">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-201">Get command:</span></span>     | [<span data-ttu-id="f3999-202">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_ссылка на \_ тестовое альфа-канал GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-204">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-204">Description:</span></span>     | <span data-ttu-id="f3999-205">Эталонное значение альфа-теста</span><span class="sxs-lookup"><span data-stu-id="f3999-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="f3999-206">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-206">Attribute group:</span></span> | <span data-ttu-id="f3999-207">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-208">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-208">Initial value:</span></span>   | <span data-ttu-id="f3999-209">0</span><span class="sxs-lookup"><span data-stu-id="f3999-209">0</span></span>                                                                                |
| <span data-ttu-id="f3999-210">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-210">Get command:</span></span>     | [<span data-ttu-id="f3999-211">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_тест глубины \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-213">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-213">Description:</span></span>     | <span data-ttu-id="f3999-214">Буфер глубины включен</span><span class="sxs-lookup"><span data-stu-id="f3999-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="f3999-215">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-215">Attribute group:</span></span> | <span data-ttu-id="f3999-216">Глубина-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="f3999-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="f3999-217">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-217">Initial value:</span></span>   | <span data-ttu-id="f3999-218">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-219">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-219">Get command:</span></span>     | [<span data-ttu-id="f3999-220">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>Глубина GL — \_ \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-222">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-222">Description:</span></span>     | <span data-ttu-id="f3999-223">Функция тестирования буфера глубины</span><span class="sxs-lookup"><span data-stu-id="f3999-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="f3999-224">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-224">Attribute group:</span></span> | <span data-ttu-id="f3999-225">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="f3999-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-226">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-226">Initial value:</span></span>   | <span data-ttu-id="f3999-227">\_меньше ГК</span><span class="sxs-lookup"><span data-stu-id="f3999-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="f3999-228">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-228">Get command:</span></span>     | [<span data-ttu-id="f3999-229">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>ГК \_ Blend</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-231">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-231">Description:</span></span>     | <span data-ttu-id="f3999-232">Наложение включено</span><span class="sxs-lookup"><span data-stu-id="f3999-232">Blending enabled</span></span>                   |
| <span data-ttu-id="f3999-233">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-233">Attribute group:</span></span> | <span data-ttu-id="f3999-234">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="f3999-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="f3999-235">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-235">Initial value:</span></span>   | <span data-ttu-id="f3999-236">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-237">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-237">Get command:</span></span>     | [<span data-ttu-id="f3999-238">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_Бленк \_ src ГК</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-240">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-240">Description:</span></span>     | <span data-ttu-id="f3999-241">Исходная функция смешения</span><span class="sxs-lookup"><span data-stu-id="f3999-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="f3999-242">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-242">Attribute group:</span></span> | <span data-ttu-id="f3999-243">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-244">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-244">Initial value:</span></span>   | <span data-ttu-id="f3999-245">\_один GL</span><span class="sxs-lookup"><span data-stu-id="f3999-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="f3999-246">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-246">Get command:</span></span>     | [<span data-ttu-id="f3999-247">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>время \_ перехода на \_ летнее время</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-249">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-249">Description:</span></span>     | <span data-ttu-id="f3999-250">Наложение функции назначения</span><span class="sxs-lookup"><span data-stu-id="f3999-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="f3999-251">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-251">Attribute group:</span></span> | <span data-ttu-id="f3999-252">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-253">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-253">Initial value:</span></span>   | <span data-ttu-id="f3999-254">ноль в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="f3999-255">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-255">Get command:</span></span>     | [<span data-ttu-id="f3999-256">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f3999-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_ДИЗЕРИНГ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-258">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-258">Description:</span></span>     | <span data-ttu-id="f3999-259">Смешение цветов включено</span><span class="sxs-lookup"><span data-stu-id="f3999-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="f3999-260">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-260">Attribute group:</span></span> | <span data-ttu-id="f3999-261">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="f3999-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="f3999-262">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-262">Initial value:</span></span>   | <span data-ttu-id="f3999-263">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="f3999-264">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-264">Get command:</span></span>     | [<span data-ttu-id="f3999-265">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_логическая \_ Операция GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f3999-267">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-267">Description:</span></span>     | <span data-ttu-id="f3999-268">Логическая операция включена</span><span class="sxs-lookup"><span data-stu-id="f3999-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="f3999-269">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-269">Attribute group:</span></span> | <span data-ttu-id="f3999-270">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="f3999-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="f3999-271">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-271">Initial value:</span></span>   | <span data-ttu-id="f3999-272">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="f3999-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f3999-273">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-273">Get command:</span></span>     | [<span data-ttu-id="f3999-274">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f3999-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f3999-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_режим логики операций ГК \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f3999-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3999-276">Описание.</span><span class="sxs-lookup"><span data-stu-id="f3999-276">Description:</span></span>     | <span data-ttu-id="f3999-277">Функция логической операции</span><span class="sxs-lookup"><span data-stu-id="f3999-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="f3999-278">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="f3999-278">Attribute group:</span></span> | <span data-ttu-id="f3999-279">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="f3999-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f3999-280">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="f3999-280">Initial value:</span></span>   | <span data-ttu-id="f3999-281">копирование в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f3999-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="f3999-282">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="f3999-282">Get command:</span></span>     | [<span data-ttu-id="f3999-283">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="f3999-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




