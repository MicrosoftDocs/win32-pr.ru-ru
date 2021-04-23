---
description: В этом разделе указаны форматы ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 12,1.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Поддержка форматов для оборудования Direct3D с уровнем компонентов 12.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d20b00a2cfb5b0343a2ebb1a56a1253ddd1966
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805182"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a><span data-ttu-id="68b50-103">Поддержка форматов для оборудования Direct3D с уровнем компонентов 12.1</span><span class="sxs-lookup"><span data-stu-id="68b50-103">Format support for Direct3D Feature Level 12.1 hardware</span></span>

<span data-ttu-id="68b50-104">В этом разделе указаны форматы ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 12,1.</span><span class="sxs-lookup"><span data-stu-id="68b50-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 12.1 hardware.</span></span>

<span data-ttu-id="68b50-105">В таблице приводится сводка по поддержке функций с использованием следующего ключа.</span><span class="sxs-lookup"><span data-stu-id="68b50-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="68b50-106">Символ</span><span class="sxs-lookup"><span data-stu-id="68b50-106">Symbol</span></span>                            | <span data-ttu-id="68b50-107">Описание</span><span class="sxs-lookup"><span data-stu-id="68b50-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="68b50-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="68b50-108">_ *-*\*</span></span>                             | <span data-ttu-id="68b50-109">Не разрешено или недоступно.</span><span class="sxs-lookup"><span data-stu-id="68b50-109">Disallowed or not available.</span></span>                                                  |
| ![обязательно](images/letter-r.jpg)  | <span data-ttu-id="68b50-111">Требуется поддержка оборудования.</span><span class="sxs-lookup"><span data-stu-id="68b50-111">Hardware support is required.</span></span>                                                 |
| ![необязательно](images/letter-o.jpg)  | <span data-ttu-id="68b50-113">Аппаратная поддержка необязательно. формат аппаратного ускорения может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="68b50-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![зависимых](images/letter-d.jpg) | <span data-ttu-id="68b50-115">Требуется, если поддерживается дополнительная функция.</span><span class="sxs-lookup"><span data-stu-id="68b50-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="68b50-116">Этот раздел содержит раздел для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="68b50-116">This topic contains a section per format.</span></span> <span data-ttu-id="68b50-117">*Цель* формата (таблицы содержат по одной строке на каждый целевой объект) может быть типом ресурса, встроенной функцией HLSL или определенной функциональностью, зависящей от конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="68b50-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="68b50-118">Чтобы программно проверить поддержку формата в D3D11 и D3D12, обратитесь к статье [Проверка поддержки аппаратных компонентов](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="68b50-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="68b50-119">Числа форматов в основном, но не все, в возрастающем числовом порядке &mdash; , некоторые из них имеют нечисловой порядок и перечислены вместе с другими соответствующими форматами.</span><span class="sxs-lookup"><span data-stu-id="68b50-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="68b50-120">Обратите внимание, что *тип* в имени формата может означать *частичную* типизацию, а не строго типизированный (см. раздел [Format Notes](#format-notes) в конце раздела).</span><span class="sxs-lookup"><span data-stu-id="68b50-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="68b50-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="68b50-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="68b50-122">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-122">Target</span></span> | <span data-ttu-id="68b50-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-123">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-124">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-125">0</span><span class="sxs-lookup"><span data-stu-id="68b50-125">0</span></span> |
| <span data-ttu-id="68b50-126">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-126">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-128">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-128">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-130">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-131">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-132">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-133">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-134">Texture2D</span></span> | \- |
| <span data-ttu-id="68b50-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-135">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-136">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-137">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-137">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-138">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-139">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-139">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-140">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-140">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-141">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-142">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-142">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-143">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-144">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-144">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-145">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-146">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-147">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-148">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-149">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-150">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-150">Structured UAV and SRV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-152">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-152">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-153">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-153">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-154">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-154">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-155">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-155">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-156">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-156">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-157">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-157">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-158">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-158">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-159">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-159">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-160">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-160">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-161">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-161">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-163">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-163">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-164">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-164">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-165">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-165">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-166">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-166">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-167">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-167">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-168">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-168">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-169">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-169">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-170">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-171">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-172">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-173">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-173">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-174">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-174">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-175">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-175">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="68b50-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>ПК</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="68b50-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="68b50-178">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-178">Target</span></span> | <span data-ttu-id="68b50-179">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-179">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-180">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-180">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-181">128</span><span class="sxs-lookup"><span data-stu-id="68b50-181">128</span></span> |
| <span data-ttu-id="68b50-182">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-182">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-184">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-184">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-185">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-185">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-186">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-186">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-187">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-187">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-188">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-190">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-192">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-194">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-196">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-196">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-197">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-197">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-198">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-198">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-199">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-199">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-200">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-200">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-201">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-201">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-202">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-204">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-204">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-205">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-205">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-206">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-207">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-208">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-209">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-210">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-211">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-211">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-212">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-213">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-214">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-215">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-216">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-217">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-218">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-219">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-220">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-220">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-222">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-223">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-224">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-225">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-226">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-226">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-227">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-228">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-228">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-230">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-231">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-232">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-233">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-233">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-235">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-235">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-236">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-236">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="68b50-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="68b50-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="68b50-239">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-239">Target</span></span> | <span data-ttu-id="68b50-240">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-240">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-241">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-241">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-242">128</span><span class="sxs-lookup"><span data-stu-id="68b50-242">128</span></span> |
| <span data-ttu-id="68b50-243">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-243">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-245">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-245">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-247">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-247">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-249">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-250">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-250">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-252">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-252">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-254">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-256">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-256">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-258">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-258">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-260">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-260">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-262">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-262">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-264">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-264">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-265">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-265">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-266">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-266">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-268">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-268">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-269">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-269">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-271">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-271">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-273">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-273">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-275">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-275">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-277">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-277">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-278">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-278">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-279">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-279">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-280">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-280">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-281">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-281">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-283">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-283">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-285">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-285">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-287">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-288">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-289">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-289">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-290">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-291">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-291">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-292">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-292">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-293">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-293">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-295">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-295">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-297">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-297">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-299">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-299">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-301">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-301">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-303">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-303">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-305">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-306">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-306">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-308">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-309">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-310">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-311">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-311">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-313">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-313">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-314">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-314">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="68b50-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="68b50-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="68b50-317">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-317">Target</span></span> | <span data-ttu-id="68b50-318">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-318">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-319">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-320">128</span><span class="sxs-lookup"><span data-stu-id="68b50-320">128</span></span> |
| <span data-ttu-id="68b50-321">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-321">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-323">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-323">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-325">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-325">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-327">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-328">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-328">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-330">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-332">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-332">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-334">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-334">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-336">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-338">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-338">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-340">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-340">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-341">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-341">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-342">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-342">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-343">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-343">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-344">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-345">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-347">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-348">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-348">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-350">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-351">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-351">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-353">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-353">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-354">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-354">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-355">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-355">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-356">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-356">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-358">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-358">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-360">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-360">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-362">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-363">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-364">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-365">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-366">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-366">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-367">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-367">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-368">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-368">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-370">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-370">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-372">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-372">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-374">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-374">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-376">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-377">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-377">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-379">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-380">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-380">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-382">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-382">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-383">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-383">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-384">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-384">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-385">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-385">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-387">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-387">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-388">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-388">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="68b50-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="68b50-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="68b50-391">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-391">Target</span></span> | <span data-ttu-id="68b50-392">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-392">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-393">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-394">128</span><span class="sxs-lookup"><span data-stu-id="68b50-394">128</span></span> |
| <span data-ttu-id="68b50-395">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-395">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-397">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-397">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-399">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-399">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-401">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-402">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-402">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-404">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-404">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-406">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-406">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-408">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-408">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-410">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-412">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-412">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-414">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-414">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-415">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-415">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-416">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-416">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-417">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-417">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-418">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-418">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-419">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-419">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-421">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-421">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-422">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-422">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-424">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-424">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-425">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-425">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-426">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-426">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-427">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-427">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-428">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-428">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-429">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-429">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-431">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-431">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-433">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-433">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-435">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-435">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-436">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-436">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-437">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-437">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-438">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-438">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-439">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-439">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-440">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-440">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-441">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-441">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-443">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-443">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-445">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-445">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-447">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-447">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-449">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-449">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-450">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-450">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-452">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-452">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-453">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-453">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-455">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-455">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-456">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-456">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-457">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-457">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-458">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-458">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-460">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-460">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-461">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-461">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="68b50-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>ПК</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="68b50-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="68b50-464">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-464">Target</span></span> | <span data-ttu-id="68b50-465">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-465">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-466">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-466">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-467">96</span><span class="sxs-lookup"><span data-stu-id="68b50-467">96</span></span> |
| <span data-ttu-id="68b50-468">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-468">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-470">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-470">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-471">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-471">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-472">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-472">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-473">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-473">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-474">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-474">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-476">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-476">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-478">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-478">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-480">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-480">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-482">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-482">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-483">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-484">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-484">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-485">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-485">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-486">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-486">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-487">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-487">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-488">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-490">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-490">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-491">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-491">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-492">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-492">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-493">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-493">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-494">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-494">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-495">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-495">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-496">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-496">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-497">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-497">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-498">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-498">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-499">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-499">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-500">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-501">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-502">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-503">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-504">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-505">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-506">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-506">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-508">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-508">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-509">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-509">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-510">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-510">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-511">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-511">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-512">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-512">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-513">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-513">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-514">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-514">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-516">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-516">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-517">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-517">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-518">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-518">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-519">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-519">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-520">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-520">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-521">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-521">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="68b50-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="68b50-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="68b50-523">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-523">Target</span></span> | <span data-ttu-id="68b50-524">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-524">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-525">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-525">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-526">96</span><span class="sxs-lookup"><span data-stu-id="68b50-526">96</span></span> |
| <span data-ttu-id="68b50-527">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-527">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-529">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-529">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-531">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-531">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-533">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-533">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-534">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-534">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-536">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-538">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-540">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-542">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-544">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-544">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-546">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-546">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-548">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-548">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-549">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-549">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-550">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-550">Shader gather4</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-552">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-552">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-553">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-555">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-555">Mipmap Auto- Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-557">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-557">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-559">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-559">Blendable RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-561">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-562">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-563">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-564">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-565">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-565">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-566">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-567">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-568">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-569">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-570">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-571">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-572">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-573">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-574">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-574">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-576">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-576">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-578">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-578">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-580">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-580">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-582">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-582">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-584">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-584">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-586">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-586">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-587">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-587">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-589">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-590">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-591">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-592">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-593">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-593">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-594">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="68b50-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="68b50-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="68b50-596">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-596">Target</span></span> | <span data-ttu-id="68b50-597">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-597">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-598">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-599">96</span><span class="sxs-lookup"><span data-stu-id="68b50-599">96</span></span> |
| <span data-ttu-id="68b50-600">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-600">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-602">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-602">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-604">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-604">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-606">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-606">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-607">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-607">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-609">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-609">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-611">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-613">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-613">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-615">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-615">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-617">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-617">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-619">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-620">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-620">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-621">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-621">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-622">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-622">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-623">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-623">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-624">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-626">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-626">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-627">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-627">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-629">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-629">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-630">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-630">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-632">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-633">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-634">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-635">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-635">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-636">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-637">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-638">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-639">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-640">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-640">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-641">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-642">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-642">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-643">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-643">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-644">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-644">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-646">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-646">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-648">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-648">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-650">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-650">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-652">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-653">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-653">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-655">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-656">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-656">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-658">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-659">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-660">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-661">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-661">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-662">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-662">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-663">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="68b50-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="68b50-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="68b50-665">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-665">Target</span></span> | <span data-ttu-id="68b50-666">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-666">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-667">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-668">96</span><span class="sxs-lookup"><span data-stu-id="68b50-668">96</span></span> |
| <span data-ttu-id="68b50-669">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-669">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-671">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-671">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-673">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-673">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-675">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-675">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-676">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-676">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-678">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-678">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-680">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-680">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-682">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-682">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-684">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-686">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-686">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-688">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-688">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-689">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-689">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-690">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-690">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-691">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-691">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-692">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-692">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-693">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-695">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-695">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-696">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-696">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-698">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-698">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-699">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-699">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-700">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-700">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-701">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-701">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-702">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-702">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-703">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-703">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-704">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-704">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-705">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-705">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-706">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-706">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-707">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-707">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-708">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-708">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-709">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-709">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-710">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-710">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-711">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-711">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-712">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-712">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-714">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-714">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-716">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-716">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="68b50-718">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-718">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-720">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-720">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-721">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-721">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-723">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-723">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-724">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-724">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-726">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-726">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-727">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-727">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-728">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-728">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-729">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-729">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-730">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-730">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-731">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-731">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="68b50-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>ПК</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="68b50-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="68b50-733">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-733">Target</span></span> | <span data-ttu-id="68b50-734">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-734">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-735">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-735">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-736">64</span><span class="sxs-lookup"><span data-stu-id="68b50-736">64</span></span> |
| <span data-ttu-id="68b50-737">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-737">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-739">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-739">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-740">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-741">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-742">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-743">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-745">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-745">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-747">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-747">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-749">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-749">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-751">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-751">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-752">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-752">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-753">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-753">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-754">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-754">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-755">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-755">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-756">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-756">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-757">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-757">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-759">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-759">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-760">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-760">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-761">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-761">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-762">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-762">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-763">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-763">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-764">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-764">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-765">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-765">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-766">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-766">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-767">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-767">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-768">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-768">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-769">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-769">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-770">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-770">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-771">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-771">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-772">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-772">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-773">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-773">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-774">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-774">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-775">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-775">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-777">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-777">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-778">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-778">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-779">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-779">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-780">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-780">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-781">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-781">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-782">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-782">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-783">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-783">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-785">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-785">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-786">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-786">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-787">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-787">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-788">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-788">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-790">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-790">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-791">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-791">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="68b50-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="68b50-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="68b50-794">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-794">Target</span></span> | <span data-ttu-id="68b50-795">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-795">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-796">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-797">64</span><span class="sxs-lookup"><span data-stu-id="68b50-797">64</span></span> |
| <span data-ttu-id="68b50-798">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-798">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-800">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-800">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-802">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-802">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-804">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-805">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-806">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-808">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-810">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-812">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-814">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-814">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-816">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-816">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-818">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-818">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-819">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-819">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-820">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-820">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-822">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-822">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-823">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-823">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-825">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-825">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-827">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-827">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-829">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-829">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-831">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-832">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-833">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-834">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-835">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-835">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-837">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-837">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-839">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-839">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-841">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-842">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-843">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-844">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-845">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-846">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-847">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-847">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-849">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-849">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-851">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-851">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-853">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-853">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-855">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-855">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-857">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-857">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-859">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-859">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-861">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-861">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-863">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-864">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-864">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-866">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-866">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-868">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-868">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-870">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-871">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-871">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="68b50-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="68b50-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="68b50-874">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-874">Target</span></span> | <span data-ttu-id="68b50-875">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-875">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-876">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-877">64</span><span class="sxs-lookup"><span data-stu-id="68b50-877">64</span></span> |
| <span data-ttu-id="68b50-878">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-878">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-880">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-880">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-882">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-882">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-884">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-885">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-886">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-888">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-890">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-892">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-894">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-894">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-896">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-896">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-898">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-898">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-899">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-899">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-900">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-900">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-902">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-902">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-903">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-905">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-905">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-907">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-907">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-909">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-909">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-911">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-912">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-913">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-914">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-915">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-915">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-917">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-917">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-919">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-919">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-921">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-922">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-923">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-924">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-925">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-925">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-926">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-926">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-927">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-927">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-929">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-929">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-931">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-931">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-933">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-933">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-935">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-935">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-937">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-937">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-939">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-939">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-940">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-940">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-942">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-943">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-944">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-945">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-945">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-947">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-947">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-948">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-948">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="68b50-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="68b50-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="68b50-951">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-951">Target</span></span> | <span data-ttu-id="68b50-952">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-952">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-953">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-953">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-954">64</span><span class="sxs-lookup"><span data-stu-id="68b50-954">64</span></span> |
| <span data-ttu-id="68b50-955">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-955">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-957">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-957">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-959">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-959">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-961">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-961">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-962">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-962">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-963">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-963">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-965">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-965">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-967">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-967">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-969">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-969">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-971">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-971">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-973">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-973">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-974">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-974">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-975">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-975">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-976">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-976">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-977">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-978">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-980">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-980">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-981">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-981">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-983">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-983">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-984">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-984">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-986">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-986">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-987">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-987">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-988">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-988">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-989">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-989">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-991">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-991">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-993">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-993">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-995">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-995">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-996">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-996">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-997">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-997">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-998">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-998">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-999">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-999">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1000">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1000">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1001">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1001">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1003">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1003">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1005">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1005">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1007">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1007">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1009">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1010">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1010">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1012">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1012">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1013">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1013">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1015">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1015">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1016">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1016">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1017">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1017">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1018">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1018">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1020">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1020">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1021">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1021">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="68b50-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="68b50-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="68b50-1024">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1024">Target</span></span> | <span data-ttu-id="68b50-1025">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1025">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1026">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1026">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1027">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1027">64</span></span> |
| <span data-ttu-id="68b50-1028">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1028">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1030">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1030">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1032">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1032">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1034">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1035">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1036">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1038">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1040">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1042">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1042">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1044">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1044">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1046">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1046">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1048">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1048">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1049">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1049">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1050">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1050">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1052">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1052">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1053">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1055">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1055">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1057">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1057">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1059">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1059">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1061">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1061">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1062">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1062">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1063">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1063">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1064">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1064">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1065">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1065">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1067">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1067">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1069">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1069">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1071">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1071">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1072">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1072">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1073">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1073">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1074">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1074">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1075">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1075">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1076">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1076">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1077">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1077">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1079">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1079">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1081">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1081">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1083">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1083">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1085">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1085">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1087">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1087">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1089">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1089">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1090">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1090">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1092">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1092">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1093">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1093">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1094">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1094">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1095">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1095">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1097">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1097">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1098">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1098">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="68b50-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="68b50-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="68b50-1101">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1101">Target</span></span> | <span data-ttu-id="68b50-1102">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1102">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1103">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1103">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1104">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1104">64</span></span> |
| <span data-ttu-id="68b50-1105">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1105">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1107">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1107">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1109">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1109">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1111">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1111">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1112">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1112">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1113">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1113">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1115">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1117">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1117">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1119">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1119">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1121">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1121">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1123">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1123">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1124">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1124">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1125">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1125">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1126">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1126">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1127">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1127">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1128">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1128">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1130">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1130">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1131">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1131">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1133">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1133">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1134">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1134">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1135">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1135">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1136">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1136">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1137">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1137">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1138">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1138">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1140">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1140">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1142">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1142">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1144">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1144">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1145">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1145">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1146">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1146">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1147">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1147">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1148">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1148">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1149">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1149">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1150">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1150">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1152">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1152">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1154">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1154">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1156">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1156">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1158">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1158">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1159">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1159">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1161">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1162">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1162">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1164">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1164">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1165">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1165">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1166">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1166">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1167">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1167">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1169">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1169">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1170">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1170">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="68b50-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>ПК</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="68b50-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="68b50-1173">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1173">Target</span></span> | <span data-ttu-id="68b50-1174">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1174">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1175">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1175">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1176">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1176">64</span></span> |
| <span data-ttu-id="68b50-1177">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1177">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1179">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1179">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1180">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1180">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1181">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1181">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1182">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1182">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1183">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1183">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1185">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1185">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1187">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1187">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1189">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1191">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1191">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-1192">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1193">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1194">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1195">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1195">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1196">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1197">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1199">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1200">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1200">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1201">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1202">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1203">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1204">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1205">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1206">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1206">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1207">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1208">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1209">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1210">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1211">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1212">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1213">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1213">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1214">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1214">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1215">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1215">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1217">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1218">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1219">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1220">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1221">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1221">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-1222">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1223">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1223">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1225">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1225">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1226">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1226">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1227">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1227">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1228">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1228">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1229">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1229">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1230">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1230">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="68b50-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="68b50-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="68b50-1233">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1233">Target</span></span> | <span data-ttu-id="68b50-1234">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1234">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1235">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1235">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1236">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1236">64</span></span> |
| <span data-ttu-id="68b50-1237">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1237">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1239">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1239">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1241">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1241">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1243">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1244">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1244">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1246">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1246">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1248">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1250">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1252">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1254">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1254">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1256">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1256">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1258">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1258">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1259">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1259">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1260">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1260">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1262">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1262">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1263">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1265">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1265">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1267">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1267">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1269">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1269">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1271">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1272">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1273">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1274">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1275">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1275">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1277">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1277">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1279">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1279">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1281">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1281">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1282">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1282">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1283">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1283">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1284">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1284">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1285">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1285">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1286">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1286">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1287">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1287">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1289">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1289">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1291">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1291">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1293">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1293">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1295">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1295">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1297">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1297">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1299">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1299">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1300">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1300">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1302">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1302">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1303">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1303">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1304">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1304">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1305">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1305">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1306">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1306">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1307">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1307">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="68b50-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="68b50-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="68b50-1310">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1310">Target</span></span> | <span data-ttu-id="68b50-1311">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1311">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1312">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1312">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1313">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1313">64</span></span> |
| <span data-ttu-id="68b50-1314">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1314">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1316">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1316">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1318">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1318">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1320">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1321">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1321">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1323">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1325">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1325">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1327">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1327">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1329">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1329">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1331">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1331">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1333">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1334">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1334">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1335">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1335">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1336">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1336">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1337">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1337">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1338">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1340">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1340">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1341">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1341">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1343">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1343">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1344">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1344">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1346">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1346">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1347">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1347">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1348">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1348">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1349">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1349">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1351">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1351">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1353">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1353">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1355">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1356">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1357">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1357">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1358">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1359">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1359">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1360">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1360">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1361">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1361">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1363">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1363">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1365">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1365">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1367">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1367">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1369">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1370">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1370">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1372">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1373">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1373">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1375">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1376">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1377">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1378">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1379">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1379">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1380">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1380">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="68b50-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="68b50-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="68b50-1383">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1383">Target</span></span> | <span data-ttu-id="68b50-1384">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1384">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1385">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1386">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1386">64</span></span> |
| <span data-ttu-id="68b50-1387">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1387">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1389">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1389">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1391">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1391">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1393">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1394">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1394">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1396">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1396">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1398">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1400">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1400">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1402">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1402">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1404">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1404">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1406">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1407">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1407">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1408">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1408">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1409">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1410">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1410">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1411">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1413">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1413">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1414">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1414">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1416">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1417">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1418">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1419">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1420">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1421">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1421">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1423">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1423">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1425">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1425">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1427">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1427">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1428">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1428">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1429">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1429">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1430">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1430">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1431">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1431">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1432">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1432">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1433">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1433">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1435">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1435">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1437">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1437">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1439">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1439">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1441">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1442">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1442">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1444">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1444">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1445">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1445">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1447">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1447">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1448">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1448">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1449">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1449">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1450">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1450">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1451">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1451">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1452">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1452">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a><span data-ttu-id="68b50-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="68b50-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span></span>
| <span data-ttu-id="68b50-1455">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1455">Target</span></span> | <span data-ttu-id="68b50-1456">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1456">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1457">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1457">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1458">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1458">64</span></span> |
| <span data-ttu-id="68b50-1459">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1459">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1461">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1461">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1462">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1462">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1463">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1464">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1465">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1467">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1469">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-1470">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1470">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1472">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1472">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-1473">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1474">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1474">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1475">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1475">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1476">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1476">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1477">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1477">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1478">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1480">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1480">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1481">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1481">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1482">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1482">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1483">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1483">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1484">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1484">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1485">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1485">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1486">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1486">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1487">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1487">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1488">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1488">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1489">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1489">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1490">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1490">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1491">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1491">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1492">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1492">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1493">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1493">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1494">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1494">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1495">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1495">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1496">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1496">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1498">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1498">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1499">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1499">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1500">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1500">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1501">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1501">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1502">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1502">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-1503">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1503">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1504">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1504">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1506">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1506">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1507">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1507">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1508">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1508">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1509">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1509">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1510">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1510">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1511">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1511">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a><span data-ttu-id="68b50-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="68b50-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span></span>
| <span data-ttu-id="68b50-1513">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1513">Target</span></span> | <span data-ttu-id="68b50-1514">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1514">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1515">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1515">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1516">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1516">64</span></span> |
| <span data-ttu-id="68b50-1517">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1517">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1519">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1519">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1520">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1520">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1521">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1521">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1522">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1522">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1523">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1523">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1525">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1525">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1527">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1527">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-1528">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1528">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1530">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1530">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-1531">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1531">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1532">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1532">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1533">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1533">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1534">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1534">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1535">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1535">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1536">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1536">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1538">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1538">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1539">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1539">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1540">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1540">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1541">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1541">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1542">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1542">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1544">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1544">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1545">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1545">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1546">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1546">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1547">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1547">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1548">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1548">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1549">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1549">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1550">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1550">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1551">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1551">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1552">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1552">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1553">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1553">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1554">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1554">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1555">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1555">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1557">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1557">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1559">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1559">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1561">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1561">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1563">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1563">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1564">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1564">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-1565">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1565">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1566">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1566">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1568">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1568">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1569">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1569">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1570">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1570">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1571">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1571">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1572">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1572">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1573">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1573">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a><span data-ttu-id="68b50-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="68b50-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span></span>
| <span data-ttu-id="68b50-1575">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1575">Target</span></span> | <span data-ttu-id="68b50-1576">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1576">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1577">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1577">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1578">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1578">64</span></span> |
| <span data-ttu-id="68b50-1579">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1579">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1581">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1581">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1582">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1582">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1583">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1583">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1584">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1584">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1585">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1587">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1589">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-1590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1590">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1592">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1592">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1594">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1594">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1596">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1596">Shader sample_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1598">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1598">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1599">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1599">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1601">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1601">Shader gather4_c</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1603">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1603">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1605">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1605">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1606">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1606">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1607">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1607">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1608">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1608">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1609">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1609">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1610">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1610">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1611">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1611">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1612">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1612">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1613">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1613">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1614">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1614">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1615">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1615">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1616">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1616">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1617">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1617">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1618">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1618">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1619">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1619">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1620">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1620">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1621">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1621">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1623">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1623">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1624">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1624">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1625">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1625">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1626">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1626">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1627">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1627">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1629">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1629">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1630">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1630">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1632">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1632">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1633">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1633">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1634">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1634">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1635">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1635">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1636">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1636">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1637">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1637">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a><span data-ttu-id="68b50-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="68b50-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span></span>
| <span data-ttu-id="68b50-1639">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1639">Target</span></span> | <span data-ttu-id="68b50-1640">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1640">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1641">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1641">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1642">64</span><span class="sxs-lookup"><span data-stu-id="68b50-1642">64</span></span> |
| <span data-ttu-id="68b50-1643">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1643">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1645">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1645">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1646">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1646">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1647">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1647">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1648">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1648">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1649">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1649">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1651">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1651">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1653">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1653">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-1654">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1654">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1656">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1656">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1658">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1658">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1659">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1659">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1660">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1660">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1661">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1661">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1662">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1662">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1663">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1663">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1665">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1665">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1666">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1666">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1667">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1667">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1668">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1668">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1669">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1669">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1670">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1670">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1671">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1671">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1672">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1672">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1673">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1673">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1674">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1674">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1675">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1675">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1676">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1676">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1677">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1677">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1678">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1678">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1679">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1679">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1680">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1680">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1681">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1681">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1683">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1684">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1685">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1686">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1687">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1687">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1689">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1689">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1690">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1690">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1692">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1692">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1693">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1693">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1694">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1694">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1695">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1695">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-1696">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1696">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1697">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1697">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="68b50-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>ПК</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="68b50-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="68b50-1699">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1699">Target</span></span> | <span data-ttu-id="68b50-1700">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1700">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1701">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1701">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1702">32</span><span class="sxs-lookup"><span data-stu-id="68b50-1702">32</span></span> |
| <span data-ttu-id="68b50-1703">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1703">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1705">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1705">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1706">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1706">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1707">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1707">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1708">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1708">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1709">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1709">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1711">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1711">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1713">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1715">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1717">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1717">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-1718">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1718">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1719">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1719">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1720">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1720">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1721">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1721">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1722">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1722">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1723">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1723">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1725">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1725">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1726">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1726">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1727">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1728">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1729">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1730">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1731">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1732">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1732">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1733">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1734">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1735">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1736">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1737">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1738">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1739">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1739">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1740">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1740">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1741">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1741">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1743">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1744">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1745">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1746">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1747">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1747">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-1748">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1749">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1749">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1751">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1751">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1752">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1752">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1753">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1753">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1754">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1754">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1756">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1756">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1757">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1757">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="68b50-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="68b50-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="68b50-1760">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1760">Target</span></span> | <span data-ttu-id="68b50-1761">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1761">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1762">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1763">32</span><span class="sxs-lookup"><span data-stu-id="68b50-1763">32</span></span> |
| <span data-ttu-id="68b50-1764">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1764">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1766">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1766">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1768">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1768">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1770">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1771">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1772">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1774">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1774">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1776">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1776">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1778">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1778">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1780">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1780">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1782">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1782">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1784">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1784">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1785">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1785">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1786">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1786">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1788">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1788">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1789">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1789">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1791">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1791">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1793">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1793">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1795">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1795">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1797">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1797">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1798">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1798">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1799">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1799">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1800">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1800">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1801">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1801">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1803">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1803">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1805">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1805">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1807">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1807">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1808">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1808">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1809">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1809">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1810">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1810">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1811">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1811">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1812">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1812">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1813">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1813">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1815">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1815">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1817">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1817">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1819">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1819">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1821">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1821">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1823">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1823">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1825">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1825">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1827">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1827">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1829">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1829">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1830">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1830">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1832">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1832">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1834">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1834">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1836">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1836">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1838">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1838">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="68b50-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="68b50-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="68b50-1841">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1841">Target</span></span> | <span data-ttu-id="68b50-1842">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1842">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1843">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1843">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1844">32</span><span class="sxs-lookup"><span data-stu-id="68b50-1844">32</span></span> |
| <span data-ttu-id="68b50-1845">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1845">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1847">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1847">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1849">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1849">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1851">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1851">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1852">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1852">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1853">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1853">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1855">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1857">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1859">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1859">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1861">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1861">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1863">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1863">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1864">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1864">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1865">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1865">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1866">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1866">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1867">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1867">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1868">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1870">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1870">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1871">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1871">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1873">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1873">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1874">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1874">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1876">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1876">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1877">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1877">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1878">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1878">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1879">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1879">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1881">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1881">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1883">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1883">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1885">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1885">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1886">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1886">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1887">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1887">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1888">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1888">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1889">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1889">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1890">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1890">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1891">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1891">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1893">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1893">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1895">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1895">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1897">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1897">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1899">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1899">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1900">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1900">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1902">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-1903">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1903">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1905">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1906">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-1907">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-1908">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1908">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1910">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1910">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-1911">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1911">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="68b50-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="68b50-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="68b50-1914">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1914">Target</span></span> | <span data-ttu-id="68b50-1915">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1915">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1916">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1916">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1917">32</span><span class="sxs-lookup"><span data-stu-id="68b50-1917">32</span></span> |
| <span data-ttu-id="68b50-1918">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1918">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1920">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1920">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1921">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1921">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1922">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1922">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1923">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1923">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1924">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1924">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-1925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1925">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1927">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-1928">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1928">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-1929">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1929">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-1930">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1930">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-1931">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1931">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-1932">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-1932">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-1933">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1933">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-1934">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-1934">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-1935">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1935">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-1936">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-1936">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-1937">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1937">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1938">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-1938">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1939">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-1939">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-1940">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-1940">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-1941">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1941">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1942">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-1942">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-1943">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1943">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-1944">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-1944">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-1945">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-1945">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-1946">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-1946">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-1947">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-1947">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-1948">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-1948">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-1949">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-1949">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-1950">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1950">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1951">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-1951">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-1952">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-1952">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1954">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1954">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1955">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-1955">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-1956">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-1956">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-1957">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-1957">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-1958">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-1958">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-1959">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-1959">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1961">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-1961">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1963">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-1963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-1964">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1964">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-1966">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-1966">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1968">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1968">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1970">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-1970">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1972">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-1972">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="68b50-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>ФНС</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="68b50-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="68b50-1975">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-1975">Target</span></span> | <span data-ttu-id="68b50-1976">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-1976">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-1977">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-1977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-1978">32</span><span class="sxs-lookup"><span data-stu-id="68b50-1978">32</span></span> |
| <span data-ttu-id="68b50-1979">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-1979">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1981">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-1981">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1983">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1983">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1985">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-1985">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1986">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-1986">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-1987">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-1987">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1989">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-1989">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1991">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-1991">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1993">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-1993">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1995">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-1995">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1997">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-1997">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-1999">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-1999">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2000">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2000">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2001">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2001">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2003">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2003">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2004">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2004">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2006">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2006">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2008">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2008">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2010">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2010">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2012">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2013">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2014">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2015">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2016">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2016">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2018">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2018">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2020">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2020">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2022">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2023">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2024">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2024">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2025">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2026">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2026">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2027">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2027">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2028">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2028">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2030">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2030">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2032">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2032">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2034">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2034">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2036">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2036">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2038">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2038">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2040">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2041">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2041">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-2042">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2043">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2044">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2045">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2045">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2046">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2046">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2047">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2047">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="68b50-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>ПК</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="68b50-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="68b50-2050">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2050">Target</span></span> | <span data-ttu-id="68b50-2051">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2051">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2052">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2053">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2053">32</span></span> |
| <span data-ttu-id="68b50-2054">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2054">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2056">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2056">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2057">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2057">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2058">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2058">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2059">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2059">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2060">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2062">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2064">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2066">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2068">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2068">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-2069">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2069">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2070">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2070">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2071">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2071">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2072">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2072">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2073">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2073">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2074">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2074">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2076">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2076">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2077">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2077">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2078">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2078">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2079">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2079">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2080">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2080">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2081">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2081">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2082">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2082">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2083">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2083">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-2084">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2084">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-2085">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2085">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-2086">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2086">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2087">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2087">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2088">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2088">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2089">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2089">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2090">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2090">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2091">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2091">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2092">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2092">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2094">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2094">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2095">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2095">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2096">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2096">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-2097">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2097">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2098">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2098">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-2099">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2099">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2100">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2100">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2102">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2102">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2103">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2103">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2104">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2104">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2105">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2105">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2107">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2107">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2108">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2108">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="68b50-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="68b50-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="68b50-2111">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2111">Target</span></span> | <span data-ttu-id="68b50-2112">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2112">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2113">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2113">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2114">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2114">32</span></span> |
| <span data-ttu-id="68b50-2115">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2115">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2117">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2117">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2119">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2119">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2121">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2121">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2122">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2122">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2123">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2123">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2125">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2127">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2127">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2129">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2129">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2131">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2131">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2133">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2133">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2135">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2135">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2136">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2136">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2137">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2137">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2139">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2139">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2140">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2142">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2142">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2144">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2144">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2146">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2146">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2148">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2148">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2149">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2149">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2150">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2150">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2151">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2151">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2152">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2152">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2154">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2154">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2156">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2156">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2158">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2158">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2159">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2159">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2160">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2160">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2161">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2161">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2162">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2162">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2163">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2163">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2164">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2164">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2166">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2166">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2168">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2168">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2170">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2170">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2172">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2172">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2174">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2174">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2176">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2176">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2178">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2178">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2180">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2180">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2181">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2181">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2183">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2183">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2185">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2185">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2187">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2187">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2189">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2189">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="68b50-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="68b50-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="68b50-2192">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2192">Target</span></span> | <span data-ttu-id="68b50-2193">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2193">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2194">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2195">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2195">32</span></span> |
| <span data-ttu-id="68b50-2196">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2196">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2198">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2198">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2199">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2199">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2200">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2200">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2201">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2201">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2202">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2202">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2204">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2204">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2206">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2206">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2208">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2210">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2210">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2212">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2212">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2214">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2214">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2215">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2215">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2216">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2216">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2218">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2219">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2221">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2221">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2223">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2223">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2225">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2225">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2227">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2227">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2228">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2228">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2229">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2229">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2230">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2230">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2231">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2231">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-2232">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2232">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-2233">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2233">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-2234">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2234">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2235">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2235">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2236">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2236">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2237">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2237">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2238">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2238">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2239">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2239">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2240">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2240">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2242">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2242">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2244">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2244">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2246">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2246">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2248">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2248">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2250">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2250">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2252">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2252">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2254">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2254">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2256">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2256">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2257">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2257">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2259">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2259">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2261">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2261">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2263">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2263">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2265">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2265">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="68b50-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="68b50-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="68b50-2268">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2268">Target</span></span> | <span data-ttu-id="68b50-2269">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2269">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2270">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2270">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2271">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2271">32</span></span> |
| <span data-ttu-id="68b50-2272">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2272">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2274">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2274">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2276">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2276">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2278">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2278">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2279">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2279">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2280">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2280">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2282">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2282">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2284">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2284">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2286">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2288">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2288">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2290">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2290">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2291">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2291">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2292">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2292">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2293">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2293">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2294">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2294">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2295">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2295">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2297">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2297">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2298">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2298">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2300">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2300">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2301">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2301">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2303">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2304">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2305">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2306">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2306">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2308">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2308">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2310">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2310">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2312">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2313">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2314">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2315">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2316">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2316">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2317">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2317">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2318">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2318">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2320">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2320">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2322">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2322">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2324">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2324">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2326">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2327">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2327">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2329">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2329">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2330">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2330">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2332">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2332">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2333">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2333">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2334">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2334">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2335">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2335">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2337">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2337">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2338">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2338">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="68b50-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="68b50-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="68b50-2341">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2341">Target</span></span> | <span data-ttu-id="68b50-2342">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2342">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2343">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2343">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2344">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2344">32</span></span> |
| <span data-ttu-id="68b50-2345">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2345">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2347">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2347">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2349">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2349">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2351">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2352">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2353">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2355">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2355">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2357">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2357">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2359">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2359">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2361">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2361">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2363">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2363">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2365">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2366">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2367">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2367">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2369">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2369">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2370">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2372">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2372">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2374">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2374">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2376">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2376">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2378">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2378">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2379">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2379">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2380">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2380">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2381">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2381">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2382">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2382">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2384">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2384">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2386">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2386">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2388">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2388">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2389">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2389">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2390">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2390">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2391">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2391">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2392">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2392">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2393">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2393">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2394">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2394">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2396">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2396">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2398">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2398">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2400">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2400">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2402">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2402">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2404">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2404">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2406">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2406">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2407">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2407">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2409">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2409">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2410">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2410">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2411">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2411">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2412">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2412">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2414">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2414">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2415">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2415">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="68b50-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="68b50-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="68b50-2418">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2418">Target</span></span> | <span data-ttu-id="68b50-2419">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2419">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2420">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2420">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2421">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2421">32</span></span> |
| <span data-ttu-id="68b50-2422">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2422">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2424">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2424">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2426">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2426">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2428">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2428">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2429">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2429">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2430">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2430">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2432">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2432">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2434">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2434">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2436">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2436">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2438">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2438">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2440">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2441">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2441">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2442">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2442">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2443">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2444">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2444">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2445">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2447">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2447">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2448">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2448">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2450">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2450">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2451">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2451">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2452">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2452">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2453">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2453">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2454">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2454">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2455">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2455">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2457">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2457">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2459">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2459">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2461">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2461">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2462">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2462">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2463">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2463">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2464">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2464">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2465">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2465">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2466">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2466">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2467">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2467">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2469">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2469">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2471">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2471">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2473">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2473">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2475">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2475">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2476">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2476">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2478">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2479">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2479">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2481">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2482">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2483">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2484">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2484">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2486">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2486">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2487">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2487">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="68b50-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>ПК</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="68b50-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="68b50-2490">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2490">Target</span></span> | <span data-ttu-id="68b50-2491">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2491">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2492">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2492">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2493">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2493">32</span></span> |
| <span data-ttu-id="68b50-2494">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2494">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2496">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2496">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2497">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2498">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2499">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2500">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2502">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2502">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2504">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2506">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2508">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2508">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-2509">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2509">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2510">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2510">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2511">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2511">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2512">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2512">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2513">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2513">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2514">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2514">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2516">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2516">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2517">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2518">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2519">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2520">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2521">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2522">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2523">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-2524">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-2525">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-2526">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2527">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2528">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2529">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2530">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2530">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2531">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2531">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2532">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2532">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2534">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2534">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2535">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2535">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2536">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2536">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-2537">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2537">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2538">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2538">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-2539">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2539">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2540">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2540">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2542">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2542">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2543">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2543">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2544">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2544">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2545">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2545">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2546">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2546">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2547">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2547">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="68b50-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="68b50-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="68b50-2550">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2550">Target</span></span> | <span data-ttu-id="68b50-2551">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2551">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2552">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2552">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2553">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2553">32</span></span> |
| <span data-ttu-id="68b50-2554">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2554">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2556">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2556">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2558">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2558">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2560">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2561">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2562">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2564">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2564">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2566">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2568">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2568">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2570">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2570">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2572">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2572">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2574">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2574">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2575">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2575">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2576">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2576">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2578">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2578">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2579">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2581">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2581">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2583">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2583">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2585">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2585">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2587">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2588">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2589">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2590">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2591">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2591">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2593">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2593">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2595">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2595">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2597">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2598">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2599">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2599">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2600">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2601">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2601">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2602">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2602">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2603">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2603">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2605">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2605">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2607">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2607">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2609">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2609">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2611">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2611">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2613">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2613">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2615">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2616">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2616">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2618">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2619">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2620">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2621">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2622">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2622">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2623">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2623">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="68b50-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="68b50-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="68b50-2626">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2626">Target</span></span> | <span data-ttu-id="68b50-2627">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2627">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2628">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2628">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2629">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2629">32</span></span> |
| <span data-ttu-id="68b50-2630">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2630">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2632">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2632">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2634">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2634">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2636">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2636">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2637">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2637">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2638">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2638">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2640">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2642">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2644">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2646">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2646">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2648">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2648">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2650">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2651">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2652">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2652">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2654">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2655">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2657">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2657">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2659">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2659">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2661">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2661">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2663">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2663">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2664">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2664">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2665">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2665">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2666">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2666">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2667">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2667">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2669">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2669">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2671">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2671">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2673">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2673">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2674">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2674">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2675">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2675">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2676">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2676">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2677">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2677">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2678">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2678">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2679">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2679">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2681">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2681">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2683">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2683">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2685">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2685">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2687">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2687">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2689">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2689">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2691">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2691">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2692">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2692">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2694">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2694">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2695">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2695">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2696">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2696">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2697">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2697">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2698">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2698">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2699">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2699">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="68b50-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="68b50-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="68b50-2702">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2702">Target</span></span> | <span data-ttu-id="68b50-2703">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2704">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2705">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2705">32</span></span> |
| <span data-ttu-id="68b50-2706">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2706">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2708">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2708">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2710">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2710">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2712">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2712">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2713">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2713">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2714">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2714">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2716">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2718">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2720">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2722">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2722">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2724">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2724">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2725">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2725">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2726">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2726">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2727">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2727">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2728">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2728">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2729">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2729">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2731">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2731">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2732">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2732">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2734">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2734">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2735">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2735">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2737">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2738">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2739">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2740">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2740">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2742">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2742">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2744">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2744">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2746">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2746">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2747">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2747">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2748">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2748">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2749">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2749">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2750">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2750">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2751">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2751">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2752">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2752">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2754">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2754">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2756">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2756">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2758">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2758">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2760">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2760">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2761">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2761">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2763">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2763">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2764">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2764">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2766">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2767">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2768">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2769">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2769">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2770">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2770">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2771">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2771">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="68b50-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="68b50-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="68b50-2774">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2774">Target</span></span> | <span data-ttu-id="68b50-2775">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2775">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2776">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2776">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2777">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2777">32</span></span> |
| <span data-ttu-id="68b50-2778">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2778">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2780">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2780">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2782">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2782">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2784">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2784">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2785">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2785">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2786">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2786">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2788">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2788">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2790">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2790">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2792">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2792">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2794">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2794">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2796">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2796">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2798">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2798">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2799">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2799">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2800">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2800">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2802">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2802">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2803">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2805">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2805">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2807">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2807">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2809">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2809">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2811">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2812">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2813">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2814">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2815">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2815">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2817">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2817">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2819">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2819">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2821">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2821">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2822">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2822">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2823">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2823">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2824">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2824">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2825">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2825">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2826">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2826">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2827">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2827">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2829">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2829">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2831">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2831">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2833">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2833">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2835">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2835">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2837">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2837">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2839">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2839">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2840">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2840">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2842">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2842">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2843">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2843">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2844">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2844">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2845">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2845">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2846">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2846">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2847">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2847">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="68b50-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="68b50-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="68b50-2850">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2850">Target</span></span> | <span data-ttu-id="68b50-2851">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2851">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2852">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2852">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2853">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2853">32</span></span> |
| <span data-ttu-id="68b50-2854">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2854">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2856">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2856">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2858">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2858">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2860">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2861">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2862">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2864">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2864">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2866">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2866">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2868">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2870">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2870">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2872">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2872">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2873">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2873">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2874">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2874">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2875">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2875">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2876">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2876">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2877">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2877">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2879">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2879">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2880">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2880">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2882">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2883">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2884">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2885">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2886">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2887">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2887">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2889">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2889">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2891">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2891">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2893">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2893">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2894">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2894">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2895">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2895">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2896">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2896">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2897">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2897">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2898">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2898">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2899">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2899">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2901">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2901">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2903">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2903">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2905">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2905">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-2907">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2907">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2908">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2908">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2910">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2910">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2911">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2911">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2913">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2914">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2915">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2916">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-2917">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2917">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2918">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2918">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="68b50-2920">DXGI_FORMAT_R32_TYPELESS<sup>ПК</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="68b50-2920">DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="68b50-2921">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2921">Target</span></span> | <span data-ttu-id="68b50-2922">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2922">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2923">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2924">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2924">32</span></span> |
| <span data-ttu-id="68b50-2925">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2925">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2927">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2927">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2928">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2929">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2930">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2931">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2933">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2933">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2935">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2935">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2937">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2937">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2939">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-2939">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-2940">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-2940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-2941">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-2941">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-2942">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-2942">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-2943">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2943">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-2944">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-2944">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-2945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2945">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2947">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-2947">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-2948">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2948">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2949">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-2949">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2950">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-2950">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-2951">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-2951">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-2952">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2952">Raw UAV and SRV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2954">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-2954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-2955">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2955">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-2956">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-2956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-2957">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-2957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-2958">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-2958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-2959">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-2959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-2960">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-2960">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-2961">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-2961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-2962">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2962">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2963">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-2963">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-2964">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-2964">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2966">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2967">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-2967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-2968">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-2968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-2969">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-2969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-2970">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-2970">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-2971">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-2971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-2972">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-2972">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2974">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-2974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-2975">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-2976">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-2976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-2977">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2977">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2979">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-2979">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-2980">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-2980">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="68b50-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="68b50-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="68b50-2983">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-2983">Target</span></span> | <span data-ttu-id="68b50-2984">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-2984">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-2985">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-2985">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-2986">32</span><span class="sxs-lookup"><span data-stu-id="68b50-2986">32</span></span> |
| <span data-ttu-id="68b50-2987">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-2987">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2989">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-2989">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2990">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2990">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2991">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-2991">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2992">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-2992">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-2993">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-2993">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2995">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-2995">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-2997">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-2997">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-2998">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-2998">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3000">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3000">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-3001">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3001">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3002">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3002">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3003">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3003">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3004">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3004">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3005">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3005">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3006">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3006">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3008">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3008">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3009">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3009">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3010">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3010">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3011">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3011">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3012">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3012">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3014">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3015">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3016">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3016">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3017">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3018">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3019">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3020">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3021">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3022">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3023">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3023">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3024">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3024">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3025">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3025">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3027">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3027">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3029">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3029">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3031">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3031">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3033">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3033">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3034">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3034">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-3035">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3035">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3036">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3036">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3038">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3038">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3039">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3039">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3040">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3040">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3041">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3041">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3043">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3043">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3044">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3044">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="68b50-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="68b50-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="68b50-3047">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3047">Target</span></span> | <span data-ttu-id="68b50-3048">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3048">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3049">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3049">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3050">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3050">32</span></span> |
| <span data-ttu-id="68b50-3051">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3051">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3053">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3053">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3055">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3055">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3057">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3057">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3058">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3058">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3060">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3062">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3064">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3066">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3068">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3068">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3070">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3070">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3072">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3072">Shader sample_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3074">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3074">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3075">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3075">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3077">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3077">Shader gather4_c</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3079">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3079">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3081">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3081">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3083">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3083">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3085">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3085">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3087">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3088">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3089">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3090">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3091">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3091">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3093">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3093">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3095">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3095">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3097">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3097">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3098">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3098">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3099">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3099">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3100">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3100">UAV Atomic Exchange</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3102">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3102">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3103">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3103">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3104">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3104">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3106">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3106">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3108">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3108">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3110">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3110">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3112">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3112">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3114">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3114">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3116">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3116">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3117">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3117">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3119">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3120">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3121">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3122">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3122">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3124">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3124">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3125">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3125">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="68b50-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="68b50-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="68b50-3128">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3128">Target</span></span> | <span data-ttu-id="68b50-3129">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3129">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3130">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3131">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3131">32</span></span> |
| <span data-ttu-id="68b50-3132">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3132">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3134">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3134">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3136">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3136">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3138">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3138">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3140">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3140">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3142">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3144">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3146">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3148">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3150">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3150">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3152">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3152">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3153">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3153">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3154">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3154">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3155">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3155">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3156">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3157">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3159">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3159">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3160">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3160">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3162">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3163">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3163">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3165">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3166">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3167">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3168">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3168">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3170">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3170">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3172">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3172">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3174">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3174">UAV Atomic Add</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3176">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3176">UAV Atomic Bitwise Ops</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3178">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3180">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3180">UAV Atomic Exchange</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3182">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3182">UAV Atomic Signed Min/Max</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3184">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3184">UAV Atomic Unsigned Min/Max</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3186">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3186">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3188">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3188">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3190">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3190">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3192">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3192">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3194">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3194">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3195">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3195">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3197">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3197">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3198">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3198">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3200">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3200">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3201">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3201">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3202">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3202">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3203">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3203">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3205">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3205">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3206">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3206">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="68b50-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="68b50-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="68b50-3209">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3209">Target</span></span> | <span data-ttu-id="68b50-3210">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3210">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3211">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3211">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3212">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3212">32</span></span> |
| <span data-ttu-id="68b50-3213">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3213">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3215">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3215">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3217">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3217">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3219">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3220">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3220">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3222">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3222">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3224">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3226">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3228">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3228">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3230">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3230">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3232">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3232">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3233">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3233">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3234">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3234">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3235">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3235">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3236">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3236">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3237">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3239">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3239">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3240">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3240">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3242">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3243">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3244">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3245">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3246">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3247">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3247">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3249">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3249">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3251">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3251">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3253">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3253">UAV Atomic Add</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3255">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3255">UAV Atomic Bitwise Ops</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3257">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3257">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3259">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3259">UAV Atomic Exchange</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3261">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3261">UAV Atomic Signed Min/Max</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3263">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3263">UAV Atomic Unsigned Min/Max</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3265">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3265">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3267">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3267">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3269">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3269">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3271">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3271">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3273">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3273">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3274">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3274">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3276">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3276">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3277">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3277">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3279">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3279">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3280">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3280">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3281">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3281">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3282">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3282">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3284">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3284">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3285">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3285">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a><span data-ttu-id="68b50-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="68b50-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span></span>
| <span data-ttu-id="68b50-3288">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3288">Target</span></span> | <span data-ttu-id="68b50-3289">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3289">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3290">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3290">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3291">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3291">32</span></span> |
| <span data-ttu-id="68b50-3292">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3292">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3294">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3294">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3295">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3295">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3296">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3296">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3297">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3297">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3298">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3298">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3300">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3302">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3302">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-3303">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3303">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3305">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3305">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-3306">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3307">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3307">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3308">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3308">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3309">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3309">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3310">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3310">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3311">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3313">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3313">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3314">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3314">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3315">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3315">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3316">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3316">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3317">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3317">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3318">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3318">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3319">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3319">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3320">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3320">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3321">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3321">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3322">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3322">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3323">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3323">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3324">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3324">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3325">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3325">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3326">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3326">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3327">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3327">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3328">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3328">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3329">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3329">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3331">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3332">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3333">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-3334">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3335">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3335">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-3336">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3337">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3337">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3339">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3339">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3340">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3340">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3341">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3341">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3342">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3342">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3343">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3343">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3344">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3344">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a><span data-ttu-id="68b50-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="68b50-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span></span>
| <span data-ttu-id="68b50-3346">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3346">Target</span></span> | <span data-ttu-id="68b50-3347">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3347">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3348">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3348">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3349">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3349">32</span></span> |
| <span data-ttu-id="68b50-3350">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3350">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3352">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3352">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3353">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3353">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3354">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3354">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3355">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3355">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3356">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3356">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3358">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3358">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3360">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-3361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3361">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3363">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3363">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-3364">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3364">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3365">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3366">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3367">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3367">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3368">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3368">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3369">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3369">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3371">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3371">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3372">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3372">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3373">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3374">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3375">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3375">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3377">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3377">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3378">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3378">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3379">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3379">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3380">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3380">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3381">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3381">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3382">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3382">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3383">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3383">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3384">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3384">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3385">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3385">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3386">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3386">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3387">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3387">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3388">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3388">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3390">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3390">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3392">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3392">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3394">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3394">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3396">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3396">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3397">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3397">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-3398">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3398">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3399">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3399">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3401">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3401">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3402">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3402">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3403">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3403">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3404">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3404">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3405">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3405">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3406">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3406">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a><span data-ttu-id="68b50-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="68b50-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span></span>
| <span data-ttu-id="68b50-3408">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3408">Target</span></span> | <span data-ttu-id="68b50-3409">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3409">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3410">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3410">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3411">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3411">32</span></span> |
| <span data-ttu-id="68b50-3412">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3412">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3414">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3414">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3415">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3415">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3416">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3416">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3417">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3417">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3418">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3418">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3420">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3420">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3422">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3422">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-3423">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3423">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3425">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3425">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3427">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3427">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3429">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3429">Shader sample_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3431">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3431">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3432">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3432">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3434">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3434">Shader gather4_c</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3436">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3438">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3438">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3439">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3439">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3440">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3440">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3441">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3441">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3442">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3442">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3443">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3443">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3444">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3444">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3445">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3445">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3446">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3446">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3447">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3447">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3448">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3448">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3449">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3449">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3450">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3450">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3451">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3451">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3452">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3452">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3453">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3453">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3454">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3454">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3456">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3456">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3457">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3457">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3458">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3458">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-3459">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3459">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3460">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3460">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3462">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3462">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3463">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3463">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3465">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3465">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3466">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3466">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3467">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3467">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3468">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3468">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3469">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3469">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3470">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3470">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a><span data-ttu-id="68b50-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="68b50-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span></span>
| <span data-ttu-id="68b50-3472">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3472">Target</span></span> | <span data-ttu-id="68b50-3473">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3473">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3474">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3474">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3475">32</span><span class="sxs-lookup"><span data-stu-id="68b50-3475">32</span></span> |
| <span data-ttu-id="68b50-3476">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3476">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3478">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3478">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3479">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3479">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3480">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3480">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3481">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3481">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3482">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3482">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3484">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3484">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3486">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3486">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-3487">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3487">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3489">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3489">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3491">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3491">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3492">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3492">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3493">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3493">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3494">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3494">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3495">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3495">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3496">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3496">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3498">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3498">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3499">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3499">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3500">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3500">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3501">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3501">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3502">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3502">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3503">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3503">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3504">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3504">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3505">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3505">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3506">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3506">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3507">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3507">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3508">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3508">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3509">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3509">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3510">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3510">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3511">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3511">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3512">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3512">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3513">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3513">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3514">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3514">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3516">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3516">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3517">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3517">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3518">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3518">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-3519">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3519">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3520">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3520">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3522">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3522">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3523">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3523">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3525">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3526">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3527">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3528">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3528">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3529">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3529">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3530">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3530">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="68b50-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>ПК</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="68b50-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="68b50-3532">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3532">Target</span></span> | <span data-ttu-id="68b50-3533">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3533">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3534">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3534">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3535">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3535">16</span></span> |
| <span data-ttu-id="68b50-3536">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3536">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3538">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3538">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3539">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3539">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3540">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3541">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3542">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3544">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3546">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3548">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3550">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3550">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-3551">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3552">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3552">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3553">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3553">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3554">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3555">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3555">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3556">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3558">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3558">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3559">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3559">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3560">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3560">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3561">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3562">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3563">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3564">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3565">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3565">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3566">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3567">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3568">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3569">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3570">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3571">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3572">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3573">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3574">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3574">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3576">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3576">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3577">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3577">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3578">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3578">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-3579">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3579">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3580">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3580">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-3581">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3581">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3582">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3582">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3584">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3584">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3585">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3585">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3586">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3586">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3587">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3587">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3588">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3588">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3589">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3589">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="68b50-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="68b50-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="68b50-3592">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3592">Target</span></span> | <span data-ttu-id="68b50-3593">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3593">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3594">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3594">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3595">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3595">16</span></span> |
| <span data-ttu-id="68b50-3596">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3596">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3598">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3598">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3600">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3600">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3602">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3603">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3604">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3606">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3608">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3608">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3610">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3612">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3612">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3614">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3614">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3616">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3616">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3617">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3617">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3618">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3618">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3620">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3620">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3621">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3621">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3623">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3623">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3625">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3625">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3627">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3627">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3629">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3629">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3630">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3630">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3631">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3631">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3632">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3632">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3633">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3633">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3635">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3635">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3637">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3637">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3639">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3639">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3640">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3640">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3641">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3641">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3642">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3642">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3643">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3643">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3644">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3644">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3645">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3645">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3647">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3647">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3649">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3649">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3651">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3651">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3653">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3653">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3655">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3655">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3657">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3658">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3658">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3660">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3660">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3661">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3661">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3662">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3662">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3663">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3663">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3665">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3665">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3666">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3666">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="68b50-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="68b50-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="68b50-3669">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3669">Target</span></span> | <span data-ttu-id="68b50-3670">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3670">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3671">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3671">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3672">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3672">16</span></span> |
| <span data-ttu-id="68b50-3673">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3673">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3675">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3675">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3677">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3677">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3679">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3679">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3680">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3680">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3681">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3681">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3683">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3683">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3685">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3685">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3687">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3687">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3689">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3689">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3691">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3691">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3692">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3692">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3693">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3693">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3694">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3694">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3695">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3695">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3696">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3696">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3698">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3698">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3699">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3699">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3701">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3701">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3702">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3702">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3704">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3704">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3705">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3705">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3706">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3706">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3707">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3707">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3709">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3709">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3711">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3711">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3713">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3713">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3714">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3714">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3715">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3715">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3716">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3716">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3717">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3717">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3718">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3718">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3719">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3719">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3721">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3721">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3723">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3723">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3725">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3725">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3727">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3728">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3728">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3730">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3730">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3731">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3731">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3733">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3733">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3734">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3734">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3735">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3735">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3736">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3736">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3737">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3737">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3738">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3738">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="68b50-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="68b50-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="68b50-3741">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3741">Target</span></span> | <span data-ttu-id="68b50-3742">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3742">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3743">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3743">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3744">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3744">16</span></span> |
| <span data-ttu-id="68b50-3745">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3745">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3747">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3747">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3749">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3749">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3751">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3752">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3753">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3755">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3757">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3759">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3761">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3761">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3763">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3763">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3765">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3765">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3766">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3766">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3767">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3767">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3769">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3769">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3770">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3770">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3772">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3772">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3774">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3774">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3776">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3776">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3778">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3778">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3779">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3779">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3780">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3780">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3781">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3781">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3782">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3782">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3784">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3784">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3786">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3786">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3788">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3789">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3790">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3791">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3792">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3793">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3794">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3794">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3796">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3796">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3798">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3798">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3800">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3800">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3802">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3802">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3804">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3804">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3806">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3807">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3807">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3809">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3809">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3810">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3810">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3811">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3811">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3812">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3812">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3813">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3813">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3814">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3814">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="68b50-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="68b50-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="68b50-3817">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3817">Target</span></span> | <span data-ttu-id="68b50-3818">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3818">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3819">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3820">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3820">16</span></span> |
| <span data-ttu-id="68b50-3821">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3821">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3823">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3823">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3825">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3825">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3827">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3828">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3829">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3831">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3833">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3835">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3837">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3837">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3839">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3839">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3840">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3840">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3841">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3841">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3842">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3842">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3843">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3843">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3844">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3844">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3846">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3846">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3847">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3847">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3849">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3849">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3850">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3850">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3851">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3851">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3852">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3852">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3853">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3853">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3854">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3854">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3856">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3856">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3858">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3858">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3860">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3860">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3861">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3861">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3862">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3862">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3863">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3863">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3864">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3864">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3865">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3865">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3866">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3866">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3868">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3868">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3870">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3870">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3872">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3872">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-3874">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3874">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3875">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3875">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3877">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3877">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3878">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3878">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3880">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3881">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3882">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3883">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3883">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-3884">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3885">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3885">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="68b50-3887">DXGI_FORMAT_R16_TYPELESS<sup>ПК</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="68b50-3887">DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="68b50-3888">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3888">Target</span></span> | <span data-ttu-id="68b50-3889">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3889">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3890">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3891">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3891">16</span></span> |
| <span data-ttu-id="68b50-3892">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3892">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3894">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3894">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3895">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3896">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3897">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3898">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3900">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3902">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3904">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3906">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3906">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-3907">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3907">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-3908">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3908">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3909">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3909">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3910">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3910">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-3911">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3911">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3912">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3914">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3914">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-3915">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3915">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3916">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3916">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3917">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3917">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3918">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3918">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3919">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3919">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3920">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3920">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3921">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3921">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-3922">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3922">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-3923">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3923">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-3924">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3924">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3925">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3925">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3926">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3926">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3927">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3927">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-3928">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3928">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3929">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-3929">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-3930">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-3930">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3932">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3932">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3933">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3933">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-3934">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-3934">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-3935">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-3935">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-3936">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-3936">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-3937">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-3937">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-3938">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-3938">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3940">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-3940">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-3941">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3941">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-3942">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-3942">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-3943">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3943">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3945">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-3945">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-3946">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-3946">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="68b50-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="68b50-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="68b50-3949">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-3949">Target</span></span> | <span data-ttu-id="68b50-3950">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-3950">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-3951">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-3951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-3952">16</span><span class="sxs-lookup"><span data-stu-id="68b50-3952">16</span></span> |
| <span data-ttu-id="68b50-3953">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-3953">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3955">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-3955">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3957">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3957">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3959">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-3959">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3960">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-3960">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-3961">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-3961">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-3963">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-3965">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3967">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-3967">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3969">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-3969">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3971">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-3971">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3973">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-3973">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-3974">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-3974">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-3975">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3975">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3977">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-3977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-3978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3978">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3980">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-3980">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3982">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-3982">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3984">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-3984">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3986">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-3986">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-3987">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-3987">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-3988">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3988">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3989">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-3989">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-3990">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3990">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3992">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-3992">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3994">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-3994">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-3996">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-3996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-3997">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-3997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-3998">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-3998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-3999">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-3999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4000">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4000">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4001">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4001">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4002">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4002">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4004">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4004">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4006">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4006">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4008">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4008">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4010">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4010">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4012">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4012">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4014">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4014">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4015">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4015">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4017">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4017">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4018">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4018">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4019">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4019">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4020">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4020">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4022">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4022">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4023">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4023">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="68b50-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="68b50-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="68b50-4026">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4026">Target</span></span> | <span data-ttu-id="68b50-4027">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4027">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4028">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4028">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4029">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4029">16</span></span> |
| <span data-ttu-id="68b50-4030">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4030">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4032">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4032">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4033">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4033">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4034">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4035">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4036">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4038">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4040">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-4041">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4041">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4043">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4043">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-4044">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4044">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4045">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4045">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4046">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4046">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4047">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4047">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4048">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4048">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4049">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4049">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4051">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4051">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4052">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4052">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4053">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4053">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4054">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4054">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4055">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4055">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4057">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4057">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4058">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4058">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4059">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4059">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-4060">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4060">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-4061">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4061">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-4062">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4062">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4063">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4063">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4064">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4064">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4065">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4065">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4066">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4066">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4067">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4067">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4068">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4068">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4070">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4070">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4072">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4072">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4074">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4074">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4076">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4076">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4077">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4077">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-4078">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4078">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4079">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4079">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4081">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4081">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4082">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4082">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4083">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4083">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4084">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4084">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4086">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4086">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4087">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4087">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="68b50-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="68b50-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="68b50-4090">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4090">Target</span></span> | <span data-ttu-id="68b50-4091">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4091">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4092">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4093">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4093">16</span></span> |
| <span data-ttu-id="68b50-4094">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4094">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4096">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4096">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4098">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4098">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4100">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4100">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4101">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4101">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4102">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4102">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4104">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4106">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4108">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4110">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4110">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4112">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4112">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4114">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4114">Shader sample_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4116">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4116">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4117">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4117">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4119">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4119">Shader gather4_c</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4121">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4121">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4123">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4123">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4125">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4125">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4127">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4127">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4129">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4129">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4130">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4130">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4131">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4131">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4132">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4132">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4133">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4133">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4135">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4135">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4137">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4137">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4139">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4139">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4140">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4140">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4141">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4141">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4142">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4142">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4143">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4143">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4144">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4144">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4145">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4145">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4147">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4147">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4149">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4149">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4151">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4151">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4153">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4153">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4155">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4155">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4157">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4157">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4158">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4158">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4160">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4160">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4161">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4161">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4162">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4162">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4163">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4163">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4165">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4165">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4166">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4166">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="68b50-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="68b50-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="68b50-4169">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4169">Target</span></span> | <span data-ttu-id="68b50-4170">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4170">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4171">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4172">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4172">16</span></span> |
| <span data-ttu-id="68b50-4173">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4173">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4175">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4175">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4177">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4177">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4179">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4179">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4181">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4182">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4184">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4184">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4186">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4186">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4188">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4188">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4190">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4190">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4192">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4193">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4194">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4195">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4195">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4196">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4197">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4199">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4200">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4200">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4202">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4202">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4203">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4203">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4205">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4206">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4207">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4208">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4208">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4210">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4210">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4212">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4212">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4214">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4215">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4216">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4217">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4218">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4219">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4220">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4220">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4222">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4222">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4224">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4224">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4226">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4226">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4228">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4228">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4229">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4229">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4231">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4231">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4232">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4232">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4234">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4235">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4236">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4237">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4237">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4239">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4239">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4240">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4240">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="68b50-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="68b50-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="68b50-4243">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4243">Target</span></span> | <span data-ttu-id="68b50-4244">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4244">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4245">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4245">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4246">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4246">16</span></span> |
| <span data-ttu-id="68b50-4247">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4247">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4249">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4249">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4251">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4251">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4253">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4253">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4254">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4254">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4255">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4255">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4257">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4259">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4259">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4261">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4261">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4263">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4263">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4265">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4265">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4267">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4267">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4268">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4268">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4269">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4269">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4271">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4271">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4272">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4272">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4274">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4274">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4276">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4276">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4278">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4278">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4280">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4280">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4281">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4282">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4283">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4284">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4284">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4286">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4286">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4288">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4288">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4290">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4291">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4292">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4292">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4293">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4294">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4294">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4295">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4295">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4296">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4296">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4298">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4298">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4300">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4300">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4302">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4302">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4304">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4304">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4306">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4306">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4308">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4308">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4309">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4309">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4311">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4311">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4312">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4312">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4313">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4313">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4314">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4314">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4316">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4316">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4317">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4317">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="68b50-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="68b50-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="68b50-4320">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4320">Target</span></span> | <span data-ttu-id="68b50-4321">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4321">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4322">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4323">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4323">16</span></span> |
| <span data-ttu-id="68b50-4324">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4324">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4326">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4326">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4328">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4328">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4330">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4331">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4332">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4334">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4336">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4338">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4340">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4340">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4342">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4342">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4343">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4343">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4344">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4344">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4345">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4345">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4346">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4346">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4347">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4347">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4349">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4349">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4350">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4350">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4352">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4353">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4354">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4355">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4356">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4357">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4357">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4359">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4359">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4361">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4361">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4363">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4364">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4365">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4365">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4366">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4367">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4367">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4368">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4368">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4369">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4369">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4371">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4371">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4373">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4373">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4375">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4375">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4377">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4378">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4378">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4380">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4380">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4381">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4381">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4383">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4383">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4384">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4384">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4385">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4385">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4386">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4386">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4388">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4388">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4389">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4389">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="68b50-4391">DXGI_FORMAT_R8_TYPELESS<sup>ПК</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="68b50-4391">DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="68b50-4392">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4392">Target</span></span> | <span data-ttu-id="68b50-4393">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4393">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4394">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4395">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4395">8</span></span> |
| <span data-ttu-id="68b50-4396">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4396">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4398">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4398">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4399">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4399">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4400">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4401">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4402">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4404">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4406">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4408">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4410">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4410">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-4411">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4411">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4412">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4412">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4413">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4413">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4414">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4414">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4415">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4415">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4416">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4416">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4418">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4418">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4419">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4419">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4420">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4420">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4421">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4421">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4422">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4422">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4423">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4423">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4424">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4424">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4425">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4425">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-4426">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4426">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-4427">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4427">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-4428">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4428">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4429">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4429">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4430">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4430">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4431">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4431">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4432">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4432">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4433">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4433">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4434">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4434">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4436">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4437">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4438">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-4439">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4440">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4440">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-4441">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4442">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4442">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4444">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4445">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4446">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4447">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4447">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4449">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4449">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4450">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4450">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="68b50-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="68b50-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="68b50-4453">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4453">Target</span></span> | <span data-ttu-id="68b50-4454">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4454">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4455">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4455">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4456">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4456">8</span></span> |
| <span data-ttu-id="68b50-4457">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4457">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4459">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4459">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4461">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4461">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4463">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4464">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4465">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4467">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4469">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4471">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4471">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4473">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4473">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4475">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4475">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4477">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4477">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4478">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4478">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4479">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4479">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4481">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4481">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4482">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4484">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4484">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4486">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4486">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4488">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4488">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4490">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4490">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4491">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4491">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4492">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4492">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4493">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4493">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4494">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4494">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4496">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4496">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4498">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4498">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4500">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4501">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4502">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4503">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4504">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4505">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4506">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4506">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4508">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4508">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4510">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4510">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4512">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4512">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4514">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4514">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4516">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4516">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4518">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4518">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4519">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4519">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4521">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4521">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4522">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4522">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4523">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4523">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4524">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4524">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4526">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4526">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4527">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4527">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="68b50-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="68b50-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="68b50-4530">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4530">Target</span></span> | <span data-ttu-id="68b50-4531">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4531">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4532">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4532">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4533">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4533">8</span></span> |
| <span data-ttu-id="68b50-4534">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4534">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4536">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4536">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4538">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4538">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4540">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4541">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4542">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4544">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4546">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4548">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4550">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4550">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4552">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4552">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4553">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4553">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4554">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4554">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4555">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4555">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4556">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4556">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4557">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4557">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4559">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4559">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4560">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4560">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4562">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4562">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4563">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4563">Output Merger Logic Op</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4565">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4566">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4567">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4568">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4568">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4570">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4570">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4572">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4572">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4574">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4575">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4576">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4577">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4578">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4578">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4579">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4579">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4580">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4580">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4582">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4582">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4584">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4584">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4586">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4586">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4588">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4588">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4589">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4589">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4591">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4591">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4592">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4592">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4594">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4594">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4595">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4595">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4596">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4596">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4597">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4597">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4599">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4599">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4600">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4600">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="68b50-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="68b50-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="68b50-4603">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4603">Target</span></span> | <span data-ttu-id="68b50-4604">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4605">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4606">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4606">8</span></span> |
| <span data-ttu-id="68b50-4607">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4607">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4609">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4609">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4611">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4611">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4613">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4613">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4614">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4614">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4615">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4615">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4617">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4617">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4619">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4619">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4621">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4621">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4623">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4623">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4625">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4625">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4627">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4627">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4628">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4628">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4629">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4629">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4631">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4631">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4632">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4634">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4634">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4636">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4636">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4638">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4638">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4640">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4640">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4641">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4641">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4642">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4642">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4643">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4643">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4644">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4644">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4646">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4646">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4648">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4648">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4650">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4650">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4651">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4651">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4652">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4652">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4653">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4653">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4654">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4654">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4655">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4655">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4656">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4656">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4658">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4658">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4660">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4660">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4662">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4662">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4664">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4664">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4666">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4666">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4668">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4668">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4669">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4669">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4671">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4671">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4672">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4672">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4673">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4673">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4674">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4674">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4676">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4676">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4677">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4677">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="68b50-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="68b50-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="68b50-4680">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4680">Target</span></span> | <span data-ttu-id="68b50-4681">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4681">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4682">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4682">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4683">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4683">8</span></span> |
| <span data-ttu-id="68b50-4684">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4684">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4686">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4686">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4688">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4688">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4690">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4690">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4691">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4691">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4692">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4692">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4694">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4696">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4696">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4698">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4700">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4700">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4702">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4702">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-4703">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4703">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4704">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4704">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4705">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4705">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-4706">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4706">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4707">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4709">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4709">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4710">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4710">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4712">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4712">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4713">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4713">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4714">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4714">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4715">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4715">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4716">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4716">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4717">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4717">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4719">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4719">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4721">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4721">UAV Typed Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4723">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4723">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4724">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4724">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4725">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4725">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4726">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4726">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4727">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4727">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4728">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4728">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4729">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4729">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4731">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4731">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4733">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4733">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4735">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4735">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4737">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4738">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4738">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4740">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4741">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4741">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4743">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4744">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4745">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4746">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4746">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4748">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4748">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4749">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4749">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="68b50-4751">DXGI_FORMAT_A8_UNORM<sup>ФНС</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="68b50-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="68b50-4752">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4752">Target</span></span> | <span data-ttu-id="68b50-4753">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4753">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4754">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4755">8</span><span class="sxs-lookup"><span data-stu-id="68b50-4755">8</span></span> |
| <span data-ttu-id="68b50-4756">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4756">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4758">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4758">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4759">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4760">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4761">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4762">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4764">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4764">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4766">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4766">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4768">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4768">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4770">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4770">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4772">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4772">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4774">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4774">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4775">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4775">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4776">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4776">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4778">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4778">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4779">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4779">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4781">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4781">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4783">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4783">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4785">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4785">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4787">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4787">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4788">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4789">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4790">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4791">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4791">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4793">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4793">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4795">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4795">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4797">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4797">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4798">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4798">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4799">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4799">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4800">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4800">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4801">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4801">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4802">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4802">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4803">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4803">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4805">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4805">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4807">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4807">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4809">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4809">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-4811">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4811">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4813">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4813">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4815">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4815">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4816">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4816">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-4817">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4817">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4818">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4818">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4819">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4819">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4820">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4820">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4822">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4822">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4823">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4823">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="68b50-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>ФНК</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="68b50-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="68b50-4826">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4826">Target</span></span> | <span data-ttu-id="68b50-4827">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4827">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4828">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4829">32</span><span class="sxs-lookup"><span data-stu-id="68b50-4829">32</span></span> |
| <span data-ttu-id="68b50-4830">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4830">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4832">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4832">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4833">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4833">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4834">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4834">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4835">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4835">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4836">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4836">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4838">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4840">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4840">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4842">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4842">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4844">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4844">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4846">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4846">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4848">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4848">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4849">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4849">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4850">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4850">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4852">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4852">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4853">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4853">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4855">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4855">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4856">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4856">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4857">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4857">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4858">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4858">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4859">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4859">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4860">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4860">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4861">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4861">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4862">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4862">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-4863">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4863">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-4864">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4864">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-4865">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4865">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4866">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4866">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4867">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4867">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4868">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4868">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4869">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4869">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4870">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4870">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4871">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4871">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4873">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4873">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4874">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4874">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4875">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4875">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-4876">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4876">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4877">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4877">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-4878">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4878">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4879">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4879">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-4880">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4881">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4882">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4883">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4883">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-4884">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4885">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4885">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="68b50-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>ФНК</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="68b50-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="68b50-4888">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4888">Target</span></span> | <span data-ttu-id="68b50-4889">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4889">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4890">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4891">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4891">16</span></span> |
| <span data-ttu-id="68b50-4892">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4892">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4894">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4894">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4895">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4896">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4897">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4898">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4900">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4902">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4904">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4906">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4906">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4908">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4908">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4910">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4910">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4911">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4911">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4912">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4912">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4914">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4914">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4915">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4915">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4917">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4917">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4918">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4918">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4919">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4919">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4920">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4921">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4922">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4923">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4924">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4924">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-4925">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-4926">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-4927">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4928">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4929">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4929">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4930">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4931">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4931">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4932">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4932">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4933">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4933">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4935">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4935">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4936">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4936">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4937">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4937">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-4938">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4938">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-4939">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-4939">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-4940">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-4940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-4941">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-4941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-4942">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-4942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-4943">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-4944">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-4944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-4945">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4945">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-4946">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-4946">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-4947">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-4947">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="68b50-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>ФНК</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="68b50-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="68b50-4949">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-4949">Target</span></span> | <span data-ttu-id="68b50-4950">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-4950">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-4951">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-4951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-4952">16</span><span class="sxs-lookup"><span data-stu-id="68b50-4952">16</span></span> |
| <span data-ttu-id="68b50-4953">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-4953">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4955">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-4955">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4956">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4956">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4957">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-4957">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4958">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-4958">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-4959">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-4959">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4961">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-4961">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4963">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-4963">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4965">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-4965">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4967">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-4967">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4969">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-4969">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4971">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-4971">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-4972">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-4972">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-4973">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4973">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4975">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-4975">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-4976">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4976">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4978">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-4978">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-4979">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4979">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4980">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-4980">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4981">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-4981">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-4982">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-4982">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-4983">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4983">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4984">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-4984">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-4985">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4985">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-4986">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-4986">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-4987">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-4987">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-4988">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-4988">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-4989">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-4989">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-4990">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-4990">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-4991">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-4991">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-4992">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4992">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4993">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-4993">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-4994">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-4994">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-4996">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4996">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4997">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-4997">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-4998">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-4998">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-4999">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-4999">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5000">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5000">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5001">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5001">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5002">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5002">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-5003">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5003">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5004">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5004">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5005">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5005">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5006">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5006">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5007">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5007">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5008">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="68b50-5009">DXGI_FORMAT_BC1_TYPELESS<sup>ПКК</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="68b50-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="68b50-5010">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5010">Target</span></span> | <span data-ttu-id="68b50-5011">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5012">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5013">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5013">64</span></span> |
| <span data-ttu-id="68b50-5014">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5014">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5016">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5016">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5017">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5018">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5019">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5021">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5023">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5025">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5027">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5027">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-5028">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5028">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-5029">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5029">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5030">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5030">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5031">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5031">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-5032">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5032">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5033">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5033">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5035">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5035">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5036">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5036">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5037">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5037">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5038">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5038">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5039">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5039">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5040">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5040">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5041">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5041">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5042">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5042">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5043">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5043">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5044">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5044">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5045">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5045">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5046">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5046">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5047">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5047">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5048">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5048">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5049">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5049">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5050">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5050">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5051">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5051">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5053">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5054">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5055">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5056">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5057">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5057">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5058">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5059">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5059">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5061">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5061">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5062">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5062">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5063">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5063">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5064">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5064">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5066">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5066">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5067">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5067">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a><span data-ttu-id="68b50-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="68b50-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="68b50-5070">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5070">Target</span></span> | <span data-ttu-id="68b50-5071">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5071">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5072">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5072">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5073">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5073">64</span></span> |
| <span data-ttu-id="68b50-5074">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5074">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5076">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5076">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5077">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5077">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5078">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5078">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5079">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5079">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5080">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5080">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5081">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5081">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5083">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5083">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5085">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5085">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5087">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5087">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5089">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5089">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5091">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5091">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5092">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5092">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5093">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5093">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5095">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5095">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5096">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5096">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5098">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5098">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5099">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5099">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5100">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5101">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5102">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5103">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5104">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5105">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5105">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5106">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5107">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5108">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5109">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5110">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5111">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5112">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5112">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5113">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5113">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5114">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5114">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5116">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5116">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5117">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5117">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5118">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5118">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5119">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5119">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5120">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5120">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5121">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5122">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5122">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5124">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5125">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5126">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5127">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5127">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5129">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5129">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5130">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5130">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a><span data-ttu-id="68b50-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="68b50-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="68b50-5133">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5133">Target</span></span> | <span data-ttu-id="68b50-5134">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5134">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5135">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5136">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5136">64</span></span> |
| <span data-ttu-id="68b50-5137">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5137">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5139">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5139">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5140">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5141">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5142">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5143">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5144">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5146">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5148">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5150">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5150">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5152">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5152">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5154">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5154">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5155">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5155">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5156">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5156">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5158">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5158">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5159">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5161">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5161">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5162">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5162">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5163">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5163">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5164">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5164">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5165">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5166">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5167">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5168">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5168">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5169">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5169">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5170">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5170">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5171">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5171">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5172">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5172">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5173">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5173">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5174">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5174">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5175">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5175">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5176">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5176">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5177">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5177">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5179">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5180">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5181">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5182">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5183">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5183">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5184">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5185">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5185">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5187">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5187">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5188">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5188">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5189">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5189">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5190">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5190">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5192">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5192">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5193">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5193">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="68b50-5195">DXGI_FORMAT_BC2_TYPELESS<sup>ПКК</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="68b50-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="68b50-5196">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5196">Target</span></span> | <span data-ttu-id="68b50-5197">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5197">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5198">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5198">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5199">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5199">128</span></span> |
| <span data-ttu-id="68b50-5200">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5200">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5202">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5202">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5203">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5204">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5205">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5206">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5207">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5209">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5209">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5211">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5211">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5213">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5213">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-5214">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5214">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-5215">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5215">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5216">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5216">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5217">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5217">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-5218">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5219">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5221">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5221">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5222">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5222">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5223">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5223">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5224">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5224">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5225">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5225">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5226">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5226">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5227">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5227">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5228">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5228">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5229">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5229">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5230">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5230">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5231">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5231">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5232">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5232">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5233">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5233">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5234">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5234">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5235">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5235">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5236">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5236">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5237">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5237">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5239">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5239">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5240">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5240">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5241">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5241">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5242">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5242">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5243">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5243">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5244">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5244">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5245">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5245">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5247">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5247">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5248">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5248">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5249">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5249">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5250">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5250">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5252">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5252">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5253">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5253">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a><span data-ttu-id="68b50-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="68b50-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="68b50-5256">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5256">Target</span></span> | <span data-ttu-id="68b50-5257">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5258">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5259">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5259">128</span></span> |
| <span data-ttu-id="68b50-5260">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5260">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5262">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5262">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5263">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5264">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5265">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5267">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5269">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5271">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5273">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5273">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5275">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5275">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5277">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5277">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5278">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5278">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5279">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5279">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5281">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5281">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5282">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5284">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5284">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5285">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5285">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5286">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5286">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5287">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5287">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5288">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5289">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5290">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5291">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5291">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5292">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5293">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5294">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5295">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5296">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5296">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5297">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5298">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5298">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5299">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5299">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5300">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5300">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5302">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5303">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5304">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5305">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5306">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5306">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5307">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5308">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5308">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5310">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5310">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5311">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5311">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5312">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5312">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5313">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5313">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5315">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5315">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5316">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5316">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a><span data-ttu-id="68b50-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="68b50-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="68b50-5319">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5319">Target</span></span> | <span data-ttu-id="68b50-5320">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5320">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5321">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5321">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5322">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5322">128</span></span> |
| <span data-ttu-id="68b50-5323">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5323">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5325">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5325">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5326">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5326">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5327">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5328">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5328">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5329">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5329">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5330">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5330">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5332">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5332">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5334">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5336">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5336">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5338">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5338">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5340">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5340">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5341">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5341">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5342">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5342">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5344">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5345">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5347">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5348">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5348">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5349">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5349">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5350">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5350">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5351">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5351">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5352">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5352">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5353">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5353">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5354">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5354">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5355">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5355">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5356">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5357">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5358">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5359">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5360">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5361">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5362">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5363">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5363">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5365">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5366">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5367">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5368">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5369">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5369">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5370">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5371">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5371">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5373">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5373">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5374">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5374">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5375">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5375">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5376">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5376">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5378">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5378">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5379">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5379">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="68b50-5381">DXGI_FORMAT_BC3_TYPELESS<sup>ПКК</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="68b50-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="68b50-5382">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5382">Target</span></span> | <span data-ttu-id="68b50-5383">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5383">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5384">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5385">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5385">128</span></span> |
| <span data-ttu-id="68b50-5386">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5386">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5388">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5388">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5389">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5389">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5390">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5391">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5392">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5393">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5395">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5397">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5399">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5399">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-5400">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-5401">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5401">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5402">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5402">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5403">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5403">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-5404">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5404">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5405">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5407">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5407">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5408">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5408">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5409">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5409">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5410">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5410">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5411">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5411">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5412">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5412">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5413">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5413">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5414">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5414">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5415">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5415">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5416">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5416">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5417">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5417">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5418">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5418">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5419">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5419">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5420">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5420">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5421">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5421">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5422">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5422">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5423">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5423">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5425">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5426">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5427">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5428">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5429">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5429">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5430">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5431">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5431">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5433">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5433">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5434">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5434">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5435">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5435">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5436">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5436">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5438">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5438">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5439">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5439">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a><span data-ttu-id="68b50-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="68b50-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="68b50-5442">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5442">Target</span></span> | <span data-ttu-id="68b50-5443">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5443">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5444">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5444">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5445">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5445">128</span></span> |
| <span data-ttu-id="68b50-5446">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5446">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5448">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5448">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5449">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5450">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5451">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5452">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5453">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5455">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5457">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5457">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5459">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5459">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5461">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5461">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5463">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5463">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5464">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5464">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5465">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5465">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5467">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5467">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5468">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5470">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5470">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5471">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5471">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5472">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5472">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5473">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5473">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5474">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5474">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5475">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5475">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5476">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5476">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5477">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5477">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5478">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5478">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5479">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5479">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5480">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5480">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5481">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5481">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5482">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5482">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5483">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5483">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5484">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5484">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5485">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5485">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5486">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5486">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5488">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5489">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5490">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5491">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5492">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5492">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5493">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5494">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5494">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5496">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5496">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5497">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5497">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5498">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5498">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5499">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5499">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5501">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5501">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5502">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5502">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a><span data-ttu-id="68b50-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="68b50-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="68b50-5505">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5505">Target</span></span> | <span data-ttu-id="68b50-5506">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5506">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5507">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5507">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5508">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5508">128</span></span> |
| <span data-ttu-id="68b50-5509">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5509">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5511">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5511">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5512">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5512">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5513">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5513">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5514">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5514">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5515">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5515">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5516">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5518">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5520">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5522">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5522">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5524">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5524">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5526">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5526">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5527">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5527">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5528">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5528">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5530">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5531">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5533">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5534">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5534">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5535">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5536">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5537">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5538">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5539">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5540">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5540">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5541">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5542">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5543">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5544">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5545">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5546">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5547">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5548">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5549">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5549">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5551">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5552">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5553">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5554">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5555">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5555">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5556">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5557">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5557">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5559">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5560">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5561">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5562">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5562">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5564">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5564">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5565">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5565">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="68b50-5567">DXGI_FORMAT_BC4_TYPELESS<sup>ПКК</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="68b50-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="68b50-5568">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5568">Target</span></span> | <span data-ttu-id="68b50-5569">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5569">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5570">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5570">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5571">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5571">64</span></span> |
| <span data-ttu-id="68b50-5572">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5572">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5574">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5574">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5575">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5575">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5576">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5576">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5577">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5577">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5578">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5578">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5579">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5579">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5581">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5581">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5583">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5583">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5585">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5585">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-5586">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5586">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-5587">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5587">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5588">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5588">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5589">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5589">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-5590">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5590">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5591">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5591">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5593">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5593">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5594">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5594">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5595">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5595">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5596">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5596">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5597">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5597">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5598">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5598">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5599">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5599">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5600">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5600">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5601">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5601">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5602">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5602">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5603">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5603">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5604">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5604">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5605">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5605">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5606">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5606">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5607">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5607">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5608">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5608">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5609">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5609">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5611">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5611">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5612">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5612">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5613">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5613">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5614">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5614">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5615">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5615">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5616">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5616">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5617">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5617">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5619">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5619">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5620">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5620">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5621">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5621">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5622">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5622">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5623">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5623">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5624">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5624">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a><span data-ttu-id="68b50-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="68b50-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="68b50-5627">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5627">Target</span></span> | <span data-ttu-id="68b50-5628">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5628">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5629">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5629">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5630">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5630">64</span></span> |
| <span data-ttu-id="68b50-5631">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5631">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5633">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5633">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5634">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5634">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5635">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5635">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5636">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5636">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5637">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5637">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5638">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5640">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5642">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5644">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5644">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5646">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5646">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5648">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5648">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5649">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5649">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5650">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5650">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5652">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5652">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5653">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5653">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5655">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5655">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5656">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5656">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5657">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5657">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5658">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5658">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5659">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5659">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5660">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5660">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5661">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5661">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5662">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5662">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5663">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5663">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5664">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5664">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5665">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5665">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5666">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5666">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5667">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5667">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5668">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5668">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5669">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5669">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5670">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5670">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5671">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5671">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5673">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5673">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5674">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5674">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5675">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5675">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5676">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5676">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5677">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5677">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5678">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5678">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5679">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5679">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5681">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5681">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5682">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5682">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5683">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5683">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5684">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5684">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5685">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5685">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5686">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5686">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a><span data-ttu-id="68b50-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="68b50-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="68b50-5689">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5689">Target</span></span> | <span data-ttu-id="68b50-5690">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5690">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5691">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5691">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5692">64</span><span class="sxs-lookup"><span data-stu-id="68b50-5692">64</span></span> |
| <span data-ttu-id="68b50-5693">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5693">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5695">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5695">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5696">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5696">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5697">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5697">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5698">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5698">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5699">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5699">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5700">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5700">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5702">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5702">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5704">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5704">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5706">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5706">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5708">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5708">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5710">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5711">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5712">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5712">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5714">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5714">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5715">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5717">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5717">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5718">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5718">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5719">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5719">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5720">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5720">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5721">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5721">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5722">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5722">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5723">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5723">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5724">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5724">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5725">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5725">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5726">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5726">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5727">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5727">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5728">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5728">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5729">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5729">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5730">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5730">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5731">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5731">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5732">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5732">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5733">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5733">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5735">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5735">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5736">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5736">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5737">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5737">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5738">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5738">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5739">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5739">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5740">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5741">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5741">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5743">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5744">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5745">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5746">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5746">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5747">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5747">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5748">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5748">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="68b50-5750">DXGI_FORMAT_BC5_TYPELESS<sup>ПКК</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="68b50-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="68b50-5751">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5751">Target</span></span> | <span data-ttu-id="68b50-5752">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5752">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5753">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5753">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5754">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5754">128</span></span> |
| <span data-ttu-id="68b50-5755">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5755">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5757">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5757">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5758">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5759">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5760">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5761">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5762">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5764">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5766">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5766">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5768">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5768">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-5769">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5769">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-5770">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5770">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5771">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5771">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5772">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5772">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-5773">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5773">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5774">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5774">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5776">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5776">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5777">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5777">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5778">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5778">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5779">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5779">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5780">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5780">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5781">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5781">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5782">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5782">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5783">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5783">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5784">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5784">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5785">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5785">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5786">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5786">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5787">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5787">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5788">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5788">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5789">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5789">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5790">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5790">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5791">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5791">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5792">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5792">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5794">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5794">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5795">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5795">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5796">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5796">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5797">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5797">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5798">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5798">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5799">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5799">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5800">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5800">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5802">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5802">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5803">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5803">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5804">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5804">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5805">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5805">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5806">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5806">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5807">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5807">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a><span data-ttu-id="68b50-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="68b50-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="68b50-5810">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5810">Target</span></span> | <span data-ttu-id="68b50-5811">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5811">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5812">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5812">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5813">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5813">128</span></span> |
| <span data-ttu-id="68b50-5814">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5814">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5816">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5816">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5817">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5817">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5818">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5818">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5819">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5819">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5820">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5820">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5821">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5821">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5823">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5823">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5825">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5825">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5827">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5827">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5829">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5829">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5831">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5831">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5832">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5832">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5833">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5833">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5835">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5835">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5836">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5838">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5838">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5839">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5839">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5840">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5841">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5842">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5843">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5844">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5845">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5845">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5846">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5847">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5848">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5849">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5850">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5851">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5852">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5852">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5853">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5853">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5854">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5854">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5856">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5857">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5858">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5859">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5860">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5860">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5861">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5862">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5862">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5864">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5864">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5865">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5865">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5866">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5866">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5867">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5867">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5868">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5868">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5869">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5869">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a><span data-ttu-id="68b50-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="68b50-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="68b50-5872">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5872">Target</span></span> | <span data-ttu-id="68b50-5873">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5873">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5874">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5875">128</span><span class="sxs-lookup"><span data-stu-id="68b50-5875">128</span></span> |
| <span data-ttu-id="68b50-5876">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5876">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5878">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5878">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5879">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5880">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5881">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5882">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-5883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5883">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5885">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5887">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5887">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5889">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5889">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5891">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5891">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5893">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5894">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5895">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5895">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5897">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5898">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5900">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5900">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-5901">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5901">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5902">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5903">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5904">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5905">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5906">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5907">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5907">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-5908">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-5909">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-5910">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5911">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5912">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5913">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5914">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5914">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5915">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5915">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5916">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5916">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5918">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5918">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5919">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5919">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-5920">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5920">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-5921">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5921">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-5922">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5922">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-5923">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5923">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-5924">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-5924">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5926">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-5926">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-5927">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5927">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-5928">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-5928">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-5929">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5929">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-5930">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-5930">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-5931">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-5931">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="68b50-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>ФНС</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="68b50-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="68b50-5934">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-5934">Target</span></span> | <span data-ttu-id="68b50-5935">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-5935">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-5936">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-5936">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-5937">16</span><span class="sxs-lookup"><span data-stu-id="68b50-5937">16</span></span> |
| <span data-ttu-id="68b50-5938">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-5938">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5940">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-5940">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-5942">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5942">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-5944">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-5944">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5945">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-5945">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-5946">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-5946">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5948">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-5948">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-5950">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-5952">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5954">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-5954">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5956">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-5956">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5958">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-5958">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-5959">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-5959">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-5960">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5960">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5962">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-5962">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-5963">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5963">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5965">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-5965">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5967">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5967">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5969">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-5969">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5971">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-5971">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-5972">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-5972">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-5973">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5973">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5974">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-5974">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-5975">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5975">Typed UAV</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-5977">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-5977">UAV Typed Store</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-5979">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-5979">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-5981">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-5981">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-5982">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-5982">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-5983">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-5983">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-5984">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-5984">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-5985">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5985">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5986">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-5986">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-5987">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-5987">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5989">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5989">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5991">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-5991">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5993">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-5993">Other Multisample Count RT</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5995">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-5995">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5997">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-5997">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-5999">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-5999">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6000">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6000">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-6001">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6001">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6002">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6002">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6003">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6003">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6004">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6004">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6005">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6005">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6006">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6006">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="68b50-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>ФНС</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="68b50-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="68b50-6009">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6009">Target</span></span> | <span data-ttu-id="68b50-6010">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6010">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6011">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6011">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6012">16</span><span class="sxs-lookup"><span data-stu-id="68b50-6012">16</span></span> |
| <span data-ttu-id="68b50-6013">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6013">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6015">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6015">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6017">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6017">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6019">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6019">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6020">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6020">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6021">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6021">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6023">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6023">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6025">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6025">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6027">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6027">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6029">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6029">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6031">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6031">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6033">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6033">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6034">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6034">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6035">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6035">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6037">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6037">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6038">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6040">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6040">Mipmap Auto- Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6042">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6042">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6044">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6044">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6046">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6046">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6047">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6047">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6048">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6048">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6049">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6049">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6050">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6050">Typed UAV</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6052">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6052">UAV Typed Store</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6054">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6054">UAV Typed Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6056">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6057">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6058">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6059">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6060">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6060">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6061">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6061">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6062">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6062">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6064">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6064">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6066">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6066">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6068">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6068">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6070">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6070">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6072">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6072">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6074">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6074">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6075">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6075">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-6076">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6076">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6077">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6077">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6078">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6078">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6079">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6079">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6080">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6080">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6081">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6081">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="68b50-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>ПК</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="68b50-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="68b50-6084">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6084">Target</span></span> | <span data-ttu-id="68b50-6085">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6085">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6086">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6086">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6087">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6087">32</span></span> |
| <span data-ttu-id="68b50-6088">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6088">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6090">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6090">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6091">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6091">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6092">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6092">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6093">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6093">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6094">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6094">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6096">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6096">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6098">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6098">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6100">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6100">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6102">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6102">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-6103">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6103">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-6104">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6104">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6105">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6105">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6106">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6106">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-6107">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6107">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6108">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6108">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6110">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6110">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6111">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6111">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6112">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6113">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6114">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6115">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6116">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6117">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6117">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6118">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6119">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6120">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6121">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6122">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6123">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6124">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6124">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6125">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6125">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6126">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6126">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6128">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6128">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6129">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6129">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6130">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6130">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6131">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6131">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6132">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6132">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6133">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6133">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6134">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6134">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6136">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6137">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6138">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6139">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6139">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6141">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6141">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6142">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6142">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="68b50-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="68b50-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="68b50-6145">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6145">Target</span></span> | <span data-ttu-id="68b50-6146">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6146">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6147">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6148">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6148">32</span></span> |
| <span data-ttu-id="68b50-6149">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6149">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6151">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6151">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6153">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6153">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6155">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6155">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6156">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6156">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6157">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6157">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6159">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6159">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6161">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6161">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6163">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6165">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6165">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6167">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6167">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6169">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6169">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6170">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6170">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6171">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6171">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6173">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6173">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6174">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6174">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6176">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6176">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6178">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6178">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6180">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6180">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6182">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6182">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6183">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6183">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6184">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6184">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6185">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6185">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6186">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6186">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6187">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6187">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6188">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6188">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6189">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6189">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6190">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6190">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6191">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6191">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6192">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6192">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6193">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6193">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6194">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6194">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6195">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6195">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6197">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6197">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6199">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6199">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6201">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6201">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6203">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6203">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6205">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6205">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6207">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6207">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6209">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6209">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6211">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6211">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6212">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6212">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6214">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6214">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6216">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6216">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6218">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6218">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6220">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6220">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="68b50-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="68b50-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="68b50-6223">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6223">Target</span></span> | <span data-ttu-id="68b50-6224">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6224">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6225">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6225">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6226">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6226">32</span></span> |
| <span data-ttu-id="68b50-6227">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6227">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6229">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6229">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6230">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6230">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6231">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6232">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6233">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6235">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6237">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6239">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6241">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6241">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6243">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6243">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6245">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6245">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6246">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6246">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6247">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6247">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6249">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6249">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6250">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6250">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6252">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6252">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6254">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6254">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6256">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6256">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6258">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6258">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6259">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6259">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6260">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6260">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6261">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6261">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6262">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6262">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6263">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6263">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6264">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6264">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6265">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6265">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6266">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6266">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6267">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6267">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6268">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6268">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6269">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6269">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6270">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6270">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6271">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6271">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6273">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6273">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6275">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6275">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6277">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6277">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6279">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6279">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6281">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6281">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6283">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6283">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6285">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6285">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6287">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6287">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6288">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6288">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6290">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6290">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6292">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6292">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6294">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6294">BackBuffer Castable Even Fully Typed</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6296">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6296">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="68b50-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>ПК</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="68b50-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="68b50-6299">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6299">Target</span></span> | <span data-ttu-id="68b50-6300">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6300">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6301">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6301">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6302">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6302">32</span></span> |
| <span data-ttu-id="68b50-6303">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6303">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6305">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6305">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6306">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6306">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6307">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6307">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6308">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6308">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6309">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6309">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6311">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6311">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6313">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6313">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6315">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6315">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6317">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6317">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-6318">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6318">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-6319">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6319">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6320">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6320">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6321">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6321">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-6322">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6322">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6323">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6323">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6325">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6325">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6326">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6326">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6327">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6327">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6328">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6328">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6329">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6329">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6330">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6330">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6331">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6331">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6332">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6332">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6333">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6333">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6334">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6334">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6335">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6335">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6336">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6336">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6337">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6337">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6338">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6338">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6339">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6339">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6340">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6340">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6341">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6341">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6343">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6343">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6344">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6344">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6345">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6345">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6346">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6347">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6347">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6348">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6348">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6349">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6349">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6351">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6351">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6352">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6352">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6353">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6353">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6354">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6354">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6356">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6356">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6357">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6357">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="68b50-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="68b50-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="68b50-6360">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6360">Target</span></span> | <span data-ttu-id="68b50-6361">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6361">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6362">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6362">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6363">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6363">32</span></span> |
| <span data-ttu-id="68b50-6364">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6364">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6366">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6366">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6368">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6368">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6370">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6370">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6371">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6371">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6372">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6372">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6374">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6374">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6376">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6376">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6378">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6378">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6380">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6380">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6382">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6382">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6384">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6384">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6385">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6385">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6386">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6386">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6388">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6388">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6389">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6391">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6391">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6393">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6393">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6395">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6395">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6397">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6398">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6399">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6400">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6401">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6401">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6402">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6403">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6404">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6405">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6406">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6407">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6408">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6408">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6409">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6409">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6410">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6410">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6412">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6412">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6414">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6414">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6416">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6416">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6418">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6418">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6420">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6420">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6422">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6422">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6423">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6423">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6425">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6425">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6426">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6426">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6428">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6428">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6430">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6430">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6432">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6432">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6433">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6433">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="68b50-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="68b50-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="68b50-6436">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6436">Target</span></span> | <span data-ttu-id="68b50-6437">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6437">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6438">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6439">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6439">32</span></span> |
| <span data-ttu-id="68b50-6440">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6440">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6442">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6442">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6443">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6443">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6444">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6444">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6445">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6445">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6446">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6446">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6448">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6450">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6450">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6452">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6454">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6454">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6456">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6456">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6458">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6458">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6459">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6459">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6460">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6460">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6462">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6462">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6463">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6465">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6465">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6467">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6467">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6469">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6469">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6471">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6471">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6472">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6472">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6473">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6473">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6474">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6474">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6475">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6475">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6476">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6476">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6477">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6477">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6478">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6478">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6479">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6479">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6480">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6480">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6481">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6481">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6482">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6482">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6483">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6483">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6484">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6484">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6486">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6486">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6488">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6488">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6490">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6490">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6492">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6492">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6494">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6494">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6496">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6497">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6497">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6499">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6499">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6500">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6500">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6501">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6501">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6502">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6502">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6504">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6504">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6505">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6505">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a><span data-ttu-id="68b50-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>ПКК</sup> (94)</span><span class="sxs-lookup"><span data-stu-id="68b50-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span></span>
| <span data-ttu-id="68b50-6508">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6508">Target</span></span> | <span data-ttu-id="68b50-6509">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6509">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6510">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6510">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6511">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6511">128</span></span> |
| <span data-ttu-id="68b50-6512">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6512">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6514">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6514">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6515">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6515">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6516">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6516">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6517">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6517">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6518">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6518">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6519">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6519">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6521">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6521">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6523">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6525">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6525">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-6526">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6526">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-6527">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6527">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6528">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6528">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6529">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6529">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-6530">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6531">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6533">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6534">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6534">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6535">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6536">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6537">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6538">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6539">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6540">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6540">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6541">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6542">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6543">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6544">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6545">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6546">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6547">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6548">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6549">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6549">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6551">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6552">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6553">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6554">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6555">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6555">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6556">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6557">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6557">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6559">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6560">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6561">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6562">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6562">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6563">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6563">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6564">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6564">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a><span data-ttu-id="68b50-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span><span class="sxs-lookup"><span data-stu-id="68b50-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span></span>
| <span data-ttu-id="68b50-6567">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6567">Target</span></span> | <span data-ttu-id="68b50-6568">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6568">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6569">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6569">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6570">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6570">128</span></span> |
| <span data-ttu-id="68b50-6571">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6571">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6573">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6573">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6574">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6574">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6575">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6575">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6576">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6576">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6577">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6577">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6578">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6578">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6580">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6580">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6582">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6582">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6584">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6584">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6586">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6586">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6588">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6588">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6589">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6589">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6590">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6590">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6592">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6592">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6593">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6593">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6595">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6595">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6596">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6596">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6597">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6597">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6598">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6598">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6599">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6599">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6600">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6600">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6601">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6601">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6602">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6602">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6603">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6603">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6604">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6604">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6605">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6605">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6606">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6606">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6607">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6607">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6608">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6608">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6609">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6609">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6610">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6610">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6611">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6611">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6613">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6613">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6614">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6614">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6615">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6615">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6616">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6616">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6617">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6617">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6618">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6618">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6619">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6619">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6621">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6622">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6622">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6623">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6623">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6624">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6624">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6625">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6625">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6626">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6626">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a><span data-ttu-id="68b50-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span><span class="sxs-lookup"><span data-stu-id="68b50-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span></span>
| <span data-ttu-id="68b50-6629">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6629">Target</span></span> | <span data-ttu-id="68b50-6630">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6630">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6631">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6632">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6632">128</span></span> |
| <span data-ttu-id="68b50-6633">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6633">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6635">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6635">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6636">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6637">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6638">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6639">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6640">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6642">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6644">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6646">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6646">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6648">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6648">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6650">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6651">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6652">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6652">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6654">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6655">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6657">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6657">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6658">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6658">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6659">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6659">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6660">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6661">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6662">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6663">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6664">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6664">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6665">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6666">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6667">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6668">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6669">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6669">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6670">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6671">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6671">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6672">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6672">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6673">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6673">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6675">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6675">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6676">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6676">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6677">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6677">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6678">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6678">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6679">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6679">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6680">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6680">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6681">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6681">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6683">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6683">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6684">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6684">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6685">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6685">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6686">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6686">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6687">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6687">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6688">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6688">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a><span data-ttu-id="68b50-6690">DXGI_FORMAT_BC7_TYPELESS<sup>ПКК</sup> (97)</span><span class="sxs-lookup"><span data-stu-id="68b50-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span></span>
| <span data-ttu-id="68b50-6691">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6691">Target</span></span> | <span data-ttu-id="68b50-6692">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6692">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6693">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6693">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6694">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6694">128</span></span> |
| <span data-ttu-id="68b50-6695">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6695">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6697">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6697">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6698">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6698">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6699">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6699">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6700">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6700">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6701">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6701">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6702">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6704">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6706">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6708">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6708">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-6709">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6709">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-6710">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6711">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6712">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6712">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-6713">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6713">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6714">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6714">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6716">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6716">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6717">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6717">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6718">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6719">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6720">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6721">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6722">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6723">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6723">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6724">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6725">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6726">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6727">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6728">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6729">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6730">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6730">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6731">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6731">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6732">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6732">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6734">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6734">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6735">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6735">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6736">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6736">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6737">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6738">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6738">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6739">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6739">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6740">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6740">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6742">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6742">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6743">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6743">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6744">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6744">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6745">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6745">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6746">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6746">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6747">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6747">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a><span data-ttu-id="68b50-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span><span class="sxs-lookup"><span data-stu-id="68b50-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span></span>
| <span data-ttu-id="68b50-6750">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6750">Target</span></span> | <span data-ttu-id="68b50-6751">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6751">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6752">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6752">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6753">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6753">128</span></span> |
| <span data-ttu-id="68b50-6754">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6754">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6756">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6756">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6757">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6757">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6758">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6758">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6759">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6759">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6760">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6760">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6761">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6761">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6763">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6765">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6767">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6767">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6769">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6769">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6771">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6771">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6772">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6772">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6773">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6773">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6775">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6775">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6776">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6778">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6778">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6779">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6779">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6780">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6780">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6781">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6781">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6782">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6782">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6783">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6783">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6784">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6784">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6785">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6785">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6786">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6786">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6787">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6787">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6788">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6789">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6790">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6791">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6792">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6793">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6794">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6794">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6796">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6796">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6797">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6797">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6798">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6798">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6799">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6799">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6800">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6800">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6801">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6801">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6802">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6802">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6804">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6804">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6805">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6805">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6806">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6806">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6807">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6807">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6808">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6808">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6809">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6809">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a><span data-ttu-id="68b50-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span><span class="sxs-lookup"><span data-stu-id="68b50-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span></span>
| <span data-ttu-id="68b50-6812">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6812">Target</span></span> | <span data-ttu-id="68b50-6813">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6813">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6814">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6814">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6815">128</span><span class="sxs-lookup"><span data-stu-id="68b50-6815">128</span></span> |
| <span data-ttu-id="68b50-6816">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6816">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6818">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6818">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6819">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6819">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6820">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6820">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6821">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6821">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6822">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6822">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6823">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6823">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6825">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6825">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6827">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6829">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6829">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6831">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6831">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6833">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6833">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6834">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6834">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6835">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6835">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6837">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6837">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6838">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6840">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6840">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6841">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6842">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6843">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6844">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6845">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6846">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6847">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-6848">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-6849">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6850">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6851">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6852">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6852">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6853">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6854">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6854">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6855">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6855">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6856">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6856">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6858">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6859">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6860">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6861">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6862">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6863">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6864">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6864">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6866">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-6867">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6867">Video Processor Input</span></span> | \- |
| <span data-ttu-id="68b50-6868">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-6869">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-6870">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6871">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6871">Tiled Resource</span></span> | ![обязательно](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="68b50-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="68b50-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="68b50-6874">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6874">Target</span></span> | <span data-ttu-id="68b50-6875">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6875">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6876">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6877">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6877">32</span></span> |
| <span data-ttu-id="68b50-6878">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6878">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6880">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6880">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6881">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6881">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6882">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6882">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6883">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6883">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6884">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6884">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6885">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6885">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6887">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6887">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-6888">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6888">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-6889">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6889">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6891">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6891">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6893">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6894">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6895">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6895">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6897">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6898">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6900">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6900">Mipmap Auto- Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6902">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6902">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6904">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6904">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6906">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6906">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6907">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6907">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6908">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6908">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6909">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6909">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6910">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6910">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6912">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6912">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6914">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6914">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6915">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6915">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6916">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6916">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6917">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6917">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6918">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6918">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6919">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6919">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6920">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6920">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6921">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6921">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6923">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6923">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6924">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6924">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6925">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6925">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6926">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6926">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6927">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6927">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6928">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6928">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6929">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6929">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-6930">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6930">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6932">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6932">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6934">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6934">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6936">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6936">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6938">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-6938">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-6939">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="68b50-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="68b50-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="68b50-6941">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-6941">Target</span></span> | <span data-ttu-id="68b50-6942">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-6942">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-6943">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-6943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-6944">32</span><span class="sxs-lookup"><span data-stu-id="68b50-6944">32</span></span> |
| <span data-ttu-id="68b50-6945">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-6945">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6947">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-6947">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6948">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6948">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6949">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-6949">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6950">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-6950">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-6951">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-6951">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-6952">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-6952">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6954">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-6954">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-6955">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-6955">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-6956">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-6956">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6958">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-6958">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6960">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-6960">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-6961">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-6961">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-6962">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6962">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6964">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-6964">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-6965">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6965">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-6966">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-6966">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-6967">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6967">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6968">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-6968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6969">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-6969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-6970">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-6970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-6971">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6972">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-6972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-6973">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6973">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6975">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-6975">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6977">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-6977">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-6978">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-6978">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-6979">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-6979">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-6980">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-6980">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-6981">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-6981">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-6982">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6982">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6983">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-6983">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-6984">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-6984">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-6986">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6986">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6987">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-6987">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-6988">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-6988">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-6989">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-6989">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-6990">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-6990">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-6991">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-6991">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-6992">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-6992">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-6993">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-6993">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6995">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6995">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6997">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-6997">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-6999">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-6999">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7001">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7001">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7002">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7002">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="68b50-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="68b50-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="68b50-7004">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7004">Target</span></span> | <span data-ttu-id="68b50-7005">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7005">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7006">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7006">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7007">64</span><span class="sxs-lookup"><span data-stu-id="68b50-7007">64</span></span> |
| <span data-ttu-id="68b50-7008">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7008">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7010">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7010">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7011">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7011">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7012">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7012">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7013">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7013">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7014">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7014">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7015">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7015">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7017">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7017">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7018">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7018">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7019">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7019">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7021">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7021">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7023">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7023">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7024">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7024">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7025">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7025">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7027">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7027">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7028">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7030">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7030">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7031">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7031">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7032">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7032">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7033">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7033">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7034">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7034">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7035">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7035">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7036">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7036">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7037">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7037">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7039">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7039">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7041">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7041">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7042">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7042">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7043">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7043">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7044">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7044">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7045">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7045">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7046">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7046">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7047">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7047">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7048">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7048">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7050">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7050">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7051">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7051">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7052">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7052">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7053">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7053">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7054">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7054">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7055">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7055">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7056">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7056">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7057">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7057">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7059">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7059">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7061">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7061">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7063">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7063">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7065">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7065">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7066">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7066">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="68b50-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="68b50-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="68b50-7068">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7068">Target</span></span> | <span data-ttu-id="68b50-7069">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7069">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7070">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7070">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7071">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7071">8</span></span> |
| <span data-ttu-id="68b50-7072">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7072">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7074">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7074">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7075">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7075">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7076">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7076">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7077">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7077">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7078">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7078">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7079">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7079">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7081">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7081">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7082">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7082">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7083">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7083">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7085">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7085">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7087">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7087">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7088">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7088">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7089">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7089">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7091">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7091">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7092">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7092">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7093">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7093">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7094">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7094">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7096">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7096">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7098">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7099">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7100">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7101">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7102">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7102">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7104">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7104">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7106">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7106">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7107">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7107">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7108">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7108">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7109">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7109">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7110">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7110">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7111">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7111">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7112">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7112">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7113">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7113">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7115">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7116">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7117">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7118">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7119">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7119">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7120">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7121">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7122">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7122">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7124">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7124">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7126">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7126">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7128">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7128">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7130">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7130">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7131">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7131">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="68b50-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="68b50-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="68b50-7133">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7133">Target</span></span> | <span data-ttu-id="68b50-7134">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7134">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7135">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7136">16</span><span class="sxs-lookup"><span data-stu-id="68b50-7136">16</span></span> |
| <span data-ttu-id="68b50-7137">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7137">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7139">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7139">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7140">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7141">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7142">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7143">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7144">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7146">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7147">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7147">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7148">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7148">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7150">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7150">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7152">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7152">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7153">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7153">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7154">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7154">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7156">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7157">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7158">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7158">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7159">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7159">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7161">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7161">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7163">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7164">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7165">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7166">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7167">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7167">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7169">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7169">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7171">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7172">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7173">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7174">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7175">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7176">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7176">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7177">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7177">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7178">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7178">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7180">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7181">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7182">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7183">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7184">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7184">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7185">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7186">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7186">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7187">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7187">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7189">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7189">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7191">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7191">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7193">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7193">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7195">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7195">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7196">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7196">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="68b50-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="68b50-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="68b50-7198">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7198">Target</span></span> | <span data-ttu-id="68b50-7199">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7199">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7200">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7200">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7201">16</span><span class="sxs-lookup"><span data-stu-id="68b50-7201">16</span></span> |
| <span data-ttu-id="68b50-7202">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7202">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7204">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7204">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7205">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7205">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7206">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7206">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7207">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7207">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7208">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7208">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7209">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7209">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7211">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7211">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7212">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7212">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7213">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7213">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7215">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7215">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7217">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7217">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7218">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7218">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7219">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7219">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7221">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7221">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7222">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7222">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7223">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7223">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7224">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7224">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7226">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7226">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7228">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7228">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7229">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7229">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7230">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7230">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7231">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7231">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7232">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7232">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7234">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7234">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7236">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7237">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7238">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7239">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7240">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7241">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7241">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7242">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7242">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7243">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7243">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7245">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7246">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7247">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7248">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7249">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7249">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7250">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7251">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7252">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7252">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7254">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7254">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7256">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7256">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7258">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7258">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7260">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7260">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7261">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7261">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="68b50-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="68b50-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="68b50-7263">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7263">Target</span></span> | <span data-ttu-id="68b50-7264">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7264">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7265">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7265">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7266">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7266">8</span></span> |
| <span data-ttu-id="68b50-7267">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7267">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7269">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7269">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7270">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7270">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7271">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7271">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7272">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7272">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7273">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7273">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7274">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7274">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7276">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7276">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7277">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7277">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7278">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7278">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-7279">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7279">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-7280">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7280">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7281">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7281">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7282">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7282">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-7283">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7283">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7284">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7284">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7285">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7285">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7286">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7286">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7287">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7287">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7288">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7288">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7289">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7289">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7290">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7290">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7291">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7291">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7292">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7292">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-7293">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7293">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-7294">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7294">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7295">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7295">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7296">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7296">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7297">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7297">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7298">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7298">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7299">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7299">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7300">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7300">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7301">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7301">CPU Lockable</span></span> | \- |
| <span data-ttu-id="68b50-7302">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7303">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7304">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7305">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7306">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7306">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7307">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7308">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7308">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7309">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7309">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7311">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7311">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7313">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7313">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7315">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7315">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7317">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7317">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7318">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7318">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="68b50-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="68b50-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="68b50-7320">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7320">Target</span></span> | <span data-ttu-id="68b50-7321">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7321">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7322">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7323">16</span><span class="sxs-lookup"><span data-stu-id="68b50-7323">16</span></span> |
| <span data-ttu-id="68b50-7324">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7324">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7326">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7326">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7327">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7327">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7328">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7328">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7329">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7329">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7330">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7331">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7331">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7333">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7333">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7334">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7335">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7335">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7337">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7337">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7339">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7339">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7340">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7340">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7341">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7341">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7343">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7343">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7344">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7344">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7345">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7345">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7346">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7346">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7347">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7348">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7349">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7350">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7351">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7352">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7352">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7354">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7354">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7356">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7357">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7358">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7359">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7360">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7361">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7362">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7363">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7363">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7365">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7366">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7367">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7368">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7369">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7369">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7370">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7371">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7371">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7372">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7372">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7374">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7374">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7376">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7376">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7378">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7378">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7380">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7380">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7381">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7381">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="68b50-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="68b50-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="68b50-7383">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7383">Target</span></span> | <span data-ttu-id="68b50-7384">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7384">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7385">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7386">32</span><span class="sxs-lookup"><span data-stu-id="68b50-7386">32</span></span> |
| <span data-ttu-id="68b50-7387">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7387">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7389">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7389">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7390">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7390">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7391">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7391">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7392">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7392">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7393">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7393">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7394">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7396">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7397">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7398">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7398">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7400">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7400">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7402">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7402">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7403">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7403">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7404">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7404">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7406">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7406">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7407">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7408">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7408">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7409">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7409">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7410">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7411">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7412">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7413">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7414">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7415">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7415">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7417">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7417">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7419">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7419">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7420">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7420">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7421">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7421">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7422">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7422">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7423">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7423">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7424">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7424">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7425">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7425">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7426">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7426">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7428">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7429">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7430">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7431">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7432">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7432">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7433">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7434">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7435">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7435">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7437">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7437">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7439">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7439">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7441">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7441">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7443">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7443">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7444">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7444">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="68b50-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="68b50-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="68b50-7446">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7446">Target</span></span> | <span data-ttu-id="68b50-7447">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7447">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7448">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7448">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7449">32</span><span class="sxs-lookup"><span data-stu-id="68b50-7449">32</span></span> |
| <span data-ttu-id="68b50-7450">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7450">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7452">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7452">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7453">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7453">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7454">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7454">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7455">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7455">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7456">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7456">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7457">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7457">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7459">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7459">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7460">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7460">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7461">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7461">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7463">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7463">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7465">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7465">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7466">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7466">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7467">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7467">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7469">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7469">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7470">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7471">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7471">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7472">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7472">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7473">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7474">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7475">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7476">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7477">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7478">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7478">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7480">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7480">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7482">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7482">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7483">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7483">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7484">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7484">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7485">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7485">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7486">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7486">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7487">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7487">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7488">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7488">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7489">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7489">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7491">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7491">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7492">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7492">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7493">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7493">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7494">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7494">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7495">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7495">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7496">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7497">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7497">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7498">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7498">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7500">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7500">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7502">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7502">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7504">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7504">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7506">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7506">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7507">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7507">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="68b50-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="68b50-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="68b50-7509">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7509">Target</span></span> | <span data-ttu-id="68b50-7510">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7510">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7511">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7511">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7512">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7512">8</span></span> |
| <span data-ttu-id="68b50-7513">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7513">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7515">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7515">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7516">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7516">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7517">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7517">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7518">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7518">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7519">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7519">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7520">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7520">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7522">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7522">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7523">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7524">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7524">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7526">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7526">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7528">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7528">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7529">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7529">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7530">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7530">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7532">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7532">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7533">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7533">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7534">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7534">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7535">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7535">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7537">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7537">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7539">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7539">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7540">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7540">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7541">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7541">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7542">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7542">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7543">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7543">Typed UAV</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7545">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7545">UAV Typed Store</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7547">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7547">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7548">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7548">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7549">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7549">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7550">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7550">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7551">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7551">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7552">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7552">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7553">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7553">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7554">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7554">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7556">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7556">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7557">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7557">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7558">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7558">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7559">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7559">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7560">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7560">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7561">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7561">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7562">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7562">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7563">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7563">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7565">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7565">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7567">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7567">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7569">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7569">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7571">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7571">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7572">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7572">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="68b50-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="68b50-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="68b50-7574">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7574">Target</span></span> | <span data-ttu-id="68b50-7575">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7575">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7576">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7576">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7577">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7577">8</span></span> |
| <span data-ttu-id="68b50-7578">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7578">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7580">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7580">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7581">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7581">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7582">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7583">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7583">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7584">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7584">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7585">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7585">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7587">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7587">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7588">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7588">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7589">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7589">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-7590">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7590">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-7591">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7591">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7592">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7592">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7593">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7593">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-7594">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7594">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7595">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7595">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7596">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7596">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7597">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7597">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7598">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7598">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7599">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7599">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7600">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7600">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7601">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7601">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7602">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7602">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7603">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7603">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-7604">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7604">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-7605">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7605">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7606">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7606">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7607">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7607">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7608">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7608">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7609">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7609">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7610">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7610">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7611">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7611">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7612">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7612">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7614">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7614">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7615">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7615">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7616">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7616">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7617">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7617">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7618">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7618">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7619">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7619">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7620">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7620">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7621">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-7622">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7622">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7624">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7624">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-7625">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7625">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-7626">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7626">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7627">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7627">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="68b50-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="68b50-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="68b50-7629">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7629">Target</span></span> | <span data-ttu-id="68b50-7630">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7630">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7631">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7632">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7632">8</span></span> |
| <span data-ttu-id="68b50-7633">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7633">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7635">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7635">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7636">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7637">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7638">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7639">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7640">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7642">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7643">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7643">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7644">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7644">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-7645">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7645">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-7646">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7646">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7647">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7647">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7648">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7648">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-7649">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7649">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7650">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7650">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7651">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7651">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7652">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7652">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7653">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7654">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7655">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7656">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7657">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7658">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7658">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-7659">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-7660">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7661">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7662">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7663">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7663">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7664">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7665">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7665">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7666">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7666">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7667">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7667">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7669">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7669">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7670">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7670">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7671">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7671">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7672">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7672">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7673">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7673">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7674">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7674">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7675">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7675">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7676">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7676">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-7677">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7677">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7679">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-7680">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7680">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-7681">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7681">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7682">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="68b50-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="68b50-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="68b50-7684">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7684">Target</span></span> | <span data-ttu-id="68b50-7685">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7685">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7686">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7687">8</span><span class="sxs-lookup"><span data-stu-id="68b50-7687">8</span></span> |
| <span data-ttu-id="68b50-7688">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7688">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7690">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7690">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7691">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7691">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7692">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7692">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7693">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7693">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7694">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7694">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7695">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7695">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7697">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7697">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7698">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7699">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7699">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-7700">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7700">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-7701">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7701">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7702">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7702">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7703">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7703">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-7704">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7704">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7705">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7705">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7706">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7706">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7707">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7707">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7708">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7708">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7709">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7709">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7710">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7710">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7711">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7711">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7712">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7712">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7713">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7713">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-7714">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7714">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-7715">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7715">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7716">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7716">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7717">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7717">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7718">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7718">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7719">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7719">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7720">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7720">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7721">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7721">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7722">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7722">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7724">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7724">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7725">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7725">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7726">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7726">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7727">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7728">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7728">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7729">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7729">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7730">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7730">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7731">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7731">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-7732">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7732">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7734">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7734">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-7735">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7735">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-7736">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7736">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7737">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7737">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="68b50-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="68b50-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="68b50-7739">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="68b50-7739">Target</span></span> | <span data-ttu-id="68b50-7740">Поддержка</span><span class="sxs-lookup"><span data-stu-id="68b50-7740">Support</span></span> |
| - | - |
| <span data-ttu-id="68b50-7741">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="68b50-7741">Bits Per Element (BPE)</span></span> | <span data-ttu-id="68b50-7742">16</span><span class="sxs-lookup"><span data-stu-id="68b50-7742">16</span></span> |
| <span data-ttu-id="68b50-7743">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="68b50-7743">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="68b50-7745">Буфер</span><span class="sxs-lookup"><span data-stu-id="68b50-7745">Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7746">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7746">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7747">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="68b50-7747">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7748">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="68b50-7748">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="68b50-7749">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68b50-7749">Texture1D</span></span> | \- |
| <span data-ttu-id="68b50-7750">Texture2D</span><span class="sxs-lookup"><span data-stu-id="68b50-7750">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7752">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68b50-7752">Texture3D</span></span> | \- |
| <span data-ttu-id="68b50-7753">TextureCube</span><span class="sxs-lookup"><span data-stu-id="68b50-7753">TextureCube</span></span> | \- |
| <span data-ttu-id="68b50-7754">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="68b50-7754">Shader ld</span></span> | \- |
| <span data-ttu-id="68b50-7755">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="68b50-7755">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="68b50-7756">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="68b50-7756">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="68b50-7757">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="68b50-7757">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="68b50-7758">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7758">Shader gather4</span></span> | \- |
| <span data-ttu-id="68b50-7759">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="68b50-7759">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="68b50-7760">Mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7760">Mipmap</span></span> | \- |
| <span data-ttu-id="68b50-7761">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="68b50-7761">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="68b50-7762">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7762">RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7763">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="68b50-7763">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7764">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="68b50-7764">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="68b50-7765">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="68b50-7765">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="68b50-7766">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7766">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7767">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="68b50-7767">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="68b50-7768">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7768">Typed UAV</span></span> | \- |
| <span data-ttu-id="68b50-7769">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="68b50-7769">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="68b50-7770">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="68b50-7770">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="68b50-7771">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="68b50-7771">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="68b50-7772">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="68b50-7772">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="68b50-7773">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="68b50-7773">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="68b50-7774">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="68b50-7774">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="68b50-7775">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7775">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7776">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="68b50-7776">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="68b50-7777">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="68b50-7777">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7779">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7779">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7780">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="68b50-7780">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="68b50-7781">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="68b50-7781">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="68b50-7782">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="68b50-7782">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="68b50-7783">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="68b50-7783">Multisample Load</span></span> | \- |
| <span data-ttu-id="68b50-7784">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="68b50-7784">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="68b50-7785">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="68b50-7785">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="68b50-7786">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="68b50-7786">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="68b50-7787">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7787">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="68b50-7789">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7789">Video Processor Output</span></span> | \- |
| <span data-ttu-id="68b50-7790">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7790">Shared Resource</span></span> | \- |
| <span data-ttu-id="68b50-7791">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="68b50-7791">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="68b50-7792">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="68b50-7792">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="68b50-7793">Форматирование заметок</span><span class="sxs-lookup"><span data-stu-id="68b50-7793">Format notes</span></span>

<span data-ttu-id="68b50-7794">Назначение формата может изменяться с одного уровня компонентов оборудования на следующий.</span><span class="sxs-lookup"><span data-stu-id="68b50-7794">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="68b50-7795"><sup>L</sup> : нетипизированный формат</span><span class="sxs-lookup"><span data-stu-id="68b50-7795"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="68b50-7796"><sup>ПК</sup> : частично типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7796"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="68b50-7797"><sup>FCS</sup> : полностью типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7797"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="68b50-7798"><sup>ФНС</sup> : полностью типизированный, неприведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7798"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="68b50-7799"><sup>ПКК</sup> : частично типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7799"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="68b50-7800"><sup>FCC</sup> : полностью типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7800"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="68b50-7801"><sup>ФНК</sup> : полностью типизированный, неприведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="68b50-7801"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="68b50-7802"><sup>V</sup> : формат видео</span><span class="sxs-lookup"><span data-stu-id="68b50-7802"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="dxgi_format_related-topics"></a><span data-ttu-id="68b50-7803">DXGI_FORMAT_Related статьи</span><span class="sxs-lookup"><span data-stu-id="68b50-7803">DXGI_FORMAT_Related topics</span></span>

[<span data-ttu-id="68b50-7804">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="68b50-7804">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="68b50-7805">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="68b50-7805">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
