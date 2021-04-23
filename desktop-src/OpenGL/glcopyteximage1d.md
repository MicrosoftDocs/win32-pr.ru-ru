---
title: Функция glCopyTexImage1D (GL. h)
description: Функция glCopyTexImage1D копирует Пиксели из буфера кадров в одномерный рисунок текстуры.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- Функция glCopyTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661945"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="629f8-104">Функция glCopyTexImage1D</span><span class="sxs-lookup"><span data-stu-id="629f8-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="629f8-105">Функция **glCopyTexImage1D** копирует Пиксели из буфера кадров в одномерный рисунок текстуры.</span><span class="sxs-lookup"><span data-stu-id="629f8-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="629f8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="629f8-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="629f8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="629f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629f8-108">*target*</span><span class="sxs-lookup"><span data-stu-id="629f8-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-109">Целевой объект, для которого будут изменены данные изображения.</span><span class="sxs-lookup"><span data-stu-id="629f8-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="629f8-110">Должно иметь значение GL \_ текстура \_ 1d.</span><span class="sxs-lookup"><span data-stu-id="629f8-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="629f8-111">*level*</span><span class="sxs-lookup"><span data-stu-id="629f8-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="629f8-112">The level-of-detail number.</span></span> <span data-ttu-id="629f8-113">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="629f8-113">Level 0 is the base image.</span></span> <span data-ttu-id="629f8-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="629f8-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="629f8-115">*интерналформат*</span><span class="sxs-lookup"><span data-stu-id="629f8-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-116">Внутренний формат и разрешение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="629f8-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="629f8-117">Этот параметр должен быть одним из следующих символьных значений.</span><span class="sxs-lookup"><span data-stu-id="629f8-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="629f8-118">Константа</span><span class="sxs-lookup"><span data-stu-id="629f8-118">Constant</span></span>                 | <span data-ttu-id="629f8-119">Биты R</span><span class="sxs-lookup"><span data-stu-id="629f8-119">R Bits</span></span> | <span data-ttu-id="629f8-120">Биты G</span><span class="sxs-lookup"><span data-stu-id="629f8-120">G Bits</span></span> | <span data-ttu-id="629f8-121">B бит</span><span class="sxs-lookup"><span data-stu-id="629f8-121">B Bits</span></span> | <span data-ttu-id="629f8-122">Биты</span><span class="sxs-lookup"><span data-stu-id="629f8-122">A Bits</span></span> | <span data-ttu-id="629f8-123">Биты L</span><span class="sxs-lookup"><span data-stu-id="629f8-123">L Bits</span></span> | <span data-ttu-id="629f8-124">Биты I</span><span class="sxs-lookup"><span data-stu-id="629f8-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="629f8-125">\_альфа-канал GL</span><span class="sxs-lookup"><span data-stu-id="629f8-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="629f8-126">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="629f8-127">4</span><span class="sxs-lookup"><span data-stu-id="629f8-127">4</span></span>      |        |        |
| <span data-ttu-id="629f8-128">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="629f8-129">8</span><span class="sxs-lookup"><span data-stu-id="629f8-129">8</span></span>      |        |        |
| <span data-ttu-id="629f8-130">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="629f8-131">12</span><span class="sxs-lookup"><span data-stu-id="629f8-131">12</span></span>     |        |        |
| <span data-ttu-id="629f8-132">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="629f8-133">16</span><span class="sxs-lookup"><span data-stu-id="629f8-133">16</span></span>     |        |        |
| <span data-ttu-id="629f8-134">\_светимость GL</span><span class="sxs-lookup"><span data-stu-id="629f8-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="629f8-135">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="629f8-136">4</span><span class="sxs-lookup"><span data-stu-id="629f8-136">4</span></span>      |        |
| <span data-ttu-id="629f8-137">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="629f8-138">8</span><span class="sxs-lookup"><span data-stu-id="629f8-138">8</span></span>      |        |
| <span data-ttu-id="629f8-139">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="629f8-140">12</span><span class="sxs-lookup"><span data-stu-id="629f8-140">12</span></span>     |        |
| <span data-ttu-id="629f8-141">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="629f8-142">16</span><span class="sxs-lookup"><span data-stu-id="629f8-142">16</span></span>     |        |
| <span data-ttu-id="629f8-143">\_ярко- \_ альфа-версия GL</span><span class="sxs-lookup"><span data-stu-id="629f8-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="629f8-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="629f8-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="629f8-145">4</span><span class="sxs-lookup"><span data-stu-id="629f8-145">4</span></span>      | <span data-ttu-id="629f8-146">4</span><span class="sxs-lookup"><span data-stu-id="629f8-146">4</span></span>      |        |
| <span data-ttu-id="629f8-147">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="629f8-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="629f8-148">2</span><span class="sxs-lookup"><span data-stu-id="629f8-148">2</span></span>      | <span data-ttu-id="629f8-149">6</span><span class="sxs-lookup"><span data-stu-id="629f8-149">6</span></span>      |        |
| <span data-ttu-id="629f8-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="629f8-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="629f8-151">8</span><span class="sxs-lookup"><span data-stu-id="629f8-151">8</span></span>      | <span data-ttu-id="629f8-152">8</span><span class="sxs-lookup"><span data-stu-id="629f8-152">8</span></span>      |        |
| <span data-ttu-id="629f8-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="629f8-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="629f8-154">4</span><span class="sxs-lookup"><span data-stu-id="629f8-154">4</span></span>      | <span data-ttu-id="629f8-155">12</span><span class="sxs-lookup"><span data-stu-id="629f8-155">12</span></span>     |        |
| <span data-ttu-id="629f8-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="629f8-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="629f8-157">12</span><span class="sxs-lookup"><span data-stu-id="629f8-157">12</span></span>     | <span data-ttu-id="629f8-158">12</span><span class="sxs-lookup"><span data-stu-id="629f8-158">12</span></span>     |        |
| <span data-ttu-id="629f8-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="629f8-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="629f8-160">16</span><span class="sxs-lookup"><span data-stu-id="629f8-160">16</span></span>     | <span data-ttu-id="629f8-161">16</span><span class="sxs-lookup"><span data-stu-id="629f8-161">16</span></span>     |        |
| <span data-ttu-id="629f8-162">\_интенсивность GL</span><span class="sxs-lookup"><span data-stu-id="629f8-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="629f8-163">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="629f8-164">4</span><span class="sxs-lookup"><span data-stu-id="629f8-164">4</span></span>      |
| <span data-ttu-id="629f8-165">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="629f8-166">8</span><span class="sxs-lookup"><span data-stu-id="629f8-166">8</span></span>      |
| <span data-ttu-id="629f8-167">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="629f8-168">12</span><span class="sxs-lookup"><span data-stu-id="629f8-168">12</span></span>     |
| <span data-ttu-id="629f8-169">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="629f8-170">16</span><span class="sxs-lookup"><span data-stu-id="629f8-170">16</span></span>     |
| <span data-ttu-id="629f8-171">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="629f8-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="629f8-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="629f8-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="629f8-173">3</span><span class="sxs-lookup"><span data-stu-id="629f8-173">3</span></span>      | <span data-ttu-id="629f8-174">3</span><span class="sxs-lookup"><span data-stu-id="629f8-174">3</span></span>      | <span data-ttu-id="629f8-175">2</span><span class="sxs-lookup"><span data-stu-id="629f8-175">2</span></span>      |        |        |        |
| <span data-ttu-id="629f8-176">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-176">GL\_RGB4</span></span>                 | <span data-ttu-id="629f8-177">4</span><span class="sxs-lookup"><span data-stu-id="629f8-177">4</span></span>      | <span data-ttu-id="629f8-178">4</span><span class="sxs-lookup"><span data-stu-id="629f8-178">4</span></span>      | <span data-ttu-id="629f8-179">4</span><span class="sxs-lookup"><span data-stu-id="629f8-179">4</span></span>      |        |        |        |
| <span data-ttu-id="629f8-180">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-180">GL\_RGB5</span></span>                 | <span data-ttu-id="629f8-181">5</span><span class="sxs-lookup"><span data-stu-id="629f8-181">5</span></span>      | <span data-ttu-id="629f8-182">5</span><span class="sxs-lookup"><span data-stu-id="629f8-182">5</span></span>      | <span data-ttu-id="629f8-183">5</span><span class="sxs-lookup"><span data-stu-id="629f8-183">5</span></span>      |        |        |        |
| <span data-ttu-id="629f8-184">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-184">GL\_RGB8</span></span>                 | <span data-ttu-id="629f8-185">8</span><span class="sxs-lookup"><span data-stu-id="629f8-185">8</span></span>      | <span data-ttu-id="629f8-186">8</span><span class="sxs-lookup"><span data-stu-id="629f8-186">8</span></span>      | <span data-ttu-id="629f8-187">8</span><span class="sxs-lookup"><span data-stu-id="629f8-187">8</span></span>      |        |        |        |
| <span data-ttu-id="629f8-188">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-188">GL\_RGB10</span></span>                | <span data-ttu-id="629f8-189">10</span><span class="sxs-lookup"><span data-stu-id="629f8-189">10</span></span>     | <span data-ttu-id="629f8-190">10</span><span class="sxs-lookup"><span data-stu-id="629f8-190">10</span></span>     | <span data-ttu-id="629f8-191">10</span><span class="sxs-lookup"><span data-stu-id="629f8-191">10</span></span>     |        |        |        |
| <span data-ttu-id="629f8-192">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-192">GL\_RGB12</span></span>                | <span data-ttu-id="629f8-193">12</span><span class="sxs-lookup"><span data-stu-id="629f8-193">12</span></span>     | <span data-ttu-id="629f8-194">12</span><span class="sxs-lookup"><span data-stu-id="629f8-194">12</span></span>     | <span data-ttu-id="629f8-195">12</span><span class="sxs-lookup"><span data-stu-id="629f8-195">12</span></span>     |        |        |        |
| <span data-ttu-id="629f8-196">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-196">GL\_RGB16</span></span>                | <span data-ttu-id="629f8-197">16</span><span class="sxs-lookup"><span data-stu-id="629f8-197">16</span></span>     | <span data-ttu-id="629f8-198">16</span><span class="sxs-lookup"><span data-stu-id="629f8-198">16</span></span>     | <span data-ttu-id="629f8-199">16</span><span class="sxs-lookup"><span data-stu-id="629f8-199">16</span></span>     |        |        |        |
| <span data-ttu-id="629f8-200">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="629f8-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="629f8-201">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-201">GL\_RGBA2</span></span>                | <span data-ttu-id="629f8-202">2</span><span class="sxs-lookup"><span data-stu-id="629f8-202">2</span></span>      | <span data-ttu-id="629f8-203">2</span><span class="sxs-lookup"><span data-stu-id="629f8-203">2</span></span>      | <span data-ttu-id="629f8-204">2</span><span class="sxs-lookup"><span data-stu-id="629f8-204">2</span></span>      | <span data-ttu-id="629f8-205">2</span><span class="sxs-lookup"><span data-stu-id="629f8-205">2</span></span>      |        |        |
| <span data-ttu-id="629f8-206">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-206">GL\_RGBA4</span></span>                | <span data-ttu-id="629f8-207">4</span><span class="sxs-lookup"><span data-stu-id="629f8-207">4</span></span>      | <span data-ttu-id="629f8-208">4</span><span class="sxs-lookup"><span data-stu-id="629f8-208">4</span></span>      | <span data-ttu-id="629f8-209">4</span><span class="sxs-lookup"><span data-stu-id="629f8-209">4</span></span>      | <span data-ttu-id="629f8-210">4</span><span class="sxs-lookup"><span data-stu-id="629f8-210">4</span></span>      |        |        |
| <span data-ttu-id="629f8-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="629f8-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="629f8-212">5</span><span class="sxs-lookup"><span data-stu-id="629f8-212">5</span></span>      | <span data-ttu-id="629f8-213">5</span><span class="sxs-lookup"><span data-stu-id="629f8-213">5</span></span>      | <span data-ttu-id="629f8-214">5</span><span class="sxs-lookup"><span data-stu-id="629f8-214">5</span></span>      | <span data-ttu-id="629f8-215">1</span><span class="sxs-lookup"><span data-stu-id="629f8-215">1</span></span>      |        |        |
| <span data-ttu-id="629f8-216">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-216">GL\_RGBA8</span></span>                | <span data-ttu-id="629f8-217">8</span><span class="sxs-lookup"><span data-stu-id="629f8-217">8</span></span>      | <span data-ttu-id="629f8-218">8</span><span class="sxs-lookup"><span data-stu-id="629f8-218">8</span></span>      | <span data-ttu-id="629f8-219">8</span><span class="sxs-lookup"><span data-stu-id="629f8-219">8</span></span>      | <span data-ttu-id="629f8-220">8</span><span class="sxs-lookup"><span data-stu-id="629f8-220">8</span></span>      |        |        |
| <span data-ttu-id="629f8-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="629f8-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="629f8-222">10</span><span class="sxs-lookup"><span data-stu-id="629f8-222">10</span></span>     | <span data-ttu-id="629f8-223">10</span><span class="sxs-lookup"><span data-stu-id="629f8-223">10</span></span>     | <span data-ttu-id="629f8-224">10</span><span class="sxs-lookup"><span data-stu-id="629f8-224">10</span></span>     | <span data-ttu-id="629f8-225">2</span><span class="sxs-lookup"><span data-stu-id="629f8-225">2</span></span>      |        |        |
| <span data-ttu-id="629f8-226">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-226">GL\_RGBA12</span></span>               | <span data-ttu-id="629f8-227">12</span><span class="sxs-lookup"><span data-stu-id="629f8-227">12</span></span>     | <span data-ttu-id="629f8-228">12</span><span class="sxs-lookup"><span data-stu-id="629f8-228">12</span></span>     | <span data-ttu-id="629f8-229">12</span><span class="sxs-lookup"><span data-stu-id="629f8-229">12</span></span>     | <span data-ttu-id="629f8-230">12</span><span class="sxs-lookup"><span data-stu-id="629f8-230">12</span></span>     |        |        |
| <span data-ttu-id="629f8-231">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="629f8-231">GL\_RGBA16</span></span>               | <span data-ttu-id="629f8-232">16</span><span class="sxs-lookup"><span data-stu-id="629f8-232">16</span></span>     | <span data-ttu-id="629f8-233">16</span><span class="sxs-lookup"><span data-stu-id="629f8-233">16</span></span>     | <span data-ttu-id="629f8-234">16</span><span class="sxs-lookup"><span data-stu-id="629f8-234">16</span></span>     | <span data-ttu-id="629f8-235">16</span><span class="sxs-lookup"><span data-stu-id="629f8-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="629f8-236">*x*</span><span class="sxs-lookup"><span data-stu-id="629f8-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-237">Координата x окна в левом нижнем углу строки пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="629f8-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="629f8-238">*y*</span><span class="sxs-lookup"><span data-stu-id="629f8-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-239">Координата точки y окна для копирования левого нижнего угла строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="629f8-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="629f8-240">*width*</span><span class="sxs-lookup"><span data-stu-id="629f8-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-241">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="629f8-241">The width of the texture image.</span></span> <span data-ttu-id="629f8-242">Должен быть равен нулю или 2N + 2 (*border*) для некоторого целого числа *n*.</span><span class="sxs-lookup"><span data-stu-id="629f8-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="629f8-243">Высота изображения текстуры равна 1.</span><span class="sxs-lookup"><span data-stu-id="629f8-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="629f8-244">*цвета*</span><span class="sxs-lookup"><span data-stu-id="629f8-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="629f8-245">Ширина границы.</span><span class="sxs-lookup"><span data-stu-id="629f8-245">The width of the border.</span></span> <span data-ttu-id="629f8-246">Значение должно быть либо нулевым, либо 1.</span><span class="sxs-lookup"><span data-stu-id="629f8-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629f8-247">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="629f8-247">Return value</span></span>

