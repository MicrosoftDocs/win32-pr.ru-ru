---
description: В этом разделе указаны форматы ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 10,1.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Поддержка форматов для оборудования Direct3D с уровнем компонентов 10.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494724"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="386eb-103">Поддержка форматов для оборудования Direct3D с уровнем компонентов 10.1</span><span class="sxs-lookup"><span data-stu-id="386eb-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="386eb-104">В этом разделе указаны форматы ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="386eb-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="386eb-105">В таблице приводится сводка по поддержке функций с использованием следующего ключа.</span><span class="sxs-lookup"><span data-stu-id="386eb-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="386eb-106">Символ</span><span class="sxs-lookup"><span data-stu-id="386eb-106">Symbol</span></span>                            | <span data-ttu-id="386eb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="386eb-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="386eb-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="386eb-108">_ *-*\*</span></span>                             | <span data-ttu-id="386eb-109">Не разрешено или недоступно.</span><span class="sxs-lookup"><span data-stu-id="386eb-109">Disallowed or not available.</span></span>                                                  |
| ![обязательно](images/letter-r.jpg)  | <span data-ttu-id="386eb-111">Требуется поддержка оборудования.</span><span class="sxs-lookup"><span data-stu-id="386eb-111">Hardware support is required.</span></span>                                                 |
| ![необязательно](images/letter-o.jpg)  | <span data-ttu-id="386eb-113">Аппаратная поддержка необязательно. формат аппаратного ускорения может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="386eb-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![зависимых](images/letter-d.jpg) | <span data-ttu-id="386eb-115">Требуется, если поддерживается дополнительная функция.</span><span class="sxs-lookup"><span data-stu-id="386eb-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="386eb-116">Этот раздел содержит раздел для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="386eb-116">This topic contains a section per format.</span></span> <span data-ttu-id="386eb-117">*Цель* формата (таблицы содержат по одной строке на каждый целевой объект) может быть типом ресурса, встроенной функцией HLSL или определенной функциональностью, зависящей от конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="386eb-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="386eb-118">Чтобы программно проверить поддержку формата в D3D11 и D3D12, обратитесь к статье [Проверка поддержки аппаратных компонентов](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="386eb-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="386eb-119">Числа форматов в основном, но не все, в возрастающем числовом порядке &mdash; , некоторые из них имеют нечисловой порядок и перечислены вместе с другими соответствующими форматами.</span><span class="sxs-lookup"><span data-stu-id="386eb-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="386eb-120">Обратите внимание, что *тип* в имени формата может означать *частичную* типизацию, а не строго типизированный (см. раздел [Format Notes](#format-notes) в конце раздела).</span><span class="sxs-lookup"><span data-stu-id="386eb-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="386eb-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="386eb-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="386eb-122">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-122">Target</span></span> | <span data-ttu-id="386eb-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-123">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-124">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-125">0</span><span class="sxs-lookup"><span data-stu-id="386eb-125">0</span></span> |
| <span data-ttu-id="386eb-126">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-126">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-128">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-128">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-130">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-131">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-132">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-133">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-134">Texture2D</span></span> | \- |
| <span data-ttu-id="386eb-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-135">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-136">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-137">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-137">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-138">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-139">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-140">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-141">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-142">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-143">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-144">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-145">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-146">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-147">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-148">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-149">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-150">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-151">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-152">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-153">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-154">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-155">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-156">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-157">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-158">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-159">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-160">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-160">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-162">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-163">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-164">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-165">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-166">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-167">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-168">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-169">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-170">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-171">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-172">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-173">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="386eb-174">\_Нетипизированные<sup>ПК</sup> DXGI_FORMAT_R32G32B32A32 (1)</span><span class="sxs-lookup"><span data-stu-id="386eb-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="386eb-175">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-175">Target</span></span> | <span data-ttu-id="386eb-176">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-176">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-177">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-178">128</span><span class="sxs-lookup"><span data-stu-id="386eb-178">128</span></span> |
| <span data-ttu-id="386eb-179">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-179">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-181">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-181">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-182">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-183">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-184">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-185">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-187">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-189">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-191">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-193">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-193">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-194">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-195">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-196">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-197">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-198">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-199">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-201">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-202">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-203">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-204">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-205">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-206">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-207">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-208">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-209">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-210">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-211">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-212">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-213">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-214">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-215">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-216">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-217">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-217">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-219">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-220">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-221">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-222">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-223">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-224">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-225">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-225">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-227">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-228">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-229">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-230">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-230">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-232">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="386eb-233">DXGI_FORMAT_R32G32B32A32 \_ с<sup></sup> плавающей запятой (2)</span><span class="sxs-lookup"><span data-stu-id="386eb-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="386eb-234">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-234">Target</span></span> | <span data-ttu-id="386eb-235">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-235">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-236">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-237">128</span><span class="sxs-lookup"><span data-stu-id="386eb-237">128</span></span> |
| <span data-ttu-id="386eb-238">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-238">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-240">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-240">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-242">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-242">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-244">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-245">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-245">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-247">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-249">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-251">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-253">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-255">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-255">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-257">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-257">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-259">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-260">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-261">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-262">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-263">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-265">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-265">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-267">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-267">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-269">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-269">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-271">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-272">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-273">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-274">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-275">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-276">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-277">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-278">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-279">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-280">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-281">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-282">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-283">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-284">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-284">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-286">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-286">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-288">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-288">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-290">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-290">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-292">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-292">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-294">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-294">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-296">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-297">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-297">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-299">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-300">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-301">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-302">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-302">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-304">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="386eb-305">DXGI_FORMAT_R32G32B32A32ое \_ <sup>FCS</sup> /uint (3)</span><span class="sxs-lookup"><span data-stu-id="386eb-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="386eb-306">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-306">Target</span></span> | <span data-ttu-id="386eb-307">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-307">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-308">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-309">128</span><span class="sxs-lookup"><span data-stu-id="386eb-309">128</span></span> |
| <span data-ttu-id="386eb-310">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-310">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-312">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-312">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-314">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-314">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-316">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-317">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-317">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-319">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-321">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-323">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-325">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-327">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-327">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-329">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-330">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-331">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-332">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-333">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-334">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-336">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-337">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-337">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-339">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-340">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-340">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-342">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-343">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-344">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-345">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-346">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-347">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-348">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-349">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-350">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-351">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-352">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-353">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-354">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-354">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-356">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-356">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-358">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-358">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-360">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-360">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-362">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-363">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-363">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-365">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-366">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-366">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-368">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-369">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-370">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-371">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-371">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-373">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="386eb-374">DXGI_FORMAT_R32G32B32A32 \_ Синт-<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="386eb-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="386eb-375">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-375">Target</span></span> | <span data-ttu-id="386eb-376">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-376">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-377">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-378">128</span><span class="sxs-lookup"><span data-stu-id="386eb-378">128</span></span> |
| <span data-ttu-id="386eb-379">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-379">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-381">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-381">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-383">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-383">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-385">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-386">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-386">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-388">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-390">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-392">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-394">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-396">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-396">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-398">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-399">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-400">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-401">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-402">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-403">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-405">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-406">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-406">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-408">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-409">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-410">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-411">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-412">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-413">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-414">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-415">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-416">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-417">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-418">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-419">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-420">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-421">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-422">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-422">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-424">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-424">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-426">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-426">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-428">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-428">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-430">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-431">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-431">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-433">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-434">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-434">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-436">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-437">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-438">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-439">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-439">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-441">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="386eb-442">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32B32 (5)</span><span class="sxs-lookup"><span data-stu-id="386eb-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="386eb-443">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-443">Target</span></span> | <span data-ttu-id="386eb-444">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-444">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-445">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-446">96</span><span class="sxs-lookup"><span data-stu-id="386eb-446">96</span></span> |
| <span data-ttu-id="386eb-447">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-447">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-449">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-449">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-450">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-451">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-452">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-453">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-455">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-457">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-459">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-461">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-461">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-462">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-463">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-464">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-465">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-466">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-467">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-469">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-470">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-471">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-472">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-473">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-474">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-475">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-476">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-477">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-478">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-479">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-480">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-481">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-482">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-483">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-484">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-485">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-485">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-487">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-488">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-489">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-490">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-491">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-492">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-493">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-493">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-495">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-496">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-497">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-498">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-499">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="386eb-500">DXGI_FORMAT_R32G32B32 \_ с<sup></sup> плавающей запятой (6)</span><span class="sxs-lookup"><span data-stu-id="386eb-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="386eb-501">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-501">Target</span></span> | <span data-ttu-id="386eb-502">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-502">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-503">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-504">96</span><span class="sxs-lookup"><span data-stu-id="386eb-504">96</span></span> |
| <span data-ttu-id="386eb-505">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-505">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-507">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-507">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-509">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-509">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-511">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-512">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-512">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-514">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-516">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-518">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-520">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-522">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-522">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-524">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-524">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-526">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-527">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-528">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-529">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-530">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-532">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-532">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-534">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-534">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-536">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-536">Blendable RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-538">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-539">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-540">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-541">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-542">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-543">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-544">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-545">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-546">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-547">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-548">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-549">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-550">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-551">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-551">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-553">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-553">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-555">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-555">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-557">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-557">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-559">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-559">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-561">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-561">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-563">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-564">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-564">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-566">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-567">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-568">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-569">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-570">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="386eb-571">DXGI_FORMAT_R32G32B32ости \_ uint (7)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="386eb-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="386eb-572">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-572">Target</span></span> | <span data-ttu-id="386eb-573">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-573">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-574">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-575">96</span><span class="sxs-lookup"><span data-stu-id="386eb-575">96</span></span> |
| <span data-ttu-id="386eb-576">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-576">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-578">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-578">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-580">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-580">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-582">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-583">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-583">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-585">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-587">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-589">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-591">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-593">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-593">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-595">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-596">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-597">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-598">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-599">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-600">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-602">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-603">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-603">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-605">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-606">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-606">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-608">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-609">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-610">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-611">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-612">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-613">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-614">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-615">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-616">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-617">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-618">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-619">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-620">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-620">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-622">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-622">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-624">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-624">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-626">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-626">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-628">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-629">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-629">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-631">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-632">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-632">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-634">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-635">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-636">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-637">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-638">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="386eb-639">DXGI_FORMAT_R32G32B32 \_ Синт-<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="386eb-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="386eb-640">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-640">Target</span></span> | <span data-ttu-id="386eb-641">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-641">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-642">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-643">96</span><span class="sxs-lookup"><span data-stu-id="386eb-643">96</span></span> |
| <span data-ttu-id="386eb-644">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-644">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-646">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-646">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-648">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-648">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-650">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-651">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-651">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-653">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-655">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-657">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-659">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-661">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-661">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-663">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-664">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-665">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-666">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-667">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-668">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-670">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-671">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-671">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-673">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-674">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-675">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-676">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-677">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-678">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-679">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-680">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-681">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-682">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-683">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-684">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-685">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-686">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-687">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-687">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-689">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-689">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-691">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-691">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="386eb-693">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-693">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-695">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-696">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-696">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-698">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-699">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-699">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-701">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-702">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-703">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-704">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-705">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="386eb-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>ПК</sup> нетипизированных типов (9)</span><span class="sxs-lookup"><span data-stu-id="386eb-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="386eb-707">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-707">Target</span></span> | <span data-ttu-id="386eb-708">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-708">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-709">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-710">64</span><span class="sxs-lookup"><span data-stu-id="386eb-710">64</span></span> |
| <span data-ttu-id="386eb-711">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-711">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-713">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-713">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-714">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-715">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-716">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-717">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-719">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-721">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-723">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-725">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-725">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-726">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-727">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-728">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-729">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-730">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-731">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-733">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-734">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-735">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-736">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-737">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-738">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-739">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-740">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-741">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-742">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-743">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-744">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-745">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-746">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-747">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-748">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-749">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-749">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-751">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-752">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-753">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-754">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-755">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-756">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-757">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-757">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-759">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-760">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-761">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-762">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-762">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-764">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="386eb-765">DXGI_FORMAT_R16G16B16A16 \_ с<sup></sup> плавающей запятой (10)</span><span class="sxs-lookup"><span data-stu-id="386eb-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="386eb-766">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-766">Target</span></span> | <span data-ttu-id="386eb-767">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-767">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-768">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-769">64</span><span class="sxs-lookup"><span data-stu-id="386eb-769">64</span></span> |
| <span data-ttu-id="386eb-770">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-770">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-772">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-772">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-774">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-774">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-776">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-777">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-778">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-780">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-782">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-784">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-786">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-786">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-788">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-788">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-790">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-791">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-792">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-793">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-794">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-796">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-796">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-798">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-798">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-800">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-800">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-802">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-803">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-804">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-805">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-806">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-807">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-808">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-809">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-810">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-811">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-812">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-813">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-814">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-815">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-815">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-817">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-817">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-819">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-819">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-821">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-821">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-823">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-823">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-825">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-825">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-827">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-827">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-829">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-829">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-831">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-832">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-832">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-834">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-834">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-836">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-836">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-838">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="386eb-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="386eb-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="386eb-840">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-840">Target</span></span> | <span data-ttu-id="386eb-841">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-841">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-842">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-843">64</span><span class="sxs-lookup"><span data-stu-id="386eb-843">64</span></span> |
| <span data-ttu-id="386eb-844">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-844">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-846">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-846">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-848">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-848">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-850">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-851">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-852">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-854">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-856">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-858">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-860">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-860">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-862">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-862">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-864">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-865">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-866">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-867">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-868">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-870">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-870">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-872">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-872">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-874">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-874">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-876">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-877">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-878">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-879">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-880">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-881">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-882">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-883">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-884">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-885">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-886">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-887">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-888">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-889">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-889">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-891">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-891">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-893">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-893">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-895">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-895">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-897">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-897">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-899">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-899">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-901">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-902">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-902">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-904">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-905">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-906">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-907">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-907">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-909">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="386eb-910">DXGI_FORMAT_R16G16B16A16ое \_ <sup>FCS</sup> /uint (12)</span><span class="sxs-lookup"><span data-stu-id="386eb-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="386eb-911">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-911">Target</span></span> | <span data-ttu-id="386eb-912">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-912">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-913">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-914">64</span><span class="sxs-lookup"><span data-stu-id="386eb-914">64</span></span> |
| <span data-ttu-id="386eb-915">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-915">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-917">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-917">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-919">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-919">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-921">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-922">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-923">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-925">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-927">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-929">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-931">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-931">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-933">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-934">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-935">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-936">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-937">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-938">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-940">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-941">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-941">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-943">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-944">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-944">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-946">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-947">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-948">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-949">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-950">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-951">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-952">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-953">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-954">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-955">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-956">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-957">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-958">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-958">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-960">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-960">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-962">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-962">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-964">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-964">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-966">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-967">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-967">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-969">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-970">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-970">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-972">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-973">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-974">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-975">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-975">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-977">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="386eb-978">DXGI_FORMAT_R16G16B16A16 \_ Снорм<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="386eb-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="386eb-979">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-979">Target</span></span> | <span data-ttu-id="386eb-980">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-980">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-981">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-982">64</span><span class="sxs-lookup"><span data-stu-id="386eb-982">64</span></span> |
| <span data-ttu-id="386eb-983">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-983">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-985">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-985">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-987">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-987">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-989">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-990">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-991">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-993">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-995">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-997">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-999">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-999">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1001">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1001">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1003">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1004">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1005">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1006">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1007">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1009">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1009">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1011">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1011">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1013">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1013">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1015">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1016">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1017">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1018">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1019">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1020">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1021">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1022">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1023">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1024">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1025">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1026">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1027">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1028">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1028">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1030">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1030">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1032">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1032">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1034">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1034">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1036">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1036">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1038">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1038">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1040">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1041">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1041">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1043">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1044">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1045">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1046">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1046">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1048">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="386eb-1049">DXGI_FORMAT_R16G16B16A16 \_ Синт-<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="386eb-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="386eb-1050">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1050">Target</span></span> | <span data-ttu-id="386eb-1051">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1052">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1053">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1053">64</span></span> |
| <span data-ttu-id="386eb-1054">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1054">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1056">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1056">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1058">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1058">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1060">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1061">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1062">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1064">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1066">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1068">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1070">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1070">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1072">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1073">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1074">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1075">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1076">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1077">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1077">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1079">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1080">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1080">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1082">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1083">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1084">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1085">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1086">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1087">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1088">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1089">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1090">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1091">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1092">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1093">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1094">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1095">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1096">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1096">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1098">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1098">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1100">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1100">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1102">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1102">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1104">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1105">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1105">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1107">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1108">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1108">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1110">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1111">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1112">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1113">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1113">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1115">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="386eb-1116">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32 (15)</span><span class="sxs-lookup"><span data-stu-id="386eb-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="386eb-1117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1117">Target</span></span> | <span data-ttu-id="386eb-1118">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1119">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1120">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1120">64</span></span> |
| <span data-ttu-id="386eb-1121">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1121">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1123">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1123">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1124">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1125">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1126">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1127">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1129">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1131">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1133">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1135">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1136">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1137">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1138">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1139">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1140">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1141">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1143">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1144">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1145">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1146">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1147">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1148">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1149">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1150">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1151">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1152">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1153">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1154">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1155">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1156">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1157">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1158">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1159">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1159">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1161">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1162">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1163">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1164">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1165">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1166">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1167">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1167">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1169">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1170">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1171">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1172">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1173">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="386eb-1174">DXGI_FORMAT_R32G32 \_ с<sup></sup> плавающей запятой (16)</span><span class="sxs-lookup"><span data-stu-id="386eb-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="386eb-1175">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1175">Target</span></span> | <span data-ttu-id="386eb-1176">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1177">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1178">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1178">64</span></span> |
| <span data-ttu-id="386eb-1179">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1179">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1181">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1181">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1183">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1183">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1185">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1186">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1186">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1188">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1190">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1192">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1194">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1196">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1196">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1198">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1198">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1200">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1201">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1202">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1203">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1204">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1206">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1206">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1208">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1208">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1210">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1210">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1212">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1213">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1214">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1215">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1216">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1217">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1218">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1219">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1220">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1221">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1222">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1223">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1224">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1225">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1225">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1227">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1227">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1229">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1229">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1231">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1231">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1233">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1233">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1235">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1235">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1237">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1238">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1238">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1240">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1241">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1242">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1243">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1244">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="386eb-1245">DXGI_FORMAT_R32G32 \_ с<sup>FCS</sup> /uint (17)</span><span class="sxs-lookup"><span data-stu-id="386eb-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="386eb-1246">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1246">Target</span></span> | <span data-ttu-id="386eb-1247">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1248">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1249">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1249">64</span></span> |
| <span data-ttu-id="386eb-1250">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1250">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1252">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1252">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1254">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1254">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1256">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1257">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1257">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1259">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1261">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1263">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1265">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1267">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1267">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1269">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1270">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1271">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1272">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1273">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1274">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1274">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1276">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1277">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1277">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1279">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1280">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1280">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1282">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1283">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1284">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1285">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1286">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1287">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1288">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1289">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1290">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1291">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1292">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1293">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1294">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1294">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1296">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1296">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1298">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1298">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1300">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1300">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1302">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1303">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1303">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1305">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1306">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1306">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1308">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1309">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1310">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1311">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1312">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="386eb-1313">DXGI_FORMAT_R32G32 \_ Синт-<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="386eb-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="386eb-1314">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1314">Target</span></span> | <span data-ttu-id="386eb-1315">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1316">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1317">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1317">64</span></span> |
| <span data-ttu-id="386eb-1318">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1318">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1320">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1320">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1322">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1322">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1324">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1325">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1325">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1327">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1329">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1331">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1333">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1335">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1335">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1337">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1338">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1339">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1340">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1341">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1342">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1342">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1344">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1345">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1345">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1347">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1348">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1349">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1350">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1351">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1352">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1353">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1354">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1355">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1356">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1357">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1358">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1359">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1360">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1361">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1361">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1363">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1363">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1365">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1365">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1367">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1367">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1369">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1370">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1370">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1372">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1373">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1373">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1375">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1376">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1377">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1378">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1379">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="386eb-1380">DXGI_FORMAT_R32G8X24 \_ <sup>ПК</sup> нетипизированного типа (19)</span><span class="sxs-lookup"><span data-stu-id="386eb-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="386eb-1381">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1381">Target</span></span> | <span data-ttu-id="386eb-1382">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1383">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1384">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1384">64</span></span> |
| <span data-ttu-id="386eb-1385">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1385">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1387">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1387">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1388">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1389">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1390">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1391">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1393">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1396">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1398">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1399">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1400">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1401">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1402">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1403">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1404">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1404">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1406">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1407">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1408">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1409">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1410">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1411">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1412">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1413">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1414">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1415">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1416">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1417">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1418">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1419">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1420">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1421">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1422">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1422">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1424">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1425">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1426">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1427">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1428">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1429">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1430">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1430">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1432">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1433">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1434">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1435">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1436">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="386eb-1437">DXGI_FORMAT_D32 с \_ плавающей запятой \_ S8X24 \_ uint (20)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="386eb-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="386eb-1438">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1438">Target</span></span> | <span data-ttu-id="386eb-1439">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1440">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1441">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1441">64</span></span> |
| <span data-ttu-id="386eb-1442">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1442">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1444">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1444">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1445">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1446">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1447">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1448">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1450">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1453">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1455">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1456">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1457">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1458">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1459">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1460">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1461">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1461">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1463">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1464">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1465">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1466">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1467">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1467">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1469">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1470">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1471">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1472">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1473">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1474">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1475">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1476">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1477">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1478">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1479">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1480">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1480">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1482">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1482">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1484">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1484">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1486">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1486">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1488">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1489">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1490">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1491">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1491">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1493">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1494">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1495">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1496">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1497">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="386eb-1498">\_Нетипизированный X8X24 с плавающей запятой \_ \_ (21)<sup></sup> DXGI_FORMAT_R32</span><span class="sxs-lookup"><span data-stu-id="386eb-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="386eb-1499">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1499">Target</span></span> | <span data-ttu-id="386eb-1500">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1501">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1502">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1502">64</span></span> |
| <span data-ttu-id="386eb-1503">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1503">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1505">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1505">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1506">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1507">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1508">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1509">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1511">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1514">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1516">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1516">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1518">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1518">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1520">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1520">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1522">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1523">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1523">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1525">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1526">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1526">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1528">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1529">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1530">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1531">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1532">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1533">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1534">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1535">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1536">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1537">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1538">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1539">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1540">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1541">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1542">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1543">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1544">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1544">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1546">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1547">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1548">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1549">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1550">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1550">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1552">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1553">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1553">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1555">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1556">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1557">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1558">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1559">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="386eb-1560">DXGI_FORMAT_X32 без \_ типов, \_ G8X24 \_ (22)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="386eb-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="386eb-1561">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1561">Target</span></span> | <span data-ttu-id="386eb-1562">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1563">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1564">64</span><span class="sxs-lookup"><span data-stu-id="386eb-1564">64</span></span> |
| <span data-ttu-id="386eb-1565">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1565">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1567">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1567">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1568">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1569">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1570">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1571">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1573">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1576">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1578">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1578">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1580">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1581">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1582">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1583">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1584">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1585">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1585">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1587">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1588">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1589">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1590">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1591">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1592">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1593">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1594">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1595">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1596">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1597">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1598">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1599">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1600">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1601">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1602">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1603">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1603">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1605">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1606">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1607">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1608">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1609">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1609">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1611">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1612">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1612">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1614">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1615">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1616">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1617">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1618">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="386eb-1619">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R10G10B10A2 (23)</span><span class="sxs-lookup"><span data-stu-id="386eb-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="386eb-1620">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1620">Target</span></span> | <span data-ttu-id="386eb-1621">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1622">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1623">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1623">32</span></span> |
| <span data-ttu-id="386eb-1624">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1624">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1626">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1626">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1627">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1628">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1629">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1630">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1632">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1634">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1636">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1638">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1639">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1640">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1641">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1642">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1643">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1644">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1644">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1646">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1647">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1648">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1649">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1650">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1651">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1652">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1653">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1654">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1655">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1656">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1657">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1658">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1659">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1660">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1661">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1662">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1662">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1664">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1665">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1666">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1667">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1668">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1669">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1670">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1670">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1672">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1673">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1674">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1675">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1675">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1677">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="386eb-1678">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="386eb-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="386eb-1679">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1679">Target</span></span> | <span data-ttu-id="386eb-1680">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1681">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1682">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1682">32</span></span> |
| <span data-ttu-id="386eb-1683">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1683">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1685">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1685">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1687">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1687">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1689">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1690">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1691">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1693">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1695">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1697">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1699">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1699">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1701">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1701">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1703">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1704">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1705">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1706">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1707">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1709">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1709">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1711">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1711">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1713">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1713">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1715">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1716">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1717">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1718">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1719">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1720">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1721">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1722">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1723">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1724">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1725">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1726">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1727">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1728">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1728">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1730">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1730">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1732">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1732">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1734">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1734">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1736">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1736">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1738">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1738">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1740">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1740">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1742">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1742">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1744">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1745">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1745">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1747">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1747">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1749">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1749">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1751">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="386eb-1752">DXGI_FORMAT_R10G10B10A2ое \_ <sup>FCS</sup> /uint (25)</span><span class="sxs-lookup"><span data-stu-id="386eb-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="386eb-1753">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1753">Target</span></span> | <span data-ttu-id="386eb-1754">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1755">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1756">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1756">32</span></span> |
| <span data-ttu-id="386eb-1757">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1757">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1759">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1759">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1761">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1761">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1763">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1764">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1765">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1767">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1769">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1771">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1773">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1773">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1775">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1776">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1777">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1778">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1779">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1780">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1782">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1783">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1783">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1785">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1786">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1786">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1788">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1789">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1790">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1791">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1792">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1793">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1794">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1795">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1796">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1797">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1798">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1799">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1800">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1800">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1802">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1802">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1804">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1804">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1806">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1806">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1808">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1809">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1809">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1811">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1812">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1812">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1814">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1815">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1816">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1817">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1817">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1819">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="386eb-1820">DXGI_FORMAT_R10G10B10 \_ XR \_ смещение \_ A2 \_ UNORM<sup></sup> (89)</span><span class="sxs-lookup"><span data-stu-id="386eb-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="386eb-1821">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1821">Target</span></span> | <span data-ttu-id="386eb-1822">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1823">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1824">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1824">32</span></span> |
| <span data-ttu-id="386eb-1825">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1825">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1827">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1827">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1828">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1829">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1830">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1832">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-1836">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1837">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1838">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1839">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1840">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1841">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-1843">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1844">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1845">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1846">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1847">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1848">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1849">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1850">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1851">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1852">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1853">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1854">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1855">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1856">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1857">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1858">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1859">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1859">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1861">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1862">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1863">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1864">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1865">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1866">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1866">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1868">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1868">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1870">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1871">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1871">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1873">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1873">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1875">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1875">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1877">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="386eb-1878">DXGI_FORMAT_R11G11B10 \_ <sup>ФНС</sup> с плавающей запятой (26)</span><span class="sxs-lookup"><span data-stu-id="386eb-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="386eb-1879">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1879">Target</span></span> | <span data-ttu-id="386eb-1880">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1881">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1882">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1882">32</span></span> |
| <span data-ttu-id="386eb-1883">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1883">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1885">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1885">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1887">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1887">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1889">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1890">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1891">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1893">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1895">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1897">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1899">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1899">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1901">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1901">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1903">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1904">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1905">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1906">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1907">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1909">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1909">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1911">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1911">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1913">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1913">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1915">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1916">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1917">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1918">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1919">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1920">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1921">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1922">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1923">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1924">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1925">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1926">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1927">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1928">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1928">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1930">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1930">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1932">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1932">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1934">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1934">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-1936">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1936">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1938">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1938">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1940">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1941">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-1942">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-1943">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-1944">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-1945">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-1946">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="386eb-1947">DXGI_FORMAT_R8G8B8A8 \_ <sup>ПК</sup> нетипизированных типов (27)</span><span class="sxs-lookup"><span data-stu-id="386eb-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="386eb-1948">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-1948">Target</span></span> | <span data-ttu-id="386eb-1949">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-1950">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-1951">32</span><span class="sxs-lookup"><span data-stu-id="386eb-1951">32</span></span> |
| <span data-ttu-id="386eb-1952">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-1952">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1954">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-1954">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1955">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1956">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1957">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-1958">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-1960">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-1962">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-1964">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1966">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-1967">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-1968">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-1969">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-1970">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-1971">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-1972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1972">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1974">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-1975">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1976">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1977">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-1978">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-1979">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1980">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-1981">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-1982">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-1983">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-1984">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-1985">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-1986">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-1987">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-1988">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1989">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-1990">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-1990">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-1992">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1993">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-1994">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-1995">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-1996">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-1997">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-1998">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-1998">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2000">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2001">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2002">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2003">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2003">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2005">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="386eb-2006">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="386eb-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="386eb-2007">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2007">Target</span></span> | <span data-ttu-id="386eb-2008">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2009">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2010">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2010">32</span></span> |
| <span data-ttu-id="386eb-2011">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2011">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2013">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2013">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2015">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2015">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2017">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2018">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2019">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2021">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2023">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2025">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2027">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2027">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2029">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2029">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2031">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2032">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2033">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2034">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2035">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2037">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2037">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2039">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2039">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2041">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2041">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2043">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2044">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2045">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2046">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2047">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2048">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2049">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2050">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2051">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2052">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2053">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2054">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2055">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2056">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2056">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2058">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2058">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2060">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2060">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2062">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2062">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2064">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2064">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2066">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2066">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2068">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2068">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2070">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2070">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2072">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2073">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2073">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2075">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2075">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2077">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2077">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2079">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="386eb-2080">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="386eb-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="386eb-2081">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2081">Target</span></span> | <span data-ttu-id="386eb-2082">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2083">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2084">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2084">32</span></span> |
| <span data-ttu-id="386eb-2085">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2085">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2087">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2087">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2088">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2089">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2090">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2091">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2093">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2095">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2097">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2099">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2099">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2101">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2101">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2103">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2104">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2105">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2106">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2107">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2107">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2109">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2109">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2111">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2111">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2113">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2113">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2115">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2116">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2117">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2118">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2119">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2120">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2121">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2122">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2123">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2124">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2125">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2126">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2127">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2128">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2128">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2130">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2130">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2132">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2132">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2134">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2134">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2136">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2136">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2138">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2138">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2140">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2140">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2142">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2142">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2144">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2145">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2145">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2147">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2147">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2149">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2149">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2151">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="386eb-2152">DXGI_FORMAT_R8G8B8A8ое \_ <sup>FCS</sup> /uint (30)</span><span class="sxs-lookup"><span data-stu-id="386eb-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="386eb-2153">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2153">Target</span></span> | <span data-ttu-id="386eb-2154">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2155">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2156">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2156">32</span></span> |
| <span data-ttu-id="386eb-2157">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2157">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2159">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2159">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2161">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2161">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2163">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2164">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2165">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2167">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2169">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2171">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2173">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2173">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2175">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2176">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2177">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2178">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2179">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2180">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2180">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2182">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2183">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2183">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2185">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2186">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2186">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2188">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2189">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2190">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2191">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2192">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2193">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2194">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2195">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2196">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2197">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2198">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2199">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2200">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2200">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2202">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2202">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2204">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2204">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2206">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2206">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2208">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2209">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2209">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2211">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2212">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2212">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2214">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2215">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2216">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2217">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2217">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2219">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="386eb-2220">DXGI_FORMAT_R8G8B8A8 \_ снормного<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="386eb-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="386eb-2221">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2221">Target</span></span> | <span data-ttu-id="386eb-2222">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2223">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2224">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2224">32</span></span> |
| <span data-ttu-id="386eb-2225">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2225">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2227">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2227">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2229">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2229">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2231">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2232">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2233">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2235">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2237">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2239">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2241">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2241">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2243">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2243">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2245">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2246">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2247">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2248">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2249">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2251">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2251">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2253">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2253">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2255">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2255">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2257">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2258">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2259">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2260">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2261">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2262">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2263">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2264">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2265">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2266">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2267">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2268">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2269">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2270">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2270">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2272">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2272">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2274">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2274">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2276">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2276">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2278">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2278">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2280">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2280">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2282">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2283">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2283">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2285">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2286">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2287">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2288">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2288">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2290">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="386eb-2291">DXGI_FORMAT_R8G8B8A8 \_ Синт-<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="386eb-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="386eb-2292">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2292">Target</span></span> | <span data-ttu-id="386eb-2293">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2294">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2295">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2295">32</span></span> |
| <span data-ttu-id="386eb-2296">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2296">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2298">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2298">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2300">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2300">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2302">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2303">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2304">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2306">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2308">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2310">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2312">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2312">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2314">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2315">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2316">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2317">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2318">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2319">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2321">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2322">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2322">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2324">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2325">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2326">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2327">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2328">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2329">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2330">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2331">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2332">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2333">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2334">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2335">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2336">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2337">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2338">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2338">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2340">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2340">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2342">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2342">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2344">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2344">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2346">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2347">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2347">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2349">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2350">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2350">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2352">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2353">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2354">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2355">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2355">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2357">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="386eb-2358">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16G16 (33)</span><span class="sxs-lookup"><span data-stu-id="386eb-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="386eb-2359">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2359">Target</span></span> | <span data-ttu-id="386eb-2360">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2361">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2362">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2362">32</span></span> |
| <span data-ttu-id="386eb-2363">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2363">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2365">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2365">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2366">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2367">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2368">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2369">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2371">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2373">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2375">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2377">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-2378">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2379">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2380">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2381">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2382">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2383">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2383">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2385">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2386">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2387">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2388">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2389">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2390">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2391">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2392">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2393">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2394">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2395">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2396">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2397">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2398">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2399">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2400">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2401">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2401">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2403">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2404">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2405">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-2406">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2407">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-2408">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2409">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2409">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2411">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2412">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2413">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2414">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2415">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="386eb-2416">DXGI_FORMAT_R16G16 \_ с<sup></sup> плавающей запятой (34)</span><span class="sxs-lookup"><span data-stu-id="386eb-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="386eb-2417">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2417">Target</span></span> | <span data-ttu-id="386eb-2418">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2419">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2420">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2420">32</span></span> |
| <span data-ttu-id="386eb-2421">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2421">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2423">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2423">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2425">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2425">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2427">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2428">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2429">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2431">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2433">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2435">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2437">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2437">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2439">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2439">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2441">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2442">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2443">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2444">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2445">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2447">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2447">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2449">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2449">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2451">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2451">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2453">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2454">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2455">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2456">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2457">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2458">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2459">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2460">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2461">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2462">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2463">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2464">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2465">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2466">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2466">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2468">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2468">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2470">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2470">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2472">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2472">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2474">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2474">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2476">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2476">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2478">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2479">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2479">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2481">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2482">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2483">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2484">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2485">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="386eb-2486">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="386eb-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="386eb-2487">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2487">Target</span></span> | <span data-ttu-id="386eb-2488">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2489">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2490">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2490">32</span></span> |
| <span data-ttu-id="386eb-2491">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2491">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2493">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2493">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2495">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2495">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2497">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2498">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2499">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2501">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2503">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2505">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2507">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2507">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2509">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2509">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2511">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2512">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2513">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2514">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2515">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2517">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2517">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2519">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2519">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2521">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2521">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2523">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2524">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2525">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2526">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2527">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2528">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2529">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2530">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2531">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2532">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2533">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2534">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2535">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2536">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2536">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2538">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2538">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2540">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2540">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2542">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2542">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2544">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2544">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2546">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2546">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2548">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2549">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2549">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2551">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2552">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2553">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2554">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2555">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="386eb-2556">DXGI_FORMAT_R16G16ое \_ <sup>FCS</sup> /uint (36)</span><span class="sxs-lookup"><span data-stu-id="386eb-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="386eb-2557">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2557">Target</span></span> | <span data-ttu-id="386eb-2558">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2559">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2560">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2560">32</span></span> |
| <span data-ttu-id="386eb-2561">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2561">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2563">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2563">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2565">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2565">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2567">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2568">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2569">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2571">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2573">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2575">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2577">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2577">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2579">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2580">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2581">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2582">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2583">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2584">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2584">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2586">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2587">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2587">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2589">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2590">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2590">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2592">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2593">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2594">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2595">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2596">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2597">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2598">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2599">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2600">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2601">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2602">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2603">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2604">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2604">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2606">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2606">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2608">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2608">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2610">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2610">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2612">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2613">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2613">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2615">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2616">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2616">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2618">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2619">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2620">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2621">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2622">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="386eb-2623">DXGI_FORMAT_R16G16 \_ Снорм<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="386eb-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="386eb-2624">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2624">Target</span></span> | <span data-ttu-id="386eb-2625">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2626">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2627">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2627">32</span></span> |
| <span data-ttu-id="386eb-2628">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2628">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2630">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2630">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2632">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2632">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2634">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2635">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2636">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2638">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2640">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2642">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2644">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2644">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2646">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2646">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2648">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2649">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2650">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2651">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2652">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2654">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2654">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2656">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2656">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2658">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2658">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2660">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2661">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2662">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2663">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2664">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2665">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2666">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2667">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2668">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2669">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2670">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2671">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2672">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2673">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2673">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2675">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2675">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2677">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2677">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2679">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2679">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2681">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2681">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2683">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2683">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2685">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2686">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2686">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2688">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2689">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2690">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2691">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2692">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="386eb-2693">DXGI_FORMAT_R16G16 \_ Синт-<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="386eb-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="386eb-2694">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2694">Target</span></span> | <span data-ttu-id="386eb-2695">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2696">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2697">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2697">32</span></span> |
| <span data-ttu-id="386eb-2698">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2698">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2700">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2700">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2702">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2702">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2704">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2705">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2706">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2708">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2710">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2712">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2714">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2714">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2716">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2717">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2718">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2719">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2720">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2721">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2723">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2724">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2724">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2726">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2727">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2728">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2729">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2730">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2731">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2732">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2733">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2734">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2735">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2736">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2737">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2738">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2739">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2740">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2740">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2742">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2742">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2744">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2744">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2746">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2746">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2748">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2749">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2749">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2751">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2752">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2752">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2754">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2755">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2756">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2757">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-2758">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="386eb-2759">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32 (39)</span><span class="sxs-lookup"><span data-stu-id="386eb-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="386eb-2760">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2760">Target</span></span> | <span data-ttu-id="386eb-2761">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2762">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2763">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2763">32</span></span> |
| <span data-ttu-id="386eb-2764">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2764">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2766">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2766">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2767">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2768">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2769">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2770">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2772">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2774">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2776">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2778">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-2779">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2780">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2781">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2782">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2783">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2784">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2784">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2786">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2787">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2788">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2789">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2790">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2791">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2792">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2793">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2794">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2795">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2796">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2797">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2798">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2799">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2800">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2801">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2802">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2802">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2804">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2805">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2806">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-2807">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2808">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-2809">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2810">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2810">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2812">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2813">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2814">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2815">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2815">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2817">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="386eb-2818">DXGI_FORMAT_D32 \_ с<sup></sup> плавающей запятой (40)</span><span class="sxs-lookup"><span data-stu-id="386eb-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="386eb-2819">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2819">Target</span></span> | <span data-ttu-id="386eb-2820">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2821">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2822">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2822">32</span></span> |
| <span data-ttu-id="386eb-2823">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2823">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2825">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2825">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2826">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2827">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2828">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2829">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2831">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2834">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2836">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-2837">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2838">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2839">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2840">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2841">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2842">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2844">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2845">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2846">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2847">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2848">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2848">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2850">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2851">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2852">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2853">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2854">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2855">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2856">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2857">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2858">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2859">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2860">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2861">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2861">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2863">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2863">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2865">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2865">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2867">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2867">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2869">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-2870">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-2871">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2872">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2872">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2874">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2875">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2876">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2877">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2877">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2879">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="386eb-2880">DXGI_FORMAT_R32 \_ с<sup></sup> плавающей запятой (41)</span><span class="sxs-lookup"><span data-stu-id="386eb-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="386eb-2881">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2881">Target</span></span> | <span data-ttu-id="386eb-2882">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2883">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2884">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2884">32</span></span> |
| <span data-ttu-id="386eb-2885">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2885">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2887">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2887">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2889">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2889">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2891">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-2892">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2892">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2894">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2896">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2898">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2900">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2902">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2902">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2904">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2904">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2906">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2906">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2908">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2909">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2909">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2911">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2912">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2914">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2914">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2916">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2916">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2918">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2918">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2920">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-2921">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2922">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2923">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2924">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2925">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2926">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2927">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2928">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-2929">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-2930">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-2931">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2932">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-2933">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-2933">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2935">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2935">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2937">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2937">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2939">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-2939">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2941">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-2941">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2943">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-2943">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2945">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-2946">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-2946">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2948">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-2949">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-2950">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-2951">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2951">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2953">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="386eb-2954">DXGI_FORMAT_R32ое \_ <sup>FCS</sup> /uint (42)</span><span class="sxs-lookup"><span data-stu-id="386eb-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="386eb-2955">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-2955">Target</span></span> | <span data-ttu-id="386eb-2956">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-2957">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-2958">32</span><span class="sxs-lookup"><span data-stu-id="386eb-2958">32</span></span> |
| <span data-ttu-id="386eb-2959">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-2959">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2961">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-2961">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2963">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2963">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2965">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-2965">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2967">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-2967">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-2969">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-2971">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-2973">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-2975">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2977">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-2977">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2979">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-2980">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-2981">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-2982">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-2983">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-2984">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2984">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2986">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-2987">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-2987">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-2989">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-2990">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-2990">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-2992">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-2993">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2994">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-2995">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-2996">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-2997">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-2998">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-2999">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3000">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3001">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3002">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3003">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3004">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3004">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3006">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3006">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3008">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3008">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3010">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3010">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3012">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3013">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3013">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3015">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3016">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3016">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3018">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3019">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3020">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3021">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3021">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3023">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="386eb-3024">DXGI_FORMAT_R32 \_ Синт-<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="386eb-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="386eb-3025">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3025">Target</span></span> | <span data-ttu-id="386eb-3026">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3027">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3028">32</span><span class="sxs-lookup"><span data-stu-id="386eb-3028">32</span></span> |
| <span data-ttu-id="386eb-3029">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3029">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3031">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3031">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3033">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3033">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3035">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3036">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3036">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3038">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3040">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3042">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3044">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3046">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3046">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3048">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3049">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3050">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3051">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3052">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3053">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3055">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3056">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3056">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3058">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3059">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3060">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3061">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3062">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3063">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3064">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3065">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3066">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3067">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3068">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3069">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3070">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3071">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3072">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3072">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3074">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3074">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3076">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3076">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3078">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3078">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3080">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3081">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3081">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3083">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3084">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3084">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3086">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3087">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3088">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3089">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3089">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3091">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="386eb-3092">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R24G8 (44)</span><span class="sxs-lookup"><span data-stu-id="386eb-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="386eb-3093">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3093">Target</span></span> | <span data-ttu-id="386eb-3094">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3095">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3096">32</span><span class="sxs-lookup"><span data-stu-id="386eb-3096">32</span></span> |
| <span data-ttu-id="386eb-3097">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3097">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3099">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3099">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3100">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3101">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3102">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3103">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3105">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3108">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3110">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-3111">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3112">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3113">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3114">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3115">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3116">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3116">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3118">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3119">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3120">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3121">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3122">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3123">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3124">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3125">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3126">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3127">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3128">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3129">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3130">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3131">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3132">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3133">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3134">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3134">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3136">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3137">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3138">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-3139">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3140">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-3141">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3142">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3142">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3144">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3145">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3146">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3147">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3148">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="386eb-3149">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="386eb-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="386eb-3150">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3150">Target</span></span> | <span data-ttu-id="386eb-3151">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3152">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3153">32</span><span class="sxs-lookup"><span data-stu-id="386eb-3153">32</span></span> |
| <span data-ttu-id="386eb-3154">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3154">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3156">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3156">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3157">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3158">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3159">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3160">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3162">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3165">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3167">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-3168">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3169">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3170">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3171">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3172">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3173">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3175">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3176">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3177">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3178">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3179">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3179">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3181">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3182">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3183">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3184">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3185">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3186">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3187">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3188">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3189">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3190">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3191">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3192">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3192">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3194">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3194">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3196">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3196">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3198">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3198">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3200">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3201">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-3202">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3203">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3203">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3205">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3206">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3207">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3208">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3209">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="386eb-3210">DXGI_FORMAT_R24 \_ UNORM \_ x8 с \_ нетипизированным типом (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="386eb-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="386eb-3211">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3211">Target</span></span> | <span data-ttu-id="386eb-3212">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3213">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3214">32</span><span class="sxs-lookup"><span data-stu-id="386eb-3214">32</span></span> |
| <span data-ttu-id="386eb-3215">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3215">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3217">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3217">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3218">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3219">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3220">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3221">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3223">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3226">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3228">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3228">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3230">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3230">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3232">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3232">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3234">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3235">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3235">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3237">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3238">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3238">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3240">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3241">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3242">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3243">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3244">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3245">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3246">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3247">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3248">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3249">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3250">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3251">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3252">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3253">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3254">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3255">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3256">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3256">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3258">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3259">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3260">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-3261">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3262">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3262">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3264">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3265">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3265">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3267">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3268">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3269">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3270">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3271">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="386eb-3272">DXGI_FORMAT_X24 \_ нетипизированного \_ G8ого типа \_ uint (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="386eb-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="386eb-3273">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3273">Target</span></span> | <span data-ttu-id="386eb-3274">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3275">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3276">32</span><span class="sxs-lookup"><span data-stu-id="386eb-3276">32</span></span> |
| <span data-ttu-id="386eb-3277">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3277">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3279">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3279">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3280">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3281">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3282">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3283">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3285">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3288">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3290">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3290">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3292">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3293">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3294">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3295">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3296">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3297">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3299">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3300">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3301">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3302">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3303">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3304">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3305">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3306">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3307">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3308">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3309">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3310">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3311">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3312">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3313">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3314">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3315">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3315">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3317">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3318">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3319">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-3320">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3321">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3321">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3323">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3324">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3324">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3326">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3327">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3328">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3329">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3330">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="386eb-3331">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8G8 (48)</span><span class="sxs-lookup"><span data-stu-id="386eb-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="386eb-3332">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3332">Target</span></span> | <span data-ttu-id="386eb-3333">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3334">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3335">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3335">16</span></span> |
| <span data-ttu-id="386eb-3336">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3336">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3338">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3338">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3339">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3340">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3341">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3342">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3344">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3346">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3348">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3350">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-3351">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3352">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3353">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3354">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3355">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3356">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3356">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3358">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3359">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3360">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3361">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3362">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3363">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3364">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3365">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3366">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3367">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3368">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3369">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3370">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3371">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3372">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3373">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3374">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3374">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3376">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3377">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3378">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-3379">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3380">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-3381">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3382">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3382">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3384">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3385">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3386">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3387">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3388">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="386eb-3389">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="386eb-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="386eb-3390">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3390">Target</span></span> | <span data-ttu-id="386eb-3391">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3392">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3393">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3393">16</span></span> |
| <span data-ttu-id="386eb-3394">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3394">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3396">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3396">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3398">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3398">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3400">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3401">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3402">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3404">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3406">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3408">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3410">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3410">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3412">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3412">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3414">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3415">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3416">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3417">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3418">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3420">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3420">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3422">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3422">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3424">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3424">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3426">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3427">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3428">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3429">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3430">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3431">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3432">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3433">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3434">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3435">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3436">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3437">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3438">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3439">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3439">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3441">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3441">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3443">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3443">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3445">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3445">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3447">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3447">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3449">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3449">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3451">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3452">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3452">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3454">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3455">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3456">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3457">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3457">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3459">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="386eb-3460">DXGI_FORMAT_R8G8ое \_ <sup>FCS</sup> /uint (50)</span><span class="sxs-lookup"><span data-stu-id="386eb-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="386eb-3461">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3461">Target</span></span> | <span data-ttu-id="386eb-3462">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3463">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3464">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3464">16</span></span> |
| <span data-ttu-id="386eb-3465">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3465">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3467">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3467">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3469">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3469">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3471">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3472">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3473">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3475">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3477">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3479">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3481">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3481">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3483">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3484">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3485">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3486">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3487">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3488">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3490">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3491">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3491">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3493">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3494">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3494">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3496">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3497">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3498">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3499">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3500">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3501">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3502">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3503">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3504">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3505">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3506">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3507">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3508">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3508">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3510">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3510">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3512">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3512">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3514">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3514">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3516">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3517">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3517">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3519">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3520">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3520">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3522">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3523">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3524">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3525">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3526">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="386eb-3527">DXGI_FORMAT_R8G8 \_ Снорм<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="386eb-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="386eb-3528">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3528">Target</span></span> | <span data-ttu-id="386eb-3529">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3530">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3531">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3531">16</span></span> |
| <span data-ttu-id="386eb-3532">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3532">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3534">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3534">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3536">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3536">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3538">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3539">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3540">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3542">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3544">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3546">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3548">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3548">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3550">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3550">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3552">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3553">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3554">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3555">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3556">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3558">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3558">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3560">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3560">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3562">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3562">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3564">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3565">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3566">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3567">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3568">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3569">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3570">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3571">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3572">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3573">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3574">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3575">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3576">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3577">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3577">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3579">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3579">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3581">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3581">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3583">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3583">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3585">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3585">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3587">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3587">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3589">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3590">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3590">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3592">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3593">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3594">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3595">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3596">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="386eb-3597">DXGI_FORMAT_R8G8 \_ Синт-<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="386eb-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="386eb-3598">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3598">Target</span></span> | <span data-ttu-id="386eb-3599">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3600">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3601">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3601">16</span></span> |
| <span data-ttu-id="386eb-3602">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3602">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3604">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3604">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3606">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3606">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3608">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3609">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3610">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3612">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3614">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3616">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3618">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3618">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3620">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3621">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3622">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3623">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3624">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3625">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3625">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3627">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3628">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3628">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3630">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3631">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3632">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3633">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3634">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3635">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3636">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3637">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3638">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3639">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3640">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3641">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3642">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3643">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3644">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3644">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3646">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3646">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3648">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3648">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3650">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3650">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3652">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3653">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3653">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3655">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3656">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3656">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3658">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3659">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3660">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3661">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-3662">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="386eb-3663">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16 (53)</span><span class="sxs-lookup"><span data-stu-id="386eb-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="386eb-3664">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3664">Target</span></span> | <span data-ttu-id="386eb-3665">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3666">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3667">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3667">16</span></span> |
| <span data-ttu-id="386eb-3668">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3668">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3670">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3670">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3671">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3672">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3673">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3674">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3676">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3678">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3680">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3682">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-3683">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3684">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3685">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3686">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3687">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3688">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3690">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3691">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3692">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3693">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3694">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3695">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3696">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3697">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3698">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3699">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3700">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3701">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3702">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3703">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3704">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3705">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3706">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3706">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3708">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3709">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3710">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-3711">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3712">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-3713">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3714">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3714">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3716">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3717">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3718">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3719">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3719">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3721">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="386eb-3722">DXGI_FORMAT_R16 \_ с<sup></sup> плавающей запятой (54)</span><span class="sxs-lookup"><span data-stu-id="386eb-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="386eb-3723">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3723">Target</span></span> | <span data-ttu-id="386eb-3724">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3725">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3726">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3726">16</span></span> |
| <span data-ttu-id="386eb-3727">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3727">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3729">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3729">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3731">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3731">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3733">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3734">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3735">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3737">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3739">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3741">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3743">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3743">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3745">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3745">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3747">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3748">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3749">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3749">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3751">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3752">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3754">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3754">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3756">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3756">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3758">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3758">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3760">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3761">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3762">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3763">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3764">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3765">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3766">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3767">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3768">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3769">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3770">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3771">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3772">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3773">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3773">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3775">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3775">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3777">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3777">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3779">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3779">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3781">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3781">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3783">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3783">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3785">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3786">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3786">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3788">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3789">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3790">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3791">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3791">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3793">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="386eb-3794">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="386eb-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="386eb-3795">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3795">Target</span></span> | <span data-ttu-id="386eb-3796">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3797">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3798">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3798">16</span></span> |
| <span data-ttu-id="386eb-3799">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3799">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3801">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3801">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3802">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3803">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3804">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3805">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3807">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3810">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3812">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-3813">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3814">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3815">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3816">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3817">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3818">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3818">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3820">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3821">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3822">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3823">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3824">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3824">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3826">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3827">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3828">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3829">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3830">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3831">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3832">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3833">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3834">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3835">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3836">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3837">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3837">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3839">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3839">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3841">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3841">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3843">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3843">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3845">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3846">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-3847">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3848">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3848">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3850">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3851">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3852">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3853">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3853">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3855">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="386eb-3856">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="386eb-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="386eb-3857">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3857">Target</span></span> | <span data-ttu-id="386eb-3858">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3859">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3860">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3860">16</span></span> |
| <span data-ttu-id="386eb-3861">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3861">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3863">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3863">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3865">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3865">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3867">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3868">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3869">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3871">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3873">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3875">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3877">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3877">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3879">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3879">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3881">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3881">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3883">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3884">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3884">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3886">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3887">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3887">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3889">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3889">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3891">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3891">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3893">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3893">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3895">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-3896">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3897">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3898">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3899">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3900">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3901">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3902">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3903">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3904">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3905">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3906">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3907">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3908">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3908">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3910">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3910">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3912">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3912">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3914">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3914">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3916">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3916">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3918">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3918">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3920">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3921">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3921">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3923">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3924">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3925">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3926">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3926">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3928">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="386eb-3929">DXGI_FORMAT_R16ое \_ <sup>FCS</sup> /uint (57)</span><span class="sxs-lookup"><span data-stu-id="386eb-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="386eb-3930">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3930">Target</span></span> | <span data-ttu-id="386eb-3931">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-3932">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-3933">16</span><span class="sxs-lookup"><span data-stu-id="386eb-3933">16</span></span> |
| <span data-ttu-id="386eb-3934">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-3934">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3936">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-3936">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3938">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3938">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3940">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-3940">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3942">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-3943">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-3945">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-3947">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-3949">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3951">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-3951">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3953">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-3954">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-3955">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-3956">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-3957">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-3958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3958">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3960">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-3961">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3961">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3963">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-3964">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-3964">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3966">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-3967">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3968">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-3969">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-3970">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-3971">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-3972">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-3973">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-3974">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-3975">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-3976">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3977">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-3978">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-3978">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3980">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3980">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3982">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-3982">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3984">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-3984">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-3986">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-3987">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-3987">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3989">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-3990">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-3990">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3992">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-3993">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-3994">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-3995">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3995">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-3997">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="386eb-3998">DXGI_FORMAT_R16 \_ Снорм<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="386eb-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="386eb-3999">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-3999">Target</span></span> | <span data-ttu-id="386eb-4000">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4001">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4002">16</span><span class="sxs-lookup"><span data-stu-id="386eb-4002">16</span></span> |
| <span data-ttu-id="386eb-4003">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4003">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4005">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4005">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4007">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4007">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4009">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4010">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4011">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4013">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4015">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4017">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4019">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4019">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4021">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4021">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4023">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4024">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4025">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4025">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4027">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4028">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4030">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4030">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4032">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4032">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4034">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4034">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4036">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4037">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4038">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4039">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4040">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4041">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4042">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4043">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4044">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4045">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4046">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4047">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4048">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4049">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4049">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4051">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4051">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4053">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4053">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4055">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4055">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4057">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4057">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4059">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4059">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4061">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4062">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4062">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4064">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4065">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4066">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4067">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4067">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4069">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="386eb-4070">DXGI_FORMAT_R16 \_ Синт-<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="386eb-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="386eb-4071">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4071">Target</span></span> | <span data-ttu-id="386eb-4072">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4073">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4074">16</span><span class="sxs-lookup"><span data-stu-id="386eb-4074">16</span></span> |
| <span data-ttu-id="386eb-4075">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4075">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4077">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4077">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4079">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4079">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4081">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4082">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4083">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4085">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4087">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4089">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4091">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4091">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4093">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4094">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4095">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4096">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4097">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4098">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4098">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4100">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4101">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4101">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4103">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4104">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4105">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4106">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4107">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4108">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4109">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4110">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4111">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4112">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4113">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4114">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4115">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4116">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4117">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4117">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4119">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4119">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4121">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4121">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4123">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4123">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4125">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4126">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4126">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4128">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4129">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4129">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4131">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4132">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4133">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4134">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4134">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4136">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="386eb-4137">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8 (60)</span><span class="sxs-lookup"><span data-stu-id="386eb-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="386eb-4138">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4138">Target</span></span> | <span data-ttu-id="386eb-4139">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4140">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4141">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4141">8</span></span> |
| <span data-ttu-id="386eb-4142">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4142">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4144">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4144">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4145">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4146">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4147">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4148">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4150">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4152">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4154">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4156">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-4157">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4158">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4159">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4160">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4161">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4162">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4162">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4164">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4165">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4166">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4167">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4168">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4169">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4170">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4171">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4172">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4173">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4174">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4175">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4176">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4177">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4178">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4179">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4180">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4180">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4182">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4183">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4184">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4185">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4186">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4187">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4188">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4188">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4190">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4191">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4192">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4193">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4193">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4195">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="386eb-4196">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="386eb-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="386eb-4197">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4197">Target</span></span> | <span data-ttu-id="386eb-4198">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4199">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4200">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4200">8</span></span> |
| <span data-ttu-id="386eb-4201">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4201">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4203">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4203">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4205">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4205">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4207">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4208">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4209">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4211">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4213">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4215">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4217">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4217">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4219">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4219">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4221">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4222">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4223">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4223">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4225">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4226">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4228">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4228">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4230">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4230">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4232">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4232">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4234">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4235">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4236">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4237">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4238">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4239">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4240">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4241">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4242">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4243">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4244">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4245">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4246">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4247">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4247">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4249">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4249">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4251">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4251">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4253">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4253">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4255">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4255">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4257">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4257">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4259">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4260">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4260">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4262">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4263">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4264">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4265">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4265">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4267">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="386eb-4268">DXGI_FORMAT_R8ое \_ <sup>FCS</sup> /uint (62)</span><span class="sxs-lookup"><span data-stu-id="386eb-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="386eb-4269">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4269">Target</span></span> | <span data-ttu-id="386eb-4270">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4271">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4272">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4272">8</span></span> |
| <span data-ttu-id="386eb-4273">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4273">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4275">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4275">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4277">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4277">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4279">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4280">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4281">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4283">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4285">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4287">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4289">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4289">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4291">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4292">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4293">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4294">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4295">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4296">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4298">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4299">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4299">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4301">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4302">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4302">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4304">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4305">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4306">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4307">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4308">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4309">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4310">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4311">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4312">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4313">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4314">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4315">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4316">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4316">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4318">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4318">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4320">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4320">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4322">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4322">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4324">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4325">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4325">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4327">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4328">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4328">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4330">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4331">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4332">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4333">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4333">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4335">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="386eb-4336">DXGI_FORMAT_R8 \_ Снорм<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="386eb-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="386eb-4337">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4337">Target</span></span> | <span data-ttu-id="386eb-4338">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4339">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4340">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4340">8</span></span> |
| <span data-ttu-id="386eb-4341">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4341">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4343">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4343">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4345">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4345">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4347">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4348">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4349">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4351">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4353">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4355">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4357">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4357">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4359">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4359">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4361">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4362">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4363">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4363">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4365">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4366">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4366">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4368">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4368">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4370">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4370">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4372">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4372">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4374">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4375">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4376">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4377">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4378">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4379">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4380">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4381">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4382">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4383">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4384">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4385">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4386">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4387">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4387">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4389">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4389">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4391">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4391">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4393">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4393">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4395">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4395">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4397">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4397">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4399">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4400">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4400">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4402">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4403">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4404">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4405">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4405">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4407">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="386eb-4408">DXGI_FORMAT_R8 \_ Синт-<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="386eb-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="386eb-4409">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4409">Target</span></span> | <span data-ttu-id="386eb-4410">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4411">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4412">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4412">8</span></span> |
| <span data-ttu-id="386eb-4413">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4413">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4415">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4415">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4417">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4417">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4419">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4420">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4421">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4423">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4425">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4427">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4429">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4429">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4431">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4432">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4433">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4434">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4435">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4436">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4438">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4439">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4439">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4441">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4442">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4443">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4444">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4445">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4446">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4447">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4448">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4449">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4450">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4451">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4452">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4453">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4454">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4455">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4455">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4457">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4457">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4459">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4459">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4461">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4461">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4463">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4464">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4464">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4466">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4467">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4467">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4469">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4470">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4471">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4472">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4472">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4474">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="386eb-4475">DXGI_FORMAT_A8 \_ UNORM<sup>фнс</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="386eb-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="386eb-4476">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4476">Target</span></span> | <span data-ttu-id="386eb-4477">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4478">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4479">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4479">8</span></span> |
| <span data-ttu-id="386eb-4480">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4480">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4482">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4482">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4483">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4484">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4485">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4486">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4488">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4490">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4492">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4494">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4494">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4496">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4496">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4498">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4499">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4500">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4501">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4502">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4502">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4504">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4504">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4506">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4506">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4508">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4508">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4510">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4511">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4512">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4513">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4514">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4515">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4516">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4517">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4518">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4519">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4520">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4521">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4522">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4523">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4523">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4525">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4525">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4527">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4527">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4529">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4529">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-4531">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4531">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4533">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4533">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4535">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4536">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-4537">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4538">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4539">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4540">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4540">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4542">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="386eb-4543">DXGI_FORMAT_R9G9B9E5 \_ Шаредексп<sup>фнк</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="386eb-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="386eb-4544">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4544">Target</span></span> | <span data-ttu-id="386eb-4545">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4546">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4547">32</span><span class="sxs-lookup"><span data-stu-id="386eb-4547">32</span></span> |
| <span data-ttu-id="386eb-4548">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4548">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4550">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4550">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4551">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4552">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4553">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4554">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4556">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4558">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4560">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4562">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4562">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4564">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4564">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4566">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4567">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4568">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4569">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4570">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4572">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4573">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4574">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4575">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4576">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4577">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4578">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4579">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4580">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4581">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4582">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4583">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4584">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4585">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4586">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4587">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4588">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4588">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4590">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4591">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4592">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4593">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4594">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4595">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4596">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-4597">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4598">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4599">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4600">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-4601">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="386eb-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>ФНК</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="386eb-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="386eb-4603">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4603">Target</span></span> | <span data-ttu-id="386eb-4604">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4605">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4606">16</span><span class="sxs-lookup"><span data-stu-id="386eb-4606">16</span></span> |
| <span data-ttu-id="386eb-4607">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4607">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4609">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4609">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4610">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4611">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4612">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4613">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4615">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4617">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4619">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4621">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4621">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4623">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4623">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4625">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4626">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4627">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4628">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4629">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4629">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4631">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4632">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4633">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4634">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4635">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4636">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4637">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4638">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4639">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4640">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4641">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4642">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4643">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4644">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4645">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4646">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4647">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4647">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4649">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4650">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4651">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4652">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4653">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4654">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4655">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-4656">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4657">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4658">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4659">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-4660">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="386eb-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>ФНК</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="386eb-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="386eb-4662">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4662">Target</span></span> | <span data-ttu-id="386eb-4663">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4664">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4665">16</span><span class="sxs-lookup"><span data-stu-id="386eb-4665">16</span></span> |
| <span data-ttu-id="386eb-4666">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4666">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4668">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4668">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4669">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4670">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4671">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4672">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4674">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4676">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4678">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4680">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4680">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4682">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4682">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4684">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4685">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4686">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4687">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4688">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4690">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4691">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4692">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4693">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4694">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4695">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4696">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4697">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4698">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4699">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4700">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4701">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4702">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4703">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4704">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4705">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4706">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4706">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4708">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4709">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4710">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4711">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4712">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4713">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4714">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-4715">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4716">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4717">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4718">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-4719">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="386eb-4720">DXGI_FORMAT_BC1 \_ нетипизированных<sup>пкк</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="386eb-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="386eb-4721">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4721">Target</span></span> | <span data-ttu-id="386eb-4722">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4723">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4724">4</span><span class="sxs-lookup"><span data-stu-id="386eb-4724">4</span></span> |
| <span data-ttu-id="386eb-4725">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4725">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4727">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4727">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4728">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4729">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4730">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4732">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4734">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4736">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4738">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-4739">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4740">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4741">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4742">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4743">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4744">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4744">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4746">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4747">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4748">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4749">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4750">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4751">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4752">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4753">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4754">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4755">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4756">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4757">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4758">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4759">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4760">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4761">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4762">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4762">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4764">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4765">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4766">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4767">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4768">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4769">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4770">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4770">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4772">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4773">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4774">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4775">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4775">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4777">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="386eb-4778">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="386eb-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="386eb-4779">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4779">Target</span></span> | <span data-ttu-id="386eb-4780">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4781">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4782">4</span><span class="sxs-lookup"><span data-stu-id="386eb-4782">4</span></span> |
| <span data-ttu-id="386eb-4783">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4783">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4785">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4785">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4786">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4787">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4788">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4790">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4792">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4794">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4796">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4796">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4798">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4798">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4800">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4801">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4802">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4803">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4804">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4804">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4806">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4807">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4808">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4809">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4810">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4811">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4812">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4813">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4814">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4815">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4816">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4817">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4818">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4819">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4820">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4821">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4822">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4822">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4824">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4825">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4826">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4827">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4828">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4829">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4830">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4830">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4832">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4833">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4834">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4835">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4835">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4837">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="386eb-4838">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="386eb-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="386eb-4839">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4839">Target</span></span> | <span data-ttu-id="386eb-4840">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4841">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4842">4</span><span class="sxs-lookup"><span data-stu-id="386eb-4842">4</span></span> |
| <span data-ttu-id="386eb-4843">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4843">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4845">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4845">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4846">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4847">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4848">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4850">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4852">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4854">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4856">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4856">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4858">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4858">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4860">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4861">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4862">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4863">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4864">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4864">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4866">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4867">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4868">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4869">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4870">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4871">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4872">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4873">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4874">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4875">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4876">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4877">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4878">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4879">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4880">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4881">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4882">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4882">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4884">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4885">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4886">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4887">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4888">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4889">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4890">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4890">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4892">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4893">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4894">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4895">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4895">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4897">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="386eb-4898">DXGI_FORMAT_BC2 \_ нетипизированных<sup>пкк</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="386eb-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="386eb-4899">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4899">Target</span></span> | <span data-ttu-id="386eb-4900">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4901">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4902">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4902">8</span></span> |
| <span data-ttu-id="386eb-4903">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4903">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4905">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4905">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4906">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4907">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4908">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4910">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4912">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4914">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4916">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-4917">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-4918">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4919">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4920">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4921">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4922">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4922">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4924">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4925">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4926">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4927">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4928">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4929">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4930">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4931">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4932">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4933">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4934">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4935">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4936">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4937">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4938">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4939">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4940">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-4940">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4942">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4943">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4944">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-4945">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-4946">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-4947">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-4948">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-4948">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4950">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-4951">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-4952">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-4953">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4953">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4955">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="386eb-4956">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="386eb-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="386eb-4957">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-4957">Target</span></span> | <span data-ttu-id="386eb-4958">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-4959">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-4960">8</span><span class="sxs-lookup"><span data-stu-id="386eb-4960">8</span></span> |
| <span data-ttu-id="386eb-4961">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-4961">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4963">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-4963">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4964">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4965">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4966">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-4968">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-4970">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-4972">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4974">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-4974">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4976">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-4976">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4978">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-4979">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-4980">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-4981">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-4982">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4982">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-4984">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-4985">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4986">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-4987">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-4988">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-4989">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4990">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-4991">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-4992">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-4993">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-4994">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-4995">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-4996">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-4997">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-4998">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-4999">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5000">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5000">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5002">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5003">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5004">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5005">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5006">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5007">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5008">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5008">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5010">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5011">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5012">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5013">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5013">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5015">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="386eb-5016">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="386eb-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="386eb-5017">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5017">Target</span></span> | <span data-ttu-id="386eb-5018">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5019">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5020">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5020">8</span></span> |
| <span data-ttu-id="386eb-5021">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5021">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5023">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5023">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5024">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5025">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5026">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5028">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5030">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5032">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5034">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5034">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5036">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5036">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5038">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5039">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5040">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5041">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5042">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5042">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5044">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5045">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5046">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5047">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5048">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5049">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5050">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5051">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5052">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5053">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5054">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5055">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5056">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5057">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5058">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5059">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5060">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5060">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5062">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5063">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5064">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5065">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5066">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5067">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5068">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5068">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5070">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5071">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5072">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5073">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5073">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5075">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="386eb-5076">DXGI_FORMAT_BC3 \_ нетипизированных<sup>пкк</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="386eb-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="386eb-5077">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5077">Target</span></span> | <span data-ttu-id="386eb-5078">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5079">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5080">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5080">8</span></span> |
| <span data-ttu-id="386eb-5081">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5081">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5083">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5083">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5084">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5085">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5086">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5088">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5090">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5092">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5094">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-5095">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-5096">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5097">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5098">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5099">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5100">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5100">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5102">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5103">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5104">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5105">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5106">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5107">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5108">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5109">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5110">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5111">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5112">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5113">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5114">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5115">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5116">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5117">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5118">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5118">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5120">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5121">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5122">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5123">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5124">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5125">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5126">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5126">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5128">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5129">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5130">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5131">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5131">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5133">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="386eb-5134">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="386eb-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="386eb-5135">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5135">Target</span></span> | <span data-ttu-id="386eb-5136">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5137">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5138">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5138">8</span></span> |
| <span data-ttu-id="386eb-5139">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5139">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5141">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5141">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5142">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5143">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5144">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5146">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5148">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5150">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5152">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5152">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5154">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5154">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5156">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5157">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5158">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5159">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5160">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5160">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5162">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5163">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5164">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5165">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5166">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5167">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5168">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5169">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5170">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5171">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5172">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5173">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5174">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5175">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5176">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5177">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5178">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5178">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5180">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5181">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5182">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5183">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5184">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5185">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5186">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5186">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5188">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5189">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5190">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5191">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5191">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5193">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="386eb-5194">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="386eb-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="386eb-5195">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5195">Target</span></span> | <span data-ttu-id="386eb-5196">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5197">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5198">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5198">8</span></span> |
| <span data-ttu-id="386eb-5199">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5199">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5201">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5201">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5202">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5203">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5204">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5206">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5208">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5210">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5212">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5212">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5214">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5214">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5216">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5217">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5218">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5219">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5220">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5220">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5222">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5223">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5224">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5225">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5226">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5227">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5228">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5229">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5230">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5231">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5232">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5233">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5234">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5235">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5236">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5237">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5238">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5238">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5240">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5241">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5242">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5243">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5244">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5245">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5246">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5246">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5248">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5249">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5250">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5251">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5251">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5253">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="386eb-5254">DXGI_FORMAT_BC4 \_ нетипизированных<sup>пкк</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="386eb-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="386eb-5255">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5255">Target</span></span> | <span data-ttu-id="386eb-5256">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5257">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5258">4</span><span class="sxs-lookup"><span data-stu-id="386eb-5258">4</span></span> |
| <span data-ttu-id="386eb-5259">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5259">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5261">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5261">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5262">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5263">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5264">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5266">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5268">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5270">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5272">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-5273">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-5274">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5275">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5276">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5277">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5278">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5278">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5280">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5281">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5282">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5283">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5284">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5285">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5286">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5287">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5288">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5289">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5290">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5291">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5292">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5293">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5294">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5295">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5296">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5296">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5298">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5299">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5300">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5301">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5302">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5303">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5304">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5304">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5306">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5307">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5308">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5309">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5310">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="386eb-5311">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="386eb-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="386eb-5312">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5312">Target</span></span> | <span data-ttu-id="386eb-5313">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5314">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5315">4</span><span class="sxs-lookup"><span data-stu-id="386eb-5315">4</span></span> |
| <span data-ttu-id="386eb-5316">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5316">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5318">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5318">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5319">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5320">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5321">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5323">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5325">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5327">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5329">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5329">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5331">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5331">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5333">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5334">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5335">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5336">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5337">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5337">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5339">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5340">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5341">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5342">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5343">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5344">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5345">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5346">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5347">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5348">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5349">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5350">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5351">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5352">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5353">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5354">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5355">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5355">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5357">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5358">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5359">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5360">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5361">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5362">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5363">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5363">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5365">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5366">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5367">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5368">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5369">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="386eb-5370">DXGI_FORMAT_BC4 \_ Снорм<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="386eb-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="386eb-5371">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5371">Target</span></span> | <span data-ttu-id="386eb-5372">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5373">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5374">4</span><span class="sxs-lookup"><span data-stu-id="386eb-5374">4</span></span> |
| <span data-ttu-id="386eb-5375">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5375">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5377">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5377">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5378">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5379">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5380">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5382">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5384">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5386">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5388">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5388">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5390">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5390">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5392">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5393">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5394">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5395">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5396">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5396">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5398">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5399">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5400">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5401">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5402">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5403">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5404">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5405">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5406">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5407">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5408">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5409">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5410">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5411">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5412">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5413">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5414">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5414">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5416">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5417">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5418">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5419">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5420">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5421">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5422">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5422">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5424">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5425">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5426">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5427">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5428">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="386eb-5429">DXGI_FORMAT_BC5 \_ нетипизированных<sup>пкк</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="386eb-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="386eb-5430">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5430">Target</span></span> | <span data-ttu-id="386eb-5431">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5432">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5433">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5433">8</span></span> |
| <span data-ttu-id="386eb-5434">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5434">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5436">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5436">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5437">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5438">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5439">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5441">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5443">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5445">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5447">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-5448">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-5449">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5450">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5451">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5452">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5453">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5453">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5455">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5456">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5457">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5458">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5459">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5460">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5461">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5462">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5463">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5464">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5465">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5466">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5467">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5468">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5469">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5470">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5471">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5471">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5473">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5474">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5475">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5476">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5477">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5478">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5479">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5479">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5481">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5482">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5483">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5484">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5485">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="386eb-5486">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="386eb-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="386eb-5487">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5487">Target</span></span> | <span data-ttu-id="386eb-5488">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5489">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5490">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5490">8</span></span> |
| <span data-ttu-id="386eb-5491">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5491">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5493">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5493">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5494">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5495">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5496">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5498">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5500">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5502">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5504">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5504">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5506">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5506">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5508">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5509">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5510">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5511">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5512">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5514">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5515">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5516">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5517">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5518">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5519">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5520">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5521">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5522">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5523">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5524">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5525">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5526">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5527">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5528">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5529">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5530">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5530">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5532">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5533">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5534">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5535">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5536">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5537">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5538">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5538">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5540">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5541">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5542">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5543">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5544">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="386eb-5545">DXGI_FORMAT_BC5 \_ Снорм<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="386eb-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="386eb-5546">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5546">Target</span></span> | <span data-ttu-id="386eb-5547">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5548">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5549">8</span><span class="sxs-lookup"><span data-stu-id="386eb-5549">8</span></span> |
| <span data-ttu-id="386eb-5550">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5550">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5552">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5552">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5553">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5554">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5555">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5557">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5559">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5561">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5563">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5563">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5565">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5565">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5567">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5568">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5569">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5570">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5571">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5571">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5573">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5574">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5575">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5576">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5577">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5578">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5579">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5580">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5581">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5582">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5583">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5584">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5585">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5586">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5587">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5588">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5589">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5589">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5591">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5592">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5593">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5594">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5595">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5596">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5597">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5597">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5599">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5600">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5601">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5602">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5603">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="386eb-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>фнс</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="386eb-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="386eb-5605">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5605">Target</span></span> | <span data-ttu-id="386eb-5606">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5607">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5608">16</span><span class="sxs-lookup"><span data-stu-id="386eb-5608">16</span></span> |
| <span data-ttu-id="386eb-5609">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5609">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5611">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5611">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5613">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5613">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5615">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5616">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5617">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5619">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5621">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5623">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5625">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5625">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5627">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5627">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5629">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5630">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5631">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5632">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5633">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5633">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5635">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5635">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5637">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5637">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5639">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5639">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5641">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5642">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5643">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5644">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5645">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5646">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5647">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5648">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5649">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5650">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5651">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5652">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5653">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5654">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5654">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5656">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5656">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5658">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5658">8x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5660">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5660">Other Multisample Count RT</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5662">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5662">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5664">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5664">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5666">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5667">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-5668">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5669">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5670">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5671">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5672">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="386eb-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>фнс</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="386eb-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="386eb-5674">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5674">Target</span></span> | <span data-ttu-id="386eb-5675">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5676">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5677">16</span><span class="sxs-lookup"><span data-stu-id="386eb-5677">16</span></span> |
| <span data-ttu-id="386eb-5678">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5678">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5680">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5680">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5682">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5682">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5684">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5685">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5686">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5688">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5690">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5692">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5694">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5694">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5696">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5696">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5698">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5699">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5700">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5701">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5702">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5702">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5704">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5704">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5706">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5706">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5708">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5708">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5710">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5711">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5712">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5713">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5714">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5715">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5716">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5717">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5718">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5719">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5720">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5721">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5722">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5723">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5723">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5725">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5725">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5727">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5727">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5729">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5729">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5731">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5731">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5733">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5733">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5735">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5736">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-5737">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5738">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5739">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5740">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-5741">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="386eb-5742">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8A8 (90)</span><span class="sxs-lookup"><span data-stu-id="386eb-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="386eb-5743">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5743">Target</span></span> | <span data-ttu-id="386eb-5744">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5745">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5746">32</span><span class="sxs-lookup"><span data-stu-id="386eb-5746">32</span></span> |
| <span data-ttu-id="386eb-5747">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5747">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5749">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5749">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5750">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5751">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5752">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5753">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5755">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5757">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5759">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5761">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-5762">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-5763">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5764">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5765">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5766">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5767">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5767">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5769">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5770">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5771">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5772">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5773">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5774">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5775">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5776">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5777">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5778">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5779">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5780">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5781">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5782">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5783">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5784">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5785">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5785">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5787">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5788">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5789">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5790">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5791">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5792">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5793">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5793">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5795">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5796">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-5797">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-5798">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5798">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5800">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="386eb-5801">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="386eb-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="386eb-5802">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5802">Target</span></span> | <span data-ttu-id="386eb-5803">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5804">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5805">32</span><span class="sxs-lookup"><span data-stu-id="386eb-5805">32</span></span> |
| <span data-ttu-id="386eb-5806">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5806">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5808">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5808">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5810">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5810">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5812">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5813">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5814">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5816">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5818">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5820">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5822">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5822">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5824">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5824">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5826">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5827">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5828">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5829">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5830">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5830">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5832">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5832">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5834">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5834">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5836">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5836">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5838">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5839">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5840">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5841">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5842">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5843">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5844">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5845">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5846">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5847">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5848">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5849">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5850">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5851">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5851">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5853">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5853">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5855">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5855">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5857">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5857">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5859">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5859">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5861">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5861">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5863">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5863">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5865">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5865">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5867">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5868">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5868">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5870">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5870">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5872">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5872">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5874">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="386eb-5875">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="386eb-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="386eb-5876">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5876">Target</span></span> | <span data-ttu-id="386eb-5877">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5878">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5879">32</span><span class="sxs-lookup"><span data-stu-id="386eb-5879">32</span></span> |
| <span data-ttu-id="386eb-5880">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5880">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5882">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5882">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5883">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5884">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5885">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5886">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5888">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5890">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5892">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5894">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5894">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5896">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5896">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5898">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5899">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5900">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5901">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5902">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5902">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5904">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5904">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5906">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5906">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5908">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5908">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5910">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5911">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5912">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5913">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5914">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5915">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5916">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5917">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5918">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5919">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5920">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5921">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5922">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5923">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5923">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5925">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5925">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5927">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5927">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5929">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5929">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5931">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5931">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5933">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5933">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5935">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5935">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5937">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5937">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5939">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-5940">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5940">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5942">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-5942">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-5944">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5944">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5946">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="386eb-5947">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8X8 (92)</span><span class="sxs-lookup"><span data-stu-id="386eb-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="386eb-5948">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-5948">Target</span></span> | <span data-ttu-id="386eb-5949">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-5950">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-5951">32</span><span class="sxs-lookup"><span data-stu-id="386eb-5951">32</span></span> |
| <span data-ttu-id="386eb-5952">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-5952">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5954">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-5954">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5955">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5956">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5957">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-5958">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-5960">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-5962">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-5964">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5966">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-5967">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-5968">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-5969">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-5970">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-5971">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-5972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5972">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5974">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-5975">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5976">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5977">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-5978">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-5979">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5980">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-5981">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-5982">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-5983">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-5984">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-5985">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-5986">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-5987">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-5988">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5989">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-5990">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-5990">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-5992">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5993">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-5994">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-5995">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-5996">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-5997">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-5998">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-5998">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6000">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6001">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-6002">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-6003">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6003">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6005">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="386eb-6006">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="386eb-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="386eb-6007">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6007">Target</span></span> | <span data-ttu-id="386eb-6008">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6009">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6010">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6010">32</span></span> |
| <span data-ttu-id="386eb-6011">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6011">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6013">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6013">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6015">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6015">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6017">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6018">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6019">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6021">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6023">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6025">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6027">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6027">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6029">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6029">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6031">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6032">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6033">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6034">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6035">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6037">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6037">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6039">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6039">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6041">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6041">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6043">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6044">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6045">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6046">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6047">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6048">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6049">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6050">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6051">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6052">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6053">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6054">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6055">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6056">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6056">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6058">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6058">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6060">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6060">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6062">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6062">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6064">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6064">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6066">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6066">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6068">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6069">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6069">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6071">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6072">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6072">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6074">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6074">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6076">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6076">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6078">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="386eb-6079">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="386eb-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="386eb-6080">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6080">Target</span></span> | <span data-ttu-id="386eb-6081">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6082">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6083">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6083">32</span></span> |
| <span data-ttu-id="386eb-6084">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6084">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6086">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6086">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6087">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6088">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6089">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6090">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6092">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6094">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6096">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6098">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6098">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6100">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6100">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6102">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6103">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6104">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6105">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6106">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6106">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6108">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6108">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6110">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6110">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6112">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6112">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6114">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6115">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6116">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6117">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6118">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6119">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6120">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6121">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6122">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6123">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6124">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6125">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6126">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6127">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6127">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6129">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6129">4x Multisample RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6131">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6131">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6133">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6133">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6135">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6135">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6137">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6137">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6139">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6140">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6140">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6142">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6143">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-6144">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-6145">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6145">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6147">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="386eb-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="386eb-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="386eb-6149">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6149">Target</span></span> | <span data-ttu-id="386eb-6150">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6151">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6152">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6152">32</span></span> |
| <span data-ttu-id="386eb-6153">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6153">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6155">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6155">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6156">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6157">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6158">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6160">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6164">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6164">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6166">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6166">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6168">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6169">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6170">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6170">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6172">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6173">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6175">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6175">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6177">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6177">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6179">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6179">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6181">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6182">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6183">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6184">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6185">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6186">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6187">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6188">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6189">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6190">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6191">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6192">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6193">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6194">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6194">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6196">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6197">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6198">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6199">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6200">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6201">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6202">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6203">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6203">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6205">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6205">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6207">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6207">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6209">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6209">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6211">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="386eb-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="386eb-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="386eb-6213">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6213">Target</span></span> | <span data-ttu-id="386eb-6214">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6215">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6216">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6216">32</span></span> |
| <span data-ttu-id="386eb-6217">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6217">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6219">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6219">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6220">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6221">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6222">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6224">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6228">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6228">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6230">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6230">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6232">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6233">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6234">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6234">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6236">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6238">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6239">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6240">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6241">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6242">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6243">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6244">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6245">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6246">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6247">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6248">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6249">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6250">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6251">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6252">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6253">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6254">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6254">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6256">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6257">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6258">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6259">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6260">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6261">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6262">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6263">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6263">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6265">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6265">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6267">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6267">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6269">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6269">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6271">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="386eb-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="386eb-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="386eb-6273">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6273">Target</span></span> | <span data-ttu-id="386eb-6274">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6275">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6276">64</span><span class="sxs-lookup"><span data-stu-id="386eb-6276">64</span></span> |
| <span data-ttu-id="386eb-6277">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6277">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6279">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6279">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6280">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6281">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6282">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6284">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6288">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6288">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6290">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6290">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6292">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6293">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6294">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6294">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6296">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6297">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6299">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6300">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6301">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6302">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6303">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6304">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6305">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6306">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6307">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6308">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6309">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6310">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6311">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6312">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6313">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6314">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6315">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6315">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6317">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6318">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6319">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6320">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6321">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6322">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6323">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6324">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6324">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6326">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6326">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6328">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6328">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6330">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6330">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6332">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="386eb-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="386eb-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="386eb-6334">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6334">Target</span></span> | <span data-ttu-id="386eb-6335">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6336">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6337">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6337">8</span></span> |
| <span data-ttu-id="386eb-6338">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6338">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6340">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6340">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6341">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6342">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6343">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6345">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6349">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6349">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6351">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6351">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6353">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6354">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6355">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6355">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6357">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6358">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6359">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6360">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6360">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6362">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6362">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6364">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6365">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6366">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6367">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6368">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6369">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6370">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6371">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6372">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6373">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6374">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6375">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6376">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6377">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6377">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6379">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6380">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6381">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6382">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6383">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6384">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6385">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6386">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6386">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6388">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6388">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6390">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6390">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6392">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6392">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6394">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="386eb-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="386eb-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="386eb-6396">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6396">Target</span></span> | <span data-ttu-id="386eb-6397">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6398">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6399">16</span><span class="sxs-lookup"><span data-stu-id="386eb-6399">16</span></span> |
| <span data-ttu-id="386eb-6400">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6400">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6402">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6402">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6403">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6404">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6405">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6407">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6411">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6411">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6413">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6413">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6415">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6416">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6417">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6417">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6419">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6421">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6422">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6422">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6424">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6424">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6426">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6427">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6428">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6429">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6430">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6431">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6432">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6433">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6434">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6435">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6436">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6437">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6438">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6439">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6439">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6441">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6442">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6443">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6444">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6445">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6446">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6447">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6448">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6448">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6450">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6450">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6452">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6452">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6454">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6454">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6456">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="386eb-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="386eb-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="386eb-6458">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6458">Target</span></span> | <span data-ttu-id="386eb-6459">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6460">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6461">16</span><span class="sxs-lookup"><span data-stu-id="386eb-6461">16</span></span> |
| <span data-ttu-id="386eb-6462">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6462">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6464">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6464">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6465">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6466">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6467">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6469">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6473">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6473">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6475">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6475">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6477">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6478">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6479">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6479">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6481">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6483">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6484">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6484">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6486">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6486">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6488">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6489">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6490">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6491">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6492">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6493">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6494">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6495">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6496">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6497">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6498">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6499">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6500">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6501">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6501">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6503">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6504">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6505">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6506">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6507">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6508">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6509">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6510">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6510">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6512">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6512">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6514">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6514">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6516">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6516">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6518">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="386eb-6519">DXGI_FORMAT_420 \_ непрозрачный<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="386eb-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="386eb-6520">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6520">Target</span></span> | <span data-ttu-id="386eb-6521">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6522">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6523">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6523">8</span></span> |
| <span data-ttu-id="386eb-6524">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6524">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6526">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6526">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6527">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6528">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6529">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6531">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6535">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-6536">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-6537">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6538">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6539">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6540">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6541">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6542">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6543">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6544">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6545">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6546">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6547">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6548">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6549">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6550">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6551">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6552">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6553">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6554">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6555">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6556">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6557">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6558">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="386eb-6559">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6560">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6561">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6562">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6563">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6564">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6565">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6566">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6566">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6568">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6568">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6570">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6570">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6572">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6572">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6574">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="386eb-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="386eb-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="386eb-6576">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6576">Target</span></span> | <span data-ttu-id="386eb-6577">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6578">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6579">16</span><span class="sxs-lookup"><span data-stu-id="386eb-6579">16</span></span> |
| <span data-ttu-id="386eb-6580">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6580">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6582">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6582">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6583">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6584">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6585">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6587">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6591">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6591">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6593">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6593">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6595">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6596">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6597">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6597">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6599">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6601">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6602">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6603">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6604">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6605">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6606">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6607">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6608">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6609">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6610">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6611">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6612">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6613">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6614">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6615">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6616">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6617">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6617">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6619">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6620">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6621">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6622">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6623">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6624">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6625">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6626">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6626">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6628">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6628">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6630">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6630">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6632">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6632">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6634">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="386eb-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="386eb-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="386eb-6636">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6636">Target</span></span> | <span data-ttu-id="386eb-6637">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6638">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6639">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6639">32</span></span> |
| <span data-ttu-id="386eb-6640">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6640">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6642">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6642">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6643">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6644">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6645">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6647">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6651">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6651">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6653">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6653">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6655">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6656">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6657">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6657">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6659">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6660">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6661">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6662">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6663">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6664">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6665">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6666">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6667">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6668">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6669">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6670">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6671">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6672">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6673">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6674">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6675">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6676">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6677">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6677">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6679">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6680">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6681">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6682">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6683">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6684">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6685">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6686">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6686">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6688">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6688">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6690">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6690">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6692">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6692">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6694">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="386eb-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="386eb-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="386eb-6696">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6696">Target</span></span> | <span data-ttu-id="386eb-6697">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6698">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6699">32</span><span class="sxs-lookup"><span data-stu-id="386eb-6699">32</span></span> |
| <span data-ttu-id="386eb-6700">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6700">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6702">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6702">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6703">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6704">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6705">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6707">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6711">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6711">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6713">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6713">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6715">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6716">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6717">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6717">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6719">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6720">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6721">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6722">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6723">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6724">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6725">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6726">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6727">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6728">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6729">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6730">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6731">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6732">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6733">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6734">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6735">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6736">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6737">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6737">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6739">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6740">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6741">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6742">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6743">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6744">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6745">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6746">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6746">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6748">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6748">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6750">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6750">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6752">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6752">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6754">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="386eb-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="386eb-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="386eb-6756">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6756">Target</span></span> | <span data-ttu-id="386eb-6757">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6758">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6759">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6759">8</span></span> |
| <span data-ttu-id="386eb-6760">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6760">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6762">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6762">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6763">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6764">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6765">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6767">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6771">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6771">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6773">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6773">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6775">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6776">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6777">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6777">Shader gather4</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6779">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6781">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6782">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6782">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6784">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6784">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6786">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6787">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6788">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6789">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6790">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6791">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6792">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6793">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6794">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6795">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6796">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6797">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6798">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6799">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6799">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6801">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6802">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6803">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6804">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6805">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6806">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6807">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6808">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6808">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6810">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6810">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6812">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6812">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6814">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6814">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6816">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="386eb-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="386eb-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="386eb-6818">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6818">Target</span></span> | <span data-ttu-id="386eb-6819">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6820">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6821">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6821">8</span></span> |
| <span data-ttu-id="386eb-6822">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6822">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6824">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6824">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6825">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6826">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6827">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6829">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6833">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-6834">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-6835">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6836">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6837">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6838">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6839">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6840">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6841">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6842">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6843">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6844">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6845">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6846">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6847">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6848">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6849">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6850">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6851">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6852">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6853">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6854">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6855">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6856">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6856">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6858">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6859">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6860">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6861">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6862">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6863">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6864">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6865">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6866">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6866">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6868">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-6869">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-6870">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="386eb-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="386eb-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="386eb-6872">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6872">Target</span></span> | <span data-ttu-id="386eb-6873">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6874">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6875">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6875">8</span></span> |
| <span data-ttu-id="386eb-6876">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6876">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6878">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6878">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6879">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6880">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6881">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6883">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6887">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-6888">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-6889">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6890">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6891">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6892">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6893">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6894">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6895">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6896">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6897">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6898">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6899">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6900">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6901">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6902">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6903">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6904">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6905">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6906">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6907">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6908">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6909">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6910">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6910">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6912">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6913">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6914">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6915">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6916">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6917">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6918">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6919">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6920">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6920">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6922">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-6923">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-6924">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="386eb-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="386eb-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="386eb-6926">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6926">Target</span></span> | <span data-ttu-id="386eb-6927">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6928">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6929">8</span><span class="sxs-lookup"><span data-stu-id="386eb-6929">8</span></span> |
| <span data-ttu-id="386eb-6930">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6930">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6932">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6932">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6933">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6934">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6935">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6937">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6941">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-6942">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-6943">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6944">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6945">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-6946">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-6947">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-6948">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-6949">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6950">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6951">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-6952">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-6953">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6954">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-6955">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-6956">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-6957">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-6958">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-6959">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-6960">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-6961">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-6962">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6963">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-6964">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-6964">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6966">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6967">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-6968">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-6969">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-6970">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-6971">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-6972">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-6973">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-6974">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6974">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6976">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-6977">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-6978">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="386eb-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="386eb-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="386eb-6980">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-6980">Target</span></span> | <span data-ttu-id="386eb-6981">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-6982">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-6983">16</span><span class="sxs-lookup"><span data-stu-id="386eb-6983">16</span></span> |
| <span data-ttu-id="386eb-6984">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-6984">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-6986">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-6986">Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6987">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6988">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6989">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="386eb-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-6991">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="386eb-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="386eb-6995">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="386eb-6996">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="386eb-6997">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-6998">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-6999">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-7000">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-7001">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="386eb-7002">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="386eb-7003">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-7004">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-7005">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-7006">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-7007">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-7008">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-7009">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-7010">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-7011">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-7012">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-7013">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-7014">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-7015">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-7016">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-7017">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-7018">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-7018">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7020">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-7021">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="386eb-7022">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="386eb-7023">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="386eb-7024">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="386eb-7025">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-7026">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-7027">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-7028">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-7028">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7030">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-7031">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-7032">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="386eb-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>фнс</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="386eb-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="386eb-7034">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="386eb-7034">Target</span></span> | <span data-ttu-id="386eb-7035">Поддержка</span><span class="sxs-lookup"><span data-stu-id="386eb-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="386eb-7036">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="386eb-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="386eb-7037">16</span><span class="sxs-lookup"><span data-stu-id="386eb-7037">16</span></span> |
| <span data-ttu-id="386eb-7038">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="386eb-7038">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7040">Буфер</span><span class="sxs-lookup"><span data-stu-id="386eb-7040">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7042">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-7042">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7044">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="386eb-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="386eb-7045">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="386eb-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="386eb-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="386eb-7046">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="386eb-7048">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="386eb-7050">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="386eb-7052">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7054">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="386eb-7054">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7056">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="386eb-7056">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7058">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="386eb-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="386eb-7059">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="386eb-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="386eb-7060">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="386eb-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="386eb-7061">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="386eb-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="386eb-7062">Mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-7062">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7064">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="386eb-7064">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7066">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7066">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7068">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="386eb-7068">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7070">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="386eb-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="386eb-7071">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="386eb-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="386eb-7072">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-7073">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="386eb-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="386eb-7074">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="386eb-7075">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="386eb-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="386eb-7076">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="386eb-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="386eb-7077">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="386eb-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="386eb-7078">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="386eb-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="386eb-7079">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="386eb-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="386eb-7080">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="386eb-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="386eb-7081">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-7082">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="386eb-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="386eb-7083">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="386eb-7083">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7085">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7085">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7087">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="386eb-7087">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7089">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="386eb-7089">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7091">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="386eb-7091">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="386eb-7093">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="386eb-7093">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="386eb-7095">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="386eb-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="386eb-7096">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="386eb-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="386eb-7097">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="386eb-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="386eb-7098">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="386eb-7099">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="386eb-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="386eb-7100">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="386eb-7101">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="386eb-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="386eb-7102">Форматирование заметок</span><span class="sxs-lookup"><span data-stu-id="386eb-7102">Format notes</span></span>

