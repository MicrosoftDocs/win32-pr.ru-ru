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
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908882"
---
# <a name="pixel-operations"></a><span data-ttu-id="6ceda-104">Операции с пикселами</span><span class="sxs-lookup"><span data-stu-id="6ceda-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="6ceda-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_тест вырезание GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-106">Property</span></span> | <span data-ttu-id="6ceda-107">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-108">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-108">Description:</span></span>     | <span data-ttu-id="6ceda-109">Ножницы включены</span><span class="sxs-lookup"><span data-stu-id="6ceda-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="6ceda-110">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-110">Attribute group:</span></span> | <span data-ttu-id="6ceda-111">Распашная/включенная</span><span class="sxs-lookup"><span data-stu-id="6ceda-111">scissor/enable</span></span>                     |
| <span data-ttu-id="6ceda-112">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-112">Initial value:</span></span>   | <span data-ttu-id="6ceda-113">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-114">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-114">Get command:</span></span>     | [<span data-ttu-id="6ceda-115">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_прямоугольная \_ раскрывающийся список</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-117">Property</span></span> | <span data-ttu-id="6ceda-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-119">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-119">Description:</span></span>     | <span data-ttu-id="6ceda-120">Прямоугольная рамка</span><span class="sxs-lookup"><span data-stu-id="6ceda-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="6ceda-121">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-121">Attribute group:</span></span> | <span data-ttu-id="6ceda-122">распашн</span><span class="sxs-lookup"><span data-stu-id="6ceda-122">scissor</span></span>                                                                          |
| <span data-ttu-id="6ceda-123">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="6ceda-124">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-124">Get command:</span></span>     | [<span data-ttu-id="6ceda-125">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_тест шаблона \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-127">Property</span></span> | <span data-ttu-id="6ceda-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-129">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-129">Description:</span></span>     | <span data-ttu-id="6ceda-130">Набор элементов включен</span><span class="sxs-lookup"><span data-stu-id="6ceda-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="6ceda-131">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-131">Attribute group:</span></span> | <span data-ttu-id="6ceda-132">набор элементов — буфер/включить</span><span class="sxs-lookup"><span data-stu-id="6ceda-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="6ceda-133">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-133">Initial value:</span></span>   | <span data-ttu-id="6ceda-134">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-135">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-135">Get command:</span></span>     | [<span data-ttu-id="6ceda-136">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>\_набор элементов GL, \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-138">Property</span></span> | <span data-ttu-id="6ceda-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-140">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-140">Description:</span></span>     | <span data-ttu-id="6ceda-141">Функция набора элементов</span><span class="sxs-lookup"><span data-stu-id="6ceda-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="6ceda-142">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-142">Attribute group:</span></span> | <span data-ttu-id="6ceda-143">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-144">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-144">Initial value:</span></span>   | <span data-ttu-id="6ceda-145">GL \_ всегда</span><span class="sxs-lookup"><span data-stu-id="6ceda-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="6ceda-146">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-146">Get command:</span></span>     | [<span data-ttu-id="6ceda-147">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_Маска значения трафарета GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-149">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-149">Property</span></span> | <span data-ttu-id="6ceda-150">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-151">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-151">Description:</span></span>     | <span data-ttu-id="6ceda-152">Маска набора элементов</span><span class="sxs-lookup"><span data-stu-id="6ceda-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="6ceda-153">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-153">Attribute group:</span></span> | <span data-ttu-id="6ceda-154">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-155">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-155">Initial value:</span></span>   | <span data-ttu-id="6ceda-156">1</span><span class="sxs-lookup"><span data-stu-id="6ceda-156">1's</span></span>                                                                              |
| <span data-ttu-id="6ceda-157">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-157">Get command:</span></span>     | [<span data-ttu-id="6ceda-158">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_ссылка на набор элементов GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-160">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-160">Property</span></span> | <span data-ttu-id="6ceda-161">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-162">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-162">Description:</span></span>     | <span data-ttu-id="6ceda-163">Значение ссылки на набор элементов</span><span class="sxs-lookup"><span data-stu-id="6ceda-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="6ceda-164">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-164">Attribute group:</span></span> | <span data-ttu-id="6ceda-165">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-166">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-166">Initial value:</span></span>   | <span data-ttu-id="6ceda-167">0</span><span class="sxs-lookup"><span data-stu-id="6ceda-167">0</span></span>                                                                                |
| <span data-ttu-id="6ceda-168">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-168">Get command:</span></span>     | [<span data-ttu-id="6ceda-169">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_сбой шаблона \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-171">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-171">Property</span></span> | <span data-ttu-id="6ceda-172">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-173">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-173">Description:</span></span>     | <span data-ttu-id="6ceda-174">Действие при сбое шаблона</span><span class="sxs-lookup"><span data-stu-id="6ceda-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="6ceda-175">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-175">Attribute group:</span></span> | <span data-ttu-id="6ceda-176">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-177">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-177">Initial value:</span></span>   | <span data-ttu-id="6ceda-178">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="6ceda-179">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-179">Get command:</span></span>     | [<span data-ttu-id="6ceda-180">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_ \_ \_ \_ не пройдена глубина этапа шаблона GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-182">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-182">Property</span></span> | <span data-ttu-id="6ceda-183">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-184">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-184">Description:</span></span>     | <span data-ttu-id="6ceda-185">Действие сбоя буфера глубины набора элементов</span><span class="sxs-lookup"><span data-stu-id="6ceda-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="6ceda-186">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-186">Attribute group:</span></span> | <span data-ttu-id="6ceda-187">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-188">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-188">Initial value:</span></span>   | <span data-ttu-id="6ceda-189">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="6ceda-190">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-190">Get command:</span></span>     | [<span data-ttu-id="6ceda-191">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_ \_ этап глубины пройденного набора элементов GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-193">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-193">Property</span></span> | <span data-ttu-id="6ceda-194">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-195">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-195">Description:</span></span>     | <span data-ttu-id="6ceda-196">Действие передачи буфера глубины набора элементов</span><span class="sxs-lookup"><span data-stu-id="6ceda-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="6ceda-197">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-197">Attribute group:</span></span> | <span data-ttu-id="6ceda-198">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="6ceda-199">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-199">Initial value:</span></span>   | <span data-ttu-id="6ceda-200">Держитесь в ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="6ceda-201">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-201">Get command:</span></span>     | [<span data-ttu-id="6ceda-202">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_альфа- \_ тест GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-204">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-204">Property</span></span> | <span data-ttu-id="6ceda-205">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-206">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-206">Description:</span></span>     | <span data-ttu-id="6ceda-207">Альфа-тестирование включено</span><span class="sxs-lookup"><span data-stu-id="6ceda-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="6ceda-208">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-208">Attribute group:</span></span> | <span data-ttu-id="6ceda-209">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="6ceda-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="6ceda-210">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-210">Initial value:</span></span>   | <span data-ttu-id="6ceda-211">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-212">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-212">Get command:</span></span>     | [<span data-ttu-id="6ceda-213">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>некоторая альфа-проверка в ГК \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-215">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-215">Property</span></span> | <span data-ttu-id="6ceda-216">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-217">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-217">Description:</span></span>     | <span data-ttu-id="6ceda-218">Функция теста Alpha</span><span class="sxs-lookup"><span data-stu-id="6ceda-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="6ceda-219">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-219">Attribute group:</span></span> | <span data-ttu-id="6ceda-220">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-221">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-221">Initial value:</span></span>   | <span data-ttu-id="6ceda-222">GL \_ всегда</span><span class="sxs-lookup"><span data-stu-id="6ceda-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="6ceda-223">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-223">Get command:</span></span>     | [<span data-ttu-id="6ceda-224">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_ссылка на \_ тестовое альфа-канал GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-226">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-226">Property</span></span> | <span data-ttu-id="6ceda-227">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-228">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-228">Description:</span></span>     | <span data-ttu-id="6ceda-229">Эталонное значение альфа-теста</span><span class="sxs-lookup"><span data-stu-id="6ceda-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="6ceda-230">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-230">Attribute group:</span></span> | <span data-ttu-id="6ceda-231">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-232">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-232">Initial value:</span></span>   | <span data-ttu-id="6ceda-233">0</span><span class="sxs-lookup"><span data-stu-id="6ceda-233">0</span></span>                                                                                |
| <span data-ttu-id="6ceda-234">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-234">Get command:</span></span>     | [<span data-ttu-id="6ceda-235">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_тест глубины \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-237">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-237">Property</span></span> | <span data-ttu-id="6ceda-238">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-239">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-239">Description:</span></span>     | <span data-ttu-id="6ceda-240">Буфер глубины включен</span><span class="sxs-lookup"><span data-stu-id="6ceda-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="6ceda-241">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-241">Attribute group:</span></span> | <span data-ttu-id="6ceda-242">Глубина-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="6ceda-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="6ceda-243">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-243">Initial value:</span></span>   | <span data-ttu-id="6ceda-244">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-245">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-245">Get command:</span></span>     | [<span data-ttu-id="6ceda-246">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>Глубина GL — \_ \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-248">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-248">Property</span></span> | <span data-ttu-id="6ceda-249">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-250">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-250">Description:</span></span>     | <span data-ttu-id="6ceda-251">Функция тестирования буфера глубины</span><span class="sxs-lookup"><span data-stu-id="6ceda-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="6ceda-252">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-252">Attribute group:</span></span> | <span data-ttu-id="6ceda-253">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="6ceda-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-254">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-254">Initial value:</span></span>   | <span data-ttu-id="6ceda-255">\_меньше ГК</span><span class="sxs-lookup"><span data-stu-id="6ceda-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="6ceda-256">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-256">Get command:</span></span>     | [<span data-ttu-id="6ceda-257">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>ГК \_ Blend</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-259">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-259">Property</span></span> | <span data-ttu-id="6ceda-260">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-261">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-261">Description:</span></span>     | <span data-ttu-id="6ceda-262">Наложение включено</span><span class="sxs-lookup"><span data-stu-id="6ceda-262">Blending enabled</span></span>                   |
| <span data-ttu-id="6ceda-263">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-263">Attribute group:</span></span> | <span data-ttu-id="6ceda-264">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="6ceda-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="6ceda-265">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-265">Initial value:</span></span>   | <span data-ttu-id="6ceda-266">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-267">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-267">Get command:</span></span>     | [<span data-ttu-id="6ceda-268">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_Бленк \_ src ГК</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-270">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-270">Property</span></span> | <span data-ttu-id="6ceda-271">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-272">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-272">Description:</span></span>     | <span data-ttu-id="6ceda-273">Исходная функция смешения</span><span class="sxs-lookup"><span data-stu-id="6ceda-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="6ceda-274">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-274">Attribute group:</span></span> | <span data-ttu-id="6ceda-275">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-276">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-276">Initial value:</span></span>   | <span data-ttu-id="6ceda-277">\_один GL</span><span class="sxs-lookup"><span data-stu-id="6ceda-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="6ceda-278">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-278">Get command:</span></span>     | [<span data-ttu-id="6ceda-279">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>время \_ перехода на \_ летнее время</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-281">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-281">Property</span></span> | <span data-ttu-id="6ceda-282">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-283">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-283">Description:</span></span>     | <span data-ttu-id="6ceda-284">Наложение функции назначения</span><span class="sxs-lookup"><span data-stu-id="6ceda-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="6ceda-285">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-285">Attribute group:</span></span> | <span data-ttu-id="6ceda-286">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-287">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-287">Initial value:</span></span>   | <span data-ttu-id="6ceda-288">ноль в ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="6ceda-289">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-289">Get command:</span></span>     | [<span data-ttu-id="6ceda-290">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="6ceda-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_ДИЗЕРИНГ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-292">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-292">Property</span></span> | <span data-ttu-id="6ceda-293">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-294">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-294">Description:</span></span>     | <span data-ttu-id="6ceda-295">Смешение цветов включено</span><span class="sxs-lookup"><span data-stu-id="6ceda-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="6ceda-296">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-296">Attribute group:</span></span> | <span data-ttu-id="6ceda-297">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="6ceda-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="6ceda-298">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-298">Initial value:</span></span>   | <span data-ttu-id="6ceda-299">значение по ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="6ceda-300">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-300">Get command:</span></span>     | [<span data-ttu-id="6ceda-301">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_логическая \_ Операция GL</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-303">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-303">Property</span></span> | <span data-ttu-id="6ceda-304">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="6ceda-305">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-305">Description:</span></span>     | <span data-ttu-id="6ceda-306">Логическая операция включена</span><span class="sxs-lookup"><span data-stu-id="6ceda-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="6ceda-307">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-307">Attribute group:</span></span> | <span data-ttu-id="6ceda-308">цвет-буферизация/включение</span><span class="sxs-lookup"><span data-stu-id="6ceda-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="6ceda-309">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-309">Initial value:</span></span>   | <span data-ttu-id="6ceda-310">GL, \_ значение false</span><span class="sxs-lookup"><span data-stu-id="6ceda-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="6ceda-311">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-311">Get command:</span></span>     | [<span data-ttu-id="6ceda-312">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="6ceda-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="6ceda-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_режим логики операций ГК \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="6ceda-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="6ceda-314">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceda-314">Property</span></span> | <span data-ttu-id="6ceda-315">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-316">Описание.</span><span class="sxs-lookup"><span data-stu-id="6ceda-316">Description:</span></span>     | <span data-ttu-id="6ceda-317">Функция логической операции</span><span class="sxs-lookup"><span data-stu-id="6ceda-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="6ceda-318">Группа атрибутов:</span><span class="sxs-lookup"><span data-stu-id="6ceda-318">Attribute group:</span></span> | <span data-ttu-id="6ceda-319">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="6ceda-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="6ceda-320">Начальное значение:</span><span class="sxs-lookup"><span data-stu-id="6ceda-320">Initial value:</span></span>   | <span data-ttu-id="6ceda-321">копирование в ГК \_</span><span class="sxs-lookup"><span data-stu-id="6ceda-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="6ceda-322">Команда Get:</span><span class="sxs-lookup"><span data-stu-id="6ceda-322">Get command:</span></span>     | [<span data-ttu-id="6ceda-323">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="6ceda-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