<span data-ttu-id="629f8-248">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="629f8-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="629f8-249">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="629f8-249">Error codes</span></span>

<span data-ttu-id="629f8-250">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="629f8-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="629f8-251">Имя</span><span class="sxs-lookup"><span data-stu-id="629f8-251">Name</span></span>                                                                                                  | <span data-ttu-id="629f8-252">Значение</span><span class="sxs-lookup"><span data-stu-id="629f8-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="629f8-253"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="629f8-254">значение *цели* не было принято.</span><span class="sxs-lookup"><span data-stu-id="629f8-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="629f8-255"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="629f8-256">*уровень* был меньше нуля или больше log2 *Max*, где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="629f8-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="629f8-257"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="629f8-258">*граница* не равна нулю или 1.</span><span class="sxs-lookup"><span data-stu-id="629f8-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="629f8-259"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="629f8-260">*Ширина* была меньше нуля, больше 2 + ГК \_ максимальный \_ \_ размер текстуры или *Ширина* не может быть представлена как 2N + (*border*) для некоторого целого числа *n*.</span><span class="sxs-lookup"><span data-stu-id="629f8-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="629f8-261"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="629f8-262">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="629f8-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="629f8-263">Комментарии</span><span class="sxs-lookup"><span data-stu-id="629f8-263">Remarks</span></span>

