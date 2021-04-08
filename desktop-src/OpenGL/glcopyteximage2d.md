---
title: Функция glCopyTexImage2D (GL. h)
description: Функция glCopyTexImage2D копирует Пиксели из буфера кадров в изображение двухмерной текстуры.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- Функция glCopyTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892097"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="00717-104">Функция glCopyTexImage2D</span><span class="sxs-lookup"><span data-stu-id="00717-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="00717-105">Функция **glCopyTexImage2D** копирует Пиксели из буфера кадров в изображение двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="00717-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="00717-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00717-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="00717-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="00717-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00717-108">*target*</span><span class="sxs-lookup"><span data-stu-id="00717-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-109">Целевой объект, в который будут изменяться данные изображения.</span><span class="sxs-lookup"><span data-stu-id="00717-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="00717-110">Должно иметь значение \_ 2D текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="00717-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="00717-111">*level*</span><span class="sxs-lookup"><span data-stu-id="00717-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="00717-112">The level-of-detail number.</span></span> <span data-ttu-id="00717-113">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="00717-113">Level 0 is the base image.</span></span> <span data-ttu-id="00717-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="00717-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="00717-115">*интерналформат*</span><span class="sxs-lookup"><span data-stu-id="00717-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-116">Внутренний формат и разрешение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="00717-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="00717-117">Значения 1, 2, 3 и 4 не принимаются для *интерналформат*.</span><span class="sxs-lookup"><span data-stu-id="00717-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="00717-118">Параметр может принимать одно из следующих символьных значений.</span><span class="sxs-lookup"><span data-stu-id="00717-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="00717-119">Константа</span><span class="sxs-lookup"><span data-stu-id="00717-119">Constant</span></span>                 | <span data-ttu-id="00717-120">Биты R</span><span class="sxs-lookup"><span data-stu-id="00717-120">R Bits</span></span> | <span data-ttu-id="00717-121">Биты G</span><span class="sxs-lookup"><span data-stu-id="00717-121">G Bits</span></span> | <span data-ttu-id="00717-122">B бит</span><span class="sxs-lookup"><span data-stu-id="00717-122">B Bits</span></span> | <span data-ttu-id="00717-123">Биты</span><span class="sxs-lookup"><span data-stu-id="00717-123">A Bits</span></span> | <span data-ttu-id="00717-124">Биты L</span><span class="sxs-lookup"><span data-stu-id="00717-124">L Bits</span></span> | <span data-ttu-id="00717-125">Биты I</span><span class="sxs-lookup"><span data-stu-id="00717-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="00717-126">\_альфа-канал GL</span><span class="sxs-lookup"><span data-stu-id="00717-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="00717-127">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="00717-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="00717-128">4</span><span class="sxs-lookup"><span data-stu-id="00717-128">4</span></span>      |        |        |
| <span data-ttu-id="00717-129">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="00717-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="00717-130">8</span><span class="sxs-lookup"><span data-stu-id="00717-130">8</span></span>      |        |        |
| <span data-ttu-id="00717-131">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="00717-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="00717-132">12</span><span class="sxs-lookup"><span data-stu-id="00717-132">12</span></span>     |        |        |
| <span data-ttu-id="00717-133">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="00717-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="00717-134">16</span><span class="sxs-lookup"><span data-stu-id="00717-134">16</span></span>     |        |        |
| <span data-ttu-id="00717-135">\_светимость GL</span><span class="sxs-lookup"><span data-stu-id="00717-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="00717-136">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="00717-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="00717-137">4</span><span class="sxs-lookup"><span data-stu-id="00717-137">4</span></span>      |        |
| <span data-ttu-id="00717-138">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="00717-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="00717-139">8</span><span class="sxs-lookup"><span data-stu-id="00717-139">8</span></span>      |        |
| <span data-ttu-id="00717-140">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="00717-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="00717-141">12</span><span class="sxs-lookup"><span data-stu-id="00717-141">12</span></span>     |        |
| <span data-ttu-id="00717-142">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="00717-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="00717-143">16</span><span class="sxs-lookup"><span data-stu-id="00717-143">16</span></span>     |        |
| <span data-ttu-id="00717-144">\_ярко- \_ альфа-версия GL</span><span class="sxs-lookup"><span data-stu-id="00717-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="00717-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="00717-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="00717-146">4</span><span class="sxs-lookup"><span data-stu-id="00717-146">4</span></span>      | <span data-ttu-id="00717-147">4</span><span class="sxs-lookup"><span data-stu-id="00717-147">4</span></span>      |        |
| <span data-ttu-id="00717-148">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="00717-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="00717-149">2</span><span class="sxs-lookup"><span data-stu-id="00717-149">2</span></span>      | <span data-ttu-id="00717-150">6</span><span class="sxs-lookup"><span data-stu-id="00717-150">6</span></span>      |        |
| <span data-ttu-id="00717-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="00717-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="00717-152">8</span><span class="sxs-lookup"><span data-stu-id="00717-152">8</span></span>      | <span data-ttu-id="00717-153">8</span><span class="sxs-lookup"><span data-stu-id="00717-153">8</span></span>      |        |
| <span data-ttu-id="00717-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="00717-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="00717-155">4</span><span class="sxs-lookup"><span data-stu-id="00717-155">4</span></span>      | <span data-ttu-id="00717-156">12</span><span class="sxs-lookup"><span data-stu-id="00717-156">12</span></span>     |        |
| <span data-ttu-id="00717-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="00717-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="00717-158">12</span><span class="sxs-lookup"><span data-stu-id="00717-158">12</span></span>     | <span data-ttu-id="00717-159">12</span><span class="sxs-lookup"><span data-stu-id="00717-159">12</span></span>     |        |
| <span data-ttu-id="00717-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="00717-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="00717-161">16</span><span class="sxs-lookup"><span data-stu-id="00717-161">16</span></span>     | <span data-ttu-id="00717-162">16</span><span class="sxs-lookup"><span data-stu-id="00717-162">16</span></span>     |        |
| <span data-ttu-id="00717-163">\_интенсивность GL</span><span class="sxs-lookup"><span data-stu-id="00717-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="00717-164">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="00717-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="00717-165">4</span><span class="sxs-lookup"><span data-stu-id="00717-165">4</span></span>      |
| <span data-ttu-id="00717-166">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="00717-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="00717-167">8</span><span class="sxs-lookup"><span data-stu-id="00717-167">8</span></span>      |
| <span data-ttu-id="00717-168">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="00717-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="00717-169">12</span><span class="sxs-lookup"><span data-stu-id="00717-169">12</span></span>     |
| <span data-ttu-id="00717-170">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="00717-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="00717-171">16</span><span class="sxs-lookup"><span data-stu-id="00717-171">16</span></span>     |
| <span data-ttu-id="00717-172">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="00717-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="00717-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="00717-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="00717-174">3</span><span class="sxs-lookup"><span data-stu-id="00717-174">3</span></span>      | <span data-ttu-id="00717-175">3</span><span class="sxs-lookup"><span data-stu-id="00717-175">3</span></span>      | <span data-ttu-id="00717-176">2</span><span class="sxs-lookup"><span data-stu-id="00717-176">2</span></span>      |        |        |        |
| <span data-ttu-id="00717-177">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="00717-177">GL\_RGB4</span></span>                 | <span data-ttu-id="00717-178">4</span><span class="sxs-lookup"><span data-stu-id="00717-178">4</span></span>      | <span data-ttu-id="00717-179">4</span><span class="sxs-lookup"><span data-stu-id="00717-179">4</span></span>      | <span data-ttu-id="00717-180">4</span><span class="sxs-lookup"><span data-stu-id="00717-180">4</span></span>      |        |        |        |
| <span data-ttu-id="00717-181">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="00717-181">GL\_RGB5</span></span>                 | <span data-ttu-id="00717-182">5</span><span class="sxs-lookup"><span data-stu-id="00717-182">5</span></span>      | <span data-ttu-id="00717-183">5</span><span class="sxs-lookup"><span data-stu-id="00717-183">5</span></span>      | <span data-ttu-id="00717-184">5</span><span class="sxs-lookup"><span data-stu-id="00717-184">5</span></span>      |        |        |        |
| <span data-ttu-id="00717-185">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="00717-185">GL\_RGB8</span></span>                 | <span data-ttu-id="00717-186">8</span><span class="sxs-lookup"><span data-stu-id="00717-186">8</span></span>      | <span data-ttu-id="00717-187">8</span><span class="sxs-lookup"><span data-stu-id="00717-187">8</span></span>      | <span data-ttu-id="00717-188">8</span><span class="sxs-lookup"><span data-stu-id="00717-188">8</span></span>      |        |        |        |
| <span data-ttu-id="00717-189">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="00717-189">GL\_RGB10</span></span>                | <span data-ttu-id="00717-190">10</span><span class="sxs-lookup"><span data-stu-id="00717-190">10</span></span>     | <span data-ttu-id="00717-191">10</span><span class="sxs-lookup"><span data-stu-id="00717-191">10</span></span>     | <span data-ttu-id="00717-192">10</span><span class="sxs-lookup"><span data-stu-id="00717-192">10</span></span>     |        |        |        |
| <span data-ttu-id="00717-193">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="00717-193">GL\_RGB12</span></span>                | <span data-ttu-id="00717-194">12</span><span class="sxs-lookup"><span data-stu-id="00717-194">12</span></span>     | <span data-ttu-id="00717-195">12</span><span class="sxs-lookup"><span data-stu-id="00717-195">12</span></span>     | <span data-ttu-id="00717-196">12</span><span class="sxs-lookup"><span data-stu-id="00717-196">12</span></span>     |        |        |        |
| <span data-ttu-id="00717-197">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="00717-197">GL\_RGB16</span></span>                | <span data-ttu-id="00717-198">16</span><span class="sxs-lookup"><span data-stu-id="00717-198">16</span></span>     | <span data-ttu-id="00717-199">16</span><span class="sxs-lookup"><span data-stu-id="00717-199">16</span></span>     | <span data-ttu-id="00717-200">16</span><span class="sxs-lookup"><span data-stu-id="00717-200">16</span></span>     |        |        |        |
| <span data-ttu-id="00717-201">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="00717-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="00717-202">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="00717-202">GL\_RGBA2</span></span>                | <span data-ttu-id="00717-203">2</span><span class="sxs-lookup"><span data-stu-id="00717-203">2</span></span>      | <span data-ttu-id="00717-204">2</span><span class="sxs-lookup"><span data-stu-id="00717-204">2</span></span>      | <span data-ttu-id="00717-205">2</span><span class="sxs-lookup"><span data-stu-id="00717-205">2</span></span>      | <span data-ttu-id="00717-206">2</span><span class="sxs-lookup"><span data-stu-id="00717-206">2</span></span>      |        |        |
| <span data-ttu-id="00717-207">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="00717-207">GL\_RGBA4</span></span>                | <span data-ttu-id="00717-208">4</span><span class="sxs-lookup"><span data-stu-id="00717-208">4</span></span>      | <span data-ttu-id="00717-209">4</span><span class="sxs-lookup"><span data-stu-id="00717-209">4</span></span>      | <span data-ttu-id="00717-210">4</span><span class="sxs-lookup"><span data-stu-id="00717-210">4</span></span>      | <span data-ttu-id="00717-211">4</span><span class="sxs-lookup"><span data-stu-id="00717-211">4</span></span>      |        |        |
| <span data-ttu-id="00717-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="00717-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="00717-213">5</span><span class="sxs-lookup"><span data-stu-id="00717-213">5</span></span>      | <span data-ttu-id="00717-214">5</span><span class="sxs-lookup"><span data-stu-id="00717-214">5</span></span>      | <span data-ttu-id="00717-215">5</span><span class="sxs-lookup"><span data-stu-id="00717-215">5</span></span>      | <span data-ttu-id="00717-216">1</span><span class="sxs-lookup"><span data-stu-id="00717-216">1</span></span>      |        |        |
| <span data-ttu-id="00717-217">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="00717-217">GL\_RGBA8</span></span>                | <span data-ttu-id="00717-218">8</span><span class="sxs-lookup"><span data-stu-id="00717-218">8</span></span>      | <span data-ttu-id="00717-219">8</span><span class="sxs-lookup"><span data-stu-id="00717-219">8</span></span>      | <span data-ttu-id="00717-220">8</span><span class="sxs-lookup"><span data-stu-id="00717-220">8</span></span>      | <span data-ttu-id="00717-221">8</span><span class="sxs-lookup"><span data-stu-id="00717-221">8</span></span>      |        |        |
| <span data-ttu-id="00717-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="00717-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="00717-223">10</span><span class="sxs-lookup"><span data-stu-id="00717-223">10</span></span>     | <span data-ttu-id="00717-224">10</span><span class="sxs-lookup"><span data-stu-id="00717-224">10</span></span>     | <span data-ttu-id="00717-225">10</span><span class="sxs-lookup"><span data-stu-id="00717-225">10</span></span>     | <span data-ttu-id="00717-226">2</span><span class="sxs-lookup"><span data-stu-id="00717-226">2</span></span>      |        |        |
| <span data-ttu-id="00717-227">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="00717-227">GL\_RGBA12</span></span>               | <span data-ttu-id="00717-228">12</span><span class="sxs-lookup"><span data-stu-id="00717-228">12</span></span>     | <span data-ttu-id="00717-229">12</span><span class="sxs-lookup"><span data-stu-id="00717-229">12</span></span>     | <span data-ttu-id="00717-230">12</span><span class="sxs-lookup"><span data-stu-id="00717-230">12</span></span>     | <span data-ttu-id="00717-231">12</span><span class="sxs-lookup"><span data-stu-id="00717-231">12</span></span>     |        |        |
| <span data-ttu-id="00717-232">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="00717-232">GL\_RGBA16</span></span>               | <span data-ttu-id="00717-233">16</span><span class="sxs-lookup"><span data-stu-id="00717-233">16</span></span>     | <span data-ttu-id="00717-234">16</span><span class="sxs-lookup"><span data-stu-id="00717-234">16</span></span>     | <span data-ttu-id="00717-235">16</span><span class="sxs-lookup"><span data-stu-id="00717-235">16</span></span>     | <span data-ttu-id="00717-236">16</span><span class="sxs-lookup"><span data-stu-id="00717-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="00717-237">*x*</span><span class="sxs-lookup"><span data-stu-id="00717-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-238">Координата x окна в левом нижнем углу прямоугольной области пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="00717-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="00717-239">*y*</span><span class="sxs-lookup"><span data-stu-id="00717-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-240">Координата точки y окна для копирования левого нижнего угла прямоугольной области пикселей.</span><span class="sxs-lookup"><span data-stu-id="00717-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="00717-241">*width*</span><span class="sxs-lookup"><span data-stu-id="00717-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-242">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="00717-242">The width of the texture image.</span></span> <span data-ttu-id="00717-243">\*Для некоторого целого числа *n* должно быть 2N + 2 *border* .</span><span class="sxs-lookup"><span data-stu-id="00717-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="00717-244">*height*</span><span class="sxs-lookup"><span data-stu-id="00717-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-245">Высота изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="00717-245">The height of the texture image.</span></span> <span data-ttu-id="00717-246">\*Для некоторого целого числа *n* должно быть 2N + 2 *border* .</span><span class="sxs-lookup"><span data-stu-id="00717-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="00717-247">*цвета*</span><span class="sxs-lookup"><span data-stu-id="00717-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="00717-248">Ширина границы.</span><span class="sxs-lookup"><span data-stu-id="00717-248">The width of the border.</span></span> <span data-ttu-id="00717-249">Значение должно быть либо нулевым, либо 1.</span><span class="sxs-lookup"><span data-stu-id="00717-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00717-250">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00717-250">Return value</span></span>