<span data-ttu-id="386eb-7103">Назначение формата может изменяться с одного уровня компонентов оборудования на следующий.</span><span class="sxs-lookup"><span data-stu-id="386eb-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="386eb-7104"><sup>L</sup> : нетипизированный формат</span><span class="sxs-lookup"><span data-stu-id="386eb-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="386eb-7105"><sup>ПК</sup> : частично типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="386eb-7106"><sup>FCS</sup> : полностью типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="386eb-7107"><sup>ФНС</sup> : полностью типизированный, неприведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="386eb-7108"><sup>ПКК</sup> : частично типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="386eb-7109"><sup>FCC</sup> : полностью типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="386eb-7110"><sup>ФНК</sup> : полностью типизированный, неприведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="386eb-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="386eb-7111"><sup>V</sup> : формат видео</span><span class="sxs-lookup"><span data-stu-id="386eb-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="386eb-7112">Задние буферы и сканирование с форматом [**DXGI \_ \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) содержат данные гаммы с линейным значением.</span><span class="sxs-lookup"><span data-stu-id="386eb-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="386eb-7113">См. также</span><span class="sxs-lookup"><span data-stu-id="386eb-7113">Related topics</span></span>

[<span data-ttu-id="386eb-7114">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="386eb-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="386eb-7115">**ID3D10Device:: Чеккформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="386eb-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="386eb-7116">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="386eb-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