<span data-ttu-id="629f8-264">Функция **glCopyTexImage1D** определяет одномерный рисунок текстуры, используя Пиксели из текущего буфера кадров, а не из основной памяти, как в случае с [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="629f8-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="629f8-265">При использовании уровня mipmap, указанного с *Level*, массивы текстур определяются как строка пикселей, выравниваемая в левом нижнем углу окна в координатах, заданных *x* и *y*, с длиной, равной *ширине* + 2 \* .</span><span class="sxs-lookup"><span data-stu-id="629f8-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="629f8-266">Внутренний формат массива текстуры указывается с помощью параметра *интерналформат* .</span><span class="sxs-lookup"><span data-stu-id="629f8-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="629f8-267">Функция **glCopyTexImage1D** обрабатывает пикселы в строке таким же образом, как и [**глкопипикселс**](glcopypixels.md), за исключением того, что перед завершающим преобразованием пикселов все значения компонентов пикселов записываются в диапазон \[ 0, 1 \] и преобразуются в внутренний формат текстуры для хранения в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="629f8-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="629f8-268">Порядок пикселей определяется с помощью более низких координат *x* , соответствующих более низким координатам текстуры.</span><span class="sxs-lookup"><span data-stu-id="629f8-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="629f8-269">Если любой из пикселов в заданной строке текущего буфера кадров находится за пределами окна, связанного с текущим контекстом отрисовки, то их значения не определены.</span><span class="sxs-lookup"><span data-stu-id="629f8-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="629f8-270">В списки вывода нельзя включать вызовы **glCopyTexImage1D** .</span><span class="sxs-lookup"><span data-stu-id="629f8-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="629f8-271">Функция **glCopyTexImage1D** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="629f8-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="629f8-272">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="629f8-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="629f8-273">Функции [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="629f8-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="629f8-274">Следующая функция получает сведения, связанные с **glCopyTexImage1D**:</span><span class="sxs-lookup"><span data-stu-id="629f8-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="629f8-275">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ 1d</span><span class="sxs-lookup"><span data-stu-id="629f8-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="629f8-276">Требования</span><span class="sxs-lookup"><span data-stu-id="629f8-276">Requirements</span></span>



| <span data-ttu-id="629f8-277">Требование</span><span class="sxs-lookup"><span data-stu-id="629f8-277">Requirement</span></span> | <span data-ttu-id="629f8-278">Значение</span><span class="sxs-lookup"><span data-stu-id="629f8-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="629f8-279">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="629f8-279">Minimum supported client</span></span><br/> | <span data-ttu-id="629f8-280">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="629f8-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="629f8-281">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="629f8-281">Minimum supported server</span></span><br/> | <span data-ttu-id="629f8-282">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="629f8-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="629f8-283">Заголовок</span><span class="sxs-lookup"><span data-stu-id="629f8-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="629f8-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="629f8-285">Библиотека</span><span class="sxs-lookup"><span data-stu-id="629f8-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="629f8-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="629f8-287">DLL</span><span class="sxs-lookup"><span data-stu-id="629f8-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="629f8-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629f8-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629f8-289">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="629f8-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629f8-290">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="629f8-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="629f8-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="629f8-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="629f8-292">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="629f8-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="629f8-293">**глфог**</span><span class="sxs-lookup"><span data-stu-id="629f8-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="629f8-294">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="629f8-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="629f8-295">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="629f8-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="629f8-296">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="629f8-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="629f8-297">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="629f8-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="629f8-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="629f8-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="629f8-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="629f8-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="629f8-300">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="629f8-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