<span data-ttu-id="00717-251">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="00717-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00717-252">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="00717-252">Error codes</span></span>

<span data-ttu-id="00717-253">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="00717-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="00717-254">Имя</span><span class="sxs-lookup"><span data-stu-id="00717-254">Name</span></span>                                                                                                  | <span data-ttu-id="00717-255">Значение</span><span class="sxs-lookup"><span data-stu-id="00717-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00717-256"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="00717-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="00717-257">значение *цели* не было принято.</span><span class="sxs-lookup"><span data-stu-id="00717-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="00717-258"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="00717-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="00717-259">*уровень* был меньше нуля или больше log2 *Max*, где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="00717-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="00717-260"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="00717-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="00717-261">*граница* не равна нулю или 1.</span><span class="sxs-lookup"><span data-stu-id="00717-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="00717-262"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="00717-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="00717-263">*Ширина* была меньше нуля, больше 2 + ГК \_ максимальный \_ \_ размер текстуры или *Ширина* не может быть представлена как 2N + 2 \*  для некоторого целого числа *n*.</span><span class="sxs-lookup"><span data-stu-id="00717-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="00717-264"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="00717-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="00717-265">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="00717-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="00717-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00717-266">Remarks</span></span>

<span data-ttu-id="00717-267">Функция **glCopyTexImage2D** определяет двухмерный рисунок текстуры, используя Пиксели из текущего буфера кадров, а не из основной памяти, как в случае с [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="00717-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="00717-268">При использовании уровня mipmap, указанного с *Level*, массивы текстур определяются в виде прямоугольника пикселей с нижним левым углом, расположенными в координатах *x* и *y*, ширины, равной *ширине* + (2 \* *границы*), и высоты, равной *высоте* + (2 \* *границы*).</span><span class="sxs-lookup"><span data-stu-id="00717-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="00717-269">Внутренний формат массива текстуры указывается с помощью параметра *интерналформат* .</span><span class="sxs-lookup"><span data-stu-id="00717-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="00717-270">Функция **glCopyTexImage2D** обрабатывает Пиксели в строке таким же образом, как и [**глкопипикселс**](glcopypixels.md) , за исключением того, что перед завершающим преобразованием пикселов все значения компонентов пикселов записываются в диапазон \[ 0, 1 \] и преобразуются в внутренний формат текстуры для хранения в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="00717-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="00717-271">Порядок пикселей определяется с помощью более низких координат *x* и *y* , соответствующих нижним координатам *s* и *t* текстур.</span><span class="sxs-lookup"><span data-stu-id="00717-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="00717-272">Если любой из пикселов в заданной строке текущего буфера кадров находится за пределами окна, связанного с текущим контекстом отрисовки, то их значения не определены.</span><span class="sxs-lookup"><span data-stu-id="00717-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="00717-273">В списки вывода нельзя включать вызовы **glCopyTexImage2D** .</span><span class="sxs-lookup"><span data-stu-id="00717-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="00717-274">Функция **glCopyTexImage2D** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="00717-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="00717-275">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="00717-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="00717-276">Функции [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="00717-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="00717-277">Следующая функция получает сведения, связанные с **glCopyTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="00717-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="00717-278">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстуры \_ 2D</span><span class="sxs-lookup"><span data-stu-id="00717-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="00717-279">Требования</span><span class="sxs-lookup"><span data-stu-id="00717-279">Requirements</span></span>



| <span data-ttu-id="00717-280">Требование</span><span class="sxs-lookup"><span data-stu-id="00717-280">Requirement</span></span> | <span data-ttu-id="00717-281">Значение</span><span class="sxs-lookup"><span data-stu-id="00717-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00717-282">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00717-282">Minimum supported client</span></span><br/> | <span data-ttu-id="00717-283">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00717-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="00717-284">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00717-284">Minimum supported server</span></span><br/> | <span data-ttu-id="00717-285">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00717-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00717-286">Заголовок</span><span class="sxs-lookup"><span data-stu-id="00717-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="00717-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="00717-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="00717-288">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00717-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="00717-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00717-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00717-290">DLL</span><span class="sxs-lookup"><span data-stu-id="00717-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00717-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00717-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00717-292">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00717-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00717-293">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="00717-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="00717-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="00717-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="00717-295">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="00717-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="00717-296">**гленд**</span><span class="sxs-lookup"><span data-stu-id="00717-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="00717-297">**глфог**</span><span class="sxs-lookup"><span data-stu-id="00717-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="00717-298">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="00717-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="00717-299">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="00717-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="00717-300">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="00717-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="00717-301">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="00717-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="00717-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="00717-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="00717-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="00717-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="00717-304">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="00717-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





