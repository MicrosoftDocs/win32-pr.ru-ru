---
description: В этом разделе указаны форматы ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,1.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Поддержка форматов для оборудования Direct3D с уровнем компонентов 9.9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894394"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="110b2-103">Поддержка форматов для оборудования Direct3D с уровнем компонентов 9.9.1</span><span class="sxs-lookup"><span data-stu-id="110b2-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="110b2-104">В этом разделе указаны форматы ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,1.</span><span class="sxs-lookup"><span data-stu-id="110b2-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="110b2-105">В таблице приводится сводка по поддержке функций с использованием следующего ключа.</span><span class="sxs-lookup"><span data-stu-id="110b2-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="110b2-106">Символ</span><span class="sxs-lookup"><span data-stu-id="110b2-106">Symbol</span></span>                            | <span data-ttu-id="110b2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="110b2-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="110b2-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="110b2-108">_ *-*\*</span></span>                             | <span data-ttu-id="110b2-109">Не разрешено или недоступно.</span><span class="sxs-lookup"><span data-stu-id="110b2-109">Disallowed or not available.</span></span>                                                  |
| ![обязательно](images/letter-r.jpg)  | <span data-ttu-id="110b2-111">Требуется поддержка оборудования.</span><span class="sxs-lookup"><span data-stu-id="110b2-111">Hardware support is required.</span></span>                                                 |
| ![необязательно](images/letter-o.jpg)  | <span data-ttu-id="110b2-113">Аппаратная поддержка необязательно. формат аппаратного ускорения может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="110b2-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![зависимых](images/letter-d.jpg) | <span data-ttu-id="110b2-115">Требуется, если поддерживается дополнительная функция.</span><span class="sxs-lookup"><span data-stu-id="110b2-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="110b2-116">Этот раздел содержит раздел для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="110b2-116">This topic contains a section per format.</span></span> <span data-ttu-id="110b2-117">*Цель* формата (таблицы содержат по одной строке на каждый целевой объект) может быть типом ресурса, встроенной функцией HLSL или определенной функциональностью, зависящей от конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="110b2-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="110b2-118">Чтобы программно проверить поддержку формата в D3D11 и D3D12, обратитесь к статье [Проверка поддержки аппаратных компонентов](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="110b2-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="110b2-119">Числа форматов в основном, но не все, в возрастающем числовом порядке &mdash; , некоторые из них имеют нечисловой порядок и перечислены вместе с другими соответствующими форматами.</span><span class="sxs-lookup"><span data-stu-id="110b2-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="110b2-120">Обратите внимание, что *тип* в имени формата может означать *частичную* типизацию, а не строго типизированный (см. раздел [Format Notes](#format-notes) в конце раздела).</span><span class="sxs-lookup"><span data-stu-id="110b2-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="110b2-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="110b2-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="110b2-122">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-122">Target</span></span> | <span data-ttu-id="110b2-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-123">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-124">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-125">0</span><span class="sxs-lookup"><span data-stu-id="110b2-125">0</span></span> |
| <span data-ttu-id="110b2-126">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-126">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-127">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-127">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-128">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-129">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-130">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-131">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-132">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-133">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-134">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-135">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-136">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-137">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-138">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-139">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-140">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-141">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-142">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-143">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-144">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-145">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-146">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-147">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-148">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-149">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-150">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-151">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-152">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-153">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-154">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-155">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-156">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-157">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-158">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-159">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-160">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-161">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-162">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-163">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-164">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-165">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-166">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-167">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-168">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-169">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-170">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="110b2-171">\_Нетипизированные<sup>ПК</sup> DXGI_FORMAT_R32G32B32A32 (1)</span><span class="sxs-lookup"><span data-stu-id="110b2-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="110b2-172">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-172">Target</span></span> | <span data-ttu-id="110b2-173">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-173">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-174">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-175">128</span><span class="sxs-lookup"><span data-stu-id="110b2-175">128</span></span> |
| <span data-ttu-id="110b2-176">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-176">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-177">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-177">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-178">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-179">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-180">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-181">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-182">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-183">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-184">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-185">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-186">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-187">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-188">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-189">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-190">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-191">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-192">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-193">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-194">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-195">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-196">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-197">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-198">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-199">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-200">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-201">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-202">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-203">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-204">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-205">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-206">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-207">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-208">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-209">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-210">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-211">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-212">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-213">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-214">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-215">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-216">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-217">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-218">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-219">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-220">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="110b2-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>ФНС</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="110b2-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="110b2-222">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-222">Target</span></span> | <span data-ttu-id="110b2-223">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-223">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-224">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-225">128</span><span class="sxs-lookup"><span data-stu-id="110b2-225">128</span></span> |
| <span data-ttu-id="110b2-226">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-226">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-228">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-228">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-229">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-229">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-231">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-232">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-233">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-234">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-235">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-236">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-237">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-238">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-239">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-240">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-241">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-242">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-243">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-243">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-244">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-245">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-246">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-247">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-248">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-249">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-250">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-251">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-252">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-253">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-254">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-255">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-256">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-257">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-258">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-259">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-260">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-261">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-262">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-263">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-264">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-265">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-266">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-267">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-268">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-269">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-270">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-271">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-272">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="110b2-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>ФНС</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="110b2-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="110b2-274">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-274">Target</span></span> | <span data-ttu-id="110b2-275">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-275">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-276">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-277">128</span><span class="sxs-lookup"><span data-stu-id="110b2-277">128</span></span> |
| <span data-ttu-id="110b2-278">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-278">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-279">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-279">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-280">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-281">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-282">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-283">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-284">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-285">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-286">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-287">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-288">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-289">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-290">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-291">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-292">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-293">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-293">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-294">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-295">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-296">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-297">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-298">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-299">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-300">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-301">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-302">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-303">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-304">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-305">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-306">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-307">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-308">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-309">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-310">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-311">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-312">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-313">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-314">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-315">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-316">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-317">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-318">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-319">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-320">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-321">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-322">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="110b2-323">DXGI_FORMAT_R32G32B32A32 \_ Синт<sup>ФНС</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="110b2-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="110b2-324">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-324">Target</span></span> | <span data-ttu-id="110b2-325">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-325">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-326">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-327">128</span><span class="sxs-lookup"><span data-stu-id="110b2-327">128</span></span> |
| <span data-ttu-id="110b2-328">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-328">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-329">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-329">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-330">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-331">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-332">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-333">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-334">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-335">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-336">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-337">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-338">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-339">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-340">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-341">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-342">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-343">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-343">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-344">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-345">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-346">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-347">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-348">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-349">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-350">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-351">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-352">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-353">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-354">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-355">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-356">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-357">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-358">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-359">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-360">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-361">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-362">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-363">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-364">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-365">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-366">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-367">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-368">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-369">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-370">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-371">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-372">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="110b2-373">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32B32 (5)</span><span class="sxs-lookup"><span data-stu-id="110b2-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="110b2-374">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-374">Target</span></span> | <span data-ttu-id="110b2-375">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-375">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-376">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-377">96</span><span class="sxs-lookup"><span data-stu-id="110b2-377">96</span></span> |
| <span data-ttu-id="110b2-378">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-378">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-379">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-379">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-380">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-381">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-382">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-383">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-384">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-385">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-386">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-387">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-388">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-389">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-390">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-391">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-392">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-393">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-393">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-394">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-395">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-396">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-397">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-398">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-399">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-400">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-401">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-402">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-403">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-404">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-405">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-406">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-407">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-408">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-409">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-410">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-411">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-412">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-413">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-414">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-415">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-416">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-417">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-418">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-419">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-420">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-421">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-422">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="110b2-423">DXGI_FORMAT_R32G32B32 \_ float<sup>ФНС</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="110b2-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="110b2-424">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-424">Target</span></span> | <span data-ttu-id="110b2-425">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-425">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-426">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-427">96</span><span class="sxs-lookup"><span data-stu-id="110b2-427">96</span></span> |
| <span data-ttu-id="110b2-428">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-428">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-430">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-430">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-431">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-431">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-433">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-434">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-435">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-436">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-437">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-438">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-439">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-440">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-441">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-442">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-443">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-444">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-445">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-446">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-447">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-448">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-448">Blendable RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-450">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-451">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-452">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-453">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-454">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-455">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-456">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-457">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-458">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-459">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-460">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-461">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-462">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-463">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-464">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-464">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-466">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-466">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-468">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-469">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-470">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-471">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-472">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-473">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-474">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-475">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-476">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-477">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="110b2-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>ФНС</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="110b2-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="110b2-479">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-479">Target</span></span> | <span data-ttu-id="110b2-480">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-480">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-481">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-482">96</span><span class="sxs-lookup"><span data-stu-id="110b2-482">96</span></span> |
| <span data-ttu-id="110b2-483">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-483">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-484">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-484">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-485">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-486">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-487">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-488">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-489">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-490">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-491">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-492">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-493">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-494">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-495">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-496">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-497">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-498">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-498">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-499">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-500">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-501">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-502">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-503">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-504">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-505">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-506">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-507">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-508">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-509">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-510">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-511">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-512">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-513">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-514">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-515">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-516">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-516">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-518">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-518">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-520">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-521">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-522">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-523">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-524">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-525">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-526">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-527">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-528">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-529">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="110b2-530">DXGI_FORMAT_R32G32B32 \_ Синт<sup>ФНС</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="110b2-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="110b2-531">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-531">Target</span></span> | <span data-ttu-id="110b2-532">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-532">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-533">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-534">96</span><span class="sxs-lookup"><span data-stu-id="110b2-534">96</span></span> |
| <span data-ttu-id="110b2-535">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-535">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-536">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-536">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-537">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-538">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-539">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-540">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-541">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-542">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-543">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-544">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-545">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-546">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-547">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-548">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-549">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-550">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-550">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-551">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-552">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-553">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-554">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-555">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-556">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-557">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-558">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-559">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-560">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-561">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-562">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-563">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-564">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-565">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-566">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-567">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-568">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-568">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-570">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-570">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="110b2-572">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-573">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-574">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-575">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-576">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-577">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-578">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-579">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-580">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-581">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="110b2-582">DXGI_FORMAT_R16G16B16A16 \_ <sup>ПК</sup> нетипизированных типов (9)</span><span class="sxs-lookup"><span data-stu-id="110b2-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="110b2-583">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-583">Target</span></span> | <span data-ttu-id="110b2-584">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-584">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-585">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-586">64</span><span class="sxs-lookup"><span data-stu-id="110b2-586">64</span></span> |
| <span data-ttu-id="110b2-587">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-587">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-588">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-588">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-589">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-590">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-591">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-592">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-593">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-594">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-595">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-596">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-597">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-598">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-599">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-600">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-601">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-602">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-602">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-603">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-604">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-605">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-606">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-607">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-608">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-609">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-610">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-611">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-612">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-613">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-614">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-615">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-616">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-617">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-618">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-619">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-620">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-621">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-622">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-623">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-624">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-625">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-626">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-627">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-628">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-629">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-630">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-631">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="110b2-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>ФНС</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="110b2-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="110b2-633">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-633">Target</span></span> | <span data-ttu-id="110b2-634">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-634">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-635">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-636">64</span><span class="sxs-lookup"><span data-stu-id="110b2-636">64</span></span> |
| <span data-ttu-id="110b2-637">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-637">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-638">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-638">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-639">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-640">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-641">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-642">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-643">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-644">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-645">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-646">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-647">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-648">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-649">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-650">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-651">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-652">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-653">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-654">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-655">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-656">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-657">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-658">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-659">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-660">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-661">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-662">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-663">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-664">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-665">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-666">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-667">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-668">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-669">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-670">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-671">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-672">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-673">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-674">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-675">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-676">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-677">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-678">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-679">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-680">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-680">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-682">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="110b2-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>ФНС</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="110b2-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="110b2-684">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-684">Target</span></span> | <span data-ttu-id="110b2-685">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-685">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-686">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-687">64</span><span class="sxs-lookup"><span data-stu-id="110b2-687">64</span></span> |
| <span data-ttu-id="110b2-688">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-688">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-689">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-689">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-690">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-691">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-692">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-693">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-694">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-695">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-696">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-697">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-698">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-699">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-700">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-701">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-702">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-703">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-704">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-705">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-706">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-707">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-708">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-709">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-710">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-711">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-712">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-713">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-714">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-715">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-716">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-717">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-718">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-719">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-720">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-721">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-722">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-723">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-724">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-725">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-726">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-727">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-728">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-729">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-730">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-731">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-732">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="110b2-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>ФНС</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="110b2-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="110b2-734">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-734">Target</span></span> | <span data-ttu-id="110b2-735">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-735">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-736">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-737">64</span><span class="sxs-lookup"><span data-stu-id="110b2-737">64</span></span> |
| <span data-ttu-id="110b2-738">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-738">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-739">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-739">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-740">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-741">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-742">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-743">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-744">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-745">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-746">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-747">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-748">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-749">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-750">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-751">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-752">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-753">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-753">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-754">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-755">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-756">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-757">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-758">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-759">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-760">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-761">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-762">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-763">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-764">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-765">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-766">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-767">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-768">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-769">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-770">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-771">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-772">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-773">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-774">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-775">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-776">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-777">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-778">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-779">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-780">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-781">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-782">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="110b2-783">DXGI_FORMAT_R16G16B16A16 \_ Снорм<sup>ФНС</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="110b2-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="110b2-784">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-784">Target</span></span> | <span data-ttu-id="110b2-785">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-785">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-786">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-787">64</span><span class="sxs-lookup"><span data-stu-id="110b2-787">64</span></span> |
| <span data-ttu-id="110b2-788">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-788">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-790">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-790">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-791">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-791">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-793">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-794">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-795">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-796">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-797">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-798">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-799">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-800">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-801">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-802">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-803">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-804">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-805">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-805">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-806">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-807">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-808">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-809">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-810">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-811">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-812">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-813">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-814">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-815">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-816">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-817">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-818">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-819">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-820">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-821">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-822">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-823">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-824">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-825">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-826">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-827">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-828">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-829">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-830">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-831">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-832">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-833">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-834">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="110b2-835">DXGI_FORMAT_R16G16B16A16 \_ Синт<sup>ФНС</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="110b2-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="110b2-836">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-836">Target</span></span> | <span data-ttu-id="110b2-837">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-837">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-838">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-839">64</span><span class="sxs-lookup"><span data-stu-id="110b2-839">64</span></span> |
| <span data-ttu-id="110b2-840">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-840">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-842">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-842">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-843">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-843">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-845">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-846">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-847">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-848">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-849">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-850">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-851">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-852">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-853">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-854">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-855">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-856">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-857">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-857">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-858">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-859">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-860">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-861">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-862">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-863">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-864">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-865">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-866">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-867">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-868">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-869">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-870">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-871">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-872">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-873">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-874">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-875">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-876">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-877">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-878">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-879">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-880">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-881">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-882">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-883">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-884">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-885">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-886">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="110b2-887">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32 (15)</span><span class="sxs-lookup"><span data-stu-id="110b2-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="110b2-888">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-888">Target</span></span> | <span data-ttu-id="110b2-889">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-889">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-890">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-891">64</span><span class="sxs-lookup"><span data-stu-id="110b2-891">64</span></span> |
| <span data-ttu-id="110b2-892">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-892">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-893">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-893">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-894">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-895">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-896">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-897">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-898">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-899">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-900">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-901">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-902">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-903">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-904">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-905">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-906">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-907">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-908">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-909">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-910">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-911">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-912">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-913">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-914">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-915">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-916">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-917">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-918">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-919">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-920">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-921">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-922">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-923">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-924">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-925">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-926">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-927">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-928">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-929">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-930">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-931">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-932">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-933">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-934">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-935">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-936">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="110b2-937">DXGI_FORMAT_R32G32 \_ float<sup>ФНС</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="110b2-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="110b2-938">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-938">Target</span></span> | <span data-ttu-id="110b2-939">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-939">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-940">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-941">64</span><span class="sxs-lookup"><span data-stu-id="110b2-941">64</span></span> |
| <span data-ttu-id="110b2-942">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-942">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-944">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-944">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-945">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-945">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-947">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-948">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-949">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-950">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-951">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-952">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-953">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-954">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-955">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-956">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-957">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-958">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-959">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-959">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-960">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-961">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-962">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-963">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-964">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-965">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-966">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-967">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-968">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-969">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-970">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-971">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-972">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-973">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-974">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-975">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-976">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-977">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-978">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-979">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-980">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-981">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-982">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-983">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-984">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-985">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-986">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-987">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-988">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="110b2-989">DXGI_FORMAT_R32G32 \_ uint<sup>ФНС</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="110b2-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="110b2-990">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-990">Target</span></span> | <span data-ttu-id="110b2-991">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-991">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-992">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-993">64</span><span class="sxs-lookup"><span data-stu-id="110b2-993">64</span></span> |
| <span data-ttu-id="110b2-994">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-994">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-995">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-995">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-996">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-997">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-998">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-999">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1003">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1004">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1005">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1006">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1007">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1008">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1009">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1010">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1011">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1012">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1013">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1014">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1015">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1016">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1017">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1018">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1019">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1020">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1021">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1022">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1023">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1024">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1025">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1026">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1027">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1028">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1029">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1030">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1031">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1032">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1033">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1034">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1035">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1036">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1037">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1038">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="110b2-1039">DXGI_FORMAT_R32G32 \_ Синт<sup>ФНС</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="110b2-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="110b2-1040">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1040">Target</span></span> | <span data-ttu-id="110b2-1041">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1042">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1043">64</span><span class="sxs-lookup"><span data-stu-id="110b2-1043">64</span></span> |
| <span data-ttu-id="110b2-1044">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1044">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1045">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1045">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1046">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1047">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1048">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1053">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1054">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1055">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1056">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1057">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1058">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1059">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1060">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1061">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1062">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1063">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1064">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1065">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1066">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1067">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1068">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1069">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1070">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1071">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1072">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1073">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1074">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1075">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1076">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1077">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1078">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1079">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1080">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1081">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1082">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1083">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1084">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1085">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1086">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1087">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1088">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="110b2-1089">DXGI_FORMAT_R32G8X24 \_ <sup>ПК</sup> нетипизированного типа (19)</span><span class="sxs-lookup"><span data-stu-id="110b2-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="110b2-1090">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1090">Target</span></span> | <span data-ttu-id="110b2-1091">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1092">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1093">64</span><span class="sxs-lookup"><span data-stu-id="110b2-1093">64</span></span> |
| <span data-ttu-id="110b2-1094">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1094">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1095">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1095">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1096">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1097">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1098">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1103">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1104">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1105">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1106">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1107">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1108">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1110">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1111">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1112">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1113">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1114">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1115">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1116">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1117">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1118">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1119">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1120">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1121">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1122">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1123">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1124">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1125">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1126">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1127">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1128">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1129">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1130">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1131">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1132">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1133">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1134">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1135">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1136">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1137">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1138">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="110b2-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>ФНС</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="110b2-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="110b2-1140">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1140">Target</span></span> | <span data-ttu-id="110b2-1141">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1142">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1143">64</span><span class="sxs-lookup"><span data-stu-id="110b2-1143">64</span></span> |
| <span data-ttu-id="110b2-1144">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1144">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1145">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1145">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1146">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1147">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1148">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1153">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1154">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1155">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1156">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1157">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1158">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1160">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1161">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1162">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1163">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1164">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1165">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1166">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1167">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1168">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1169">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1170">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1171">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1172">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1173">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1174">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1175">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1176">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1177">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1178">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1179">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1180">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1181">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1182">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1183">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1184">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1185">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1186">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1187">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1188">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="110b2-1189">DXGI_FORMAT_R32 \_ \_ ФНС с типом float X8X24 \_ (21)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="110b2-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="110b2-1190">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1190">Target</span></span> | <span data-ttu-id="110b2-1191">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1192">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1193">64</span><span class="sxs-lookup"><span data-stu-id="110b2-1193">64</span></span> |
| <span data-ttu-id="110b2-1194">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1194">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1195">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1195">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1196">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1197">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1198">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1203">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1204">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1205">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1206">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1207">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1208">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1209">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1210">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1211">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1212">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1213">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1214">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1215">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1216">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1217">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1218">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1219">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1220">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1221">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1222">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1223">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1224">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1225">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1226">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1227">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1228">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1229">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1230">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1231">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1232">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1233">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1234">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1235">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1236">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1237">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1238">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="110b2-1239">DXGI_FORMAT_X32 без \_ типа \_ G8X24 \_ uint<sup>ФНС</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="110b2-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="110b2-1240">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1240">Target</span></span> | <span data-ttu-id="110b2-1241">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1242">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1243">64</span><span class="sxs-lookup"><span data-stu-id="110b2-1243">64</span></span> |
| <span data-ttu-id="110b2-1244">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1244">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1245">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1245">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1246">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1247">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1248">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1253">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1254">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1255">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1256">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1257">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1258">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1260">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1261">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1262">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1263">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1264">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1265">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1266">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1267">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1268">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1269">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1270">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1271">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1272">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1273">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1274">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1275">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1276">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1277">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1278">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1279">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1280">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1281">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1282">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1283">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1284">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1285">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1286">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1287">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1288">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="110b2-1289">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R10G10B10A2 (23)</span><span class="sxs-lookup"><span data-stu-id="110b2-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="110b2-1290">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1290">Target</span></span> | <span data-ttu-id="110b2-1291">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1292">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1293">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1293">32</span></span> |
| <span data-ttu-id="110b2-1294">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1294">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1295">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1295">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1296">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1297">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1298">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1303">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1304">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1305">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1306">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1307">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1308">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1309">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1310">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1311">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1312">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1313">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1314">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1315">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1316">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1317">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1318">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1319">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1320">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1321">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1322">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1323">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1324">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1325">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1326">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1327">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1328">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1329">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1330">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1331">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1332">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1333">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1334">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1335">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1336">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1337">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1338">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="110b2-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>ФНС</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="110b2-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="110b2-1340">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1340">Target</span></span> | <span data-ttu-id="110b2-1341">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1342">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1343">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1343">32</span></span> |
| <span data-ttu-id="110b2-1344">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1344">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1345">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1345">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1346">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1347">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1348">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1353">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1354">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1355">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1356">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1357">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1358">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1359">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1360">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1361">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1362">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1363">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1364">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1365">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1366">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1367">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1368">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1369">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1370">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1371">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1372">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1373">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1374">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1375">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1376">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1377">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1378">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1379">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1380">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1381">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1382">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1383">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1384">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1385">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1386">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1387">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1387">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1389">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="110b2-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>ФНС</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="110b2-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="110b2-1391">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1391">Target</span></span> | <span data-ttu-id="110b2-1392">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1393">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1394">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1394">32</span></span> |
| <span data-ttu-id="110b2-1395">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1395">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1396">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1396">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1397">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1398">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1399">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1404">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1405">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1406">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1407">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1408">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1409">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1410">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1411">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1412">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1413">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1414">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1415">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1416">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1417">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1418">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1419">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1420">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1421">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1422">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1423">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1424">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1425">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1426">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1427">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1428">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1429">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1430">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1431">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1432">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1433">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1434">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1435">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1436">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1437">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1438">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1439">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="110b2-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ смещение \_ a2 \_ UNORM<sup>ФНС</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="110b2-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="110b2-1441">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1441">Target</span></span> | <span data-ttu-id="110b2-1442">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1443">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1444">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1444">32</span></span> |
| <span data-ttu-id="110b2-1445">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1445">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1446">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1446">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1447">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1448">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1449">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1454">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1455">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1456">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1457">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1458">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1459">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1461">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1462">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1463">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1464">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1465">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1466">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1467">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1468">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1469">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1470">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1471">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1472">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1473">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1474">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1475">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1476">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1477">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1478">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1479">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1480">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1481">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1482">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1483">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1484">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1485">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1486">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1487">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1488">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1489">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="110b2-1490">DXGI_FORMAT_R11G11B10 \_ <sup>ФНС</sup> с плавающей запятой (26)</span><span class="sxs-lookup"><span data-stu-id="110b2-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="110b2-1491">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1491">Target</span></span> | <span data-ttu-id="110b2-1492">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1493">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1494">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1494">32</span></span> |
| <span data-ttu-id="110b2-1495">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1495">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1496">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1496">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1497">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1498">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1499">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1504">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1505">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1506">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1507">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1508">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1509">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1511">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1512">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1513">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1514">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1515">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1516">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1517">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1518">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1519">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1520">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1521">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1522">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1523">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1524">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1525">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1526">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1527">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1528">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1529">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1530">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1531">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1532">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1533">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1534">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1535">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1536">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1537">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1538">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1539">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="110b2-1540">DXGI_FORMAT_R8G8B8A8 \_ <sup>ПК</sup> нетипизированных типов (27)</span><span class="sxs-lookup"><span data-stu-id="110b2-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="110b2-1541">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1541">Target</span></span> | <span data-ttu-id="110b2-1542">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1543">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1544">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1544">32</span></span> |
| <span data-ttu-id="110b2-1545">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1545">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1546">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1546">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1547">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1548">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1549">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1554">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1555">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1556">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1557">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1558">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1559">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1560">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1561">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1562">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1563">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1564">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1565">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1566">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1567">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1568">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1569">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1570">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1571">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1572">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1573">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1574">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1575">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1576">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1577">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1578">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1579">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1580">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1581">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1582">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1583">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1584">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1585">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1586">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1587">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1588">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1589">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="110b2-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>ФНС</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="110b2-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="110b2-1591">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1591">Target</span></span> | <span data-ttu-id="110b2-1592">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1593">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1594">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1594">32</span></span> |
| <span data-ttu-id="110b2-1595">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1595">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1597">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1597">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1598">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1598">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1600">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1601">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1603">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1605">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1607">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1609">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1609">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1611">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1611">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1613">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1614">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1615">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1616">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1617">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1619">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1619">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1621">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1621">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1623">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1623">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1625">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1626">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1627">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1628">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1629">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1630">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1631">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1632">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1633">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1634">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1635">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1636">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1637">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1638">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1638">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1640">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1640">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1642">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1642">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1644">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1644">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1646">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1646">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1648">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1649">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1649">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1651">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1652">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1653">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1653">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1655">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1655">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1657">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1657">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1659">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="110b2-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>ФНС</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="110b2-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="110b2-1661">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1661">Target</span></span> | <span data-ttu-id="110b2-1662">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1663">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1664">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1664">32</span></span> |
| <span data-ttu-id="110b2-1665">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1665">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1667">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1667">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1668">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1669">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1670">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1672">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1674">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1676">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1678">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1678">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1680">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1680">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1682">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1683">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1684">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1685">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1686">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1686">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1688">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1688">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1690">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1690">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1692">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1692">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1694">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1695">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1696">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1697">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1698">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1699">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1700">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1701">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1702">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1703">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1704">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1705">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1706">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1707">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1707">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1709">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1709">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1711">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1711">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1713">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1713">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1715">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1715">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1717">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1718">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1718">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1720">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1721">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1722">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1722">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-1724">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1724">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1726">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1726">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1728">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="110b2-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>ФНС</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="110b2-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="110b2-1730">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1730">Target</span></span> | <span data-ttu-id="110b2-1731">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1732">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1733">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1733">32</span></span> |
| <span data-ttu-id="110b2-1734">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1734">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1736">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1736">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1737">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1737">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1739">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1740">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1745">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1746">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1747">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1748">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1749">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1750">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1751">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1752">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1753">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1754">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1755">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1756">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1757">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1758">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1759">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1760">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1761">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1762">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1763">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1764">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1765">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1766">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1767">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1768">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1769">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1770">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1771">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1772">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1773">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1774">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1775">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1776">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1777">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1778">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1779">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1780">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="110b2-1781">DXGI_FORMAT_R8G8B8A8 \_ Снорм<sup>ФНС</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="110b2-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="110b2-1782">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1782">Target</span></span> | <span data-ttu-id="110b2-1783">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1784">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1785">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1785">32</span></span> |
| <span data-ttu-id="110b2-1786">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1786">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1788">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1788">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1789">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1790">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1791">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1793">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1796">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1798">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1798">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1800">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1800">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1802">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1803">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1804">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1805">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1806">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1808">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1809">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1810">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1811">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1812">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1813">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1814">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1815">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1816">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1817">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1818">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1819">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1820">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1821">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1822">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1823">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1824">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1824">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-1826">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1827">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1828">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1829">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1830">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1831">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1832">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1833">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1834">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1835">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1836">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1837">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="110b2-1838">DXGI_FORMAT_R8G8B8A8 \_ Синт<sup>фнс</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="110b2-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="110b2-1839">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1839">Target</span></span> | <span data-ttu-id="110b2-1840">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1841">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1842">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1842">32</span></span> |
| <span data-ttu-id="110b2-1843">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1843">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1844">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1844">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1845">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1846">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1847">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1852">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1853">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1854">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1855">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1856">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1857">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1859">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1860">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1861">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1862">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1863">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1864">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1865">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1866">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1867">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1868">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1869">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1870">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1871">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1872">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1873">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1874">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1875">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1876">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1877">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1878">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1879">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1880">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1881">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1882">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1883">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1884">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1885">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1886">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1887">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="110b2-1888">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16G16 (33)</span><span class="sxs-lookup"><span data-stu-id="110b2-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="110b2-1889">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1889">Target</span></span> | <span data-ttu-id="110b2-1890">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1891">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1892">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1892">32</span></span> |
| <span data-ttu-id="110b2-1893">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1893">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1894">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1894">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1895">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1896">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1897">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1902">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1903">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1904">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1905">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1906">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1907">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1908">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1909">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1910">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1911">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1912">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1913">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1914">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1915">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1916">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1917">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1918">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1919">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1920">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1921">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1922">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1923">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1924">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1925">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1926">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1927">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1928">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1929">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1930">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1931">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1932">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1933">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1934">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1935">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1936">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1937">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="110b2-1938">DXGI_FORMAT_R16G16 \_ float<sup>фнс</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="110b2-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="110b2-1939">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1939">Target</span></span> | <span data-ttu-id="110b2-1940">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1941">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1942">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1942">32</span></span> |
| <span data-ttu-id="110b2-1943">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1943">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1944">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1944">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1945">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1946">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1947">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-1952">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-1953">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-1954">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-1955">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-1956">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-1957">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-1958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-1959">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-1960">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1961">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1962">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-1963">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-1964">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1965">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-1966">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-1967">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-1968">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-1969">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-1970">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-1971">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-1972">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-1973">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1974">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-1975">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-1976">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1977">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-1978">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-1979">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-1980">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-1981">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-1982">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-1983">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-1984">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-1985">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-1986">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-1987">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="110b2-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>фнс</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="110b2-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="110b2-1989">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-1989">Target</span></span> | <span data-ttu-id="110b2-1990">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-1991">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-1992">32</span><span class="sxs-lookup"><span data-stu-id="110b2-1992">32</span></span> |
| <span data-ttu-id="110b2-1993">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-1993">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-1994">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-1994">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1995">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1996">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1997">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2002">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2003">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2004">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2005">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2006">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2007">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2008">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2009">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2010">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2011">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2012">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2013">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2014">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2015">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2016">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2017">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2018">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2019">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2020">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2021">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2022">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2023">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2024">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2025">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2026">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2027">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2028">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2029">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2030">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2031">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2032">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2033">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2034">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2035">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2036">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2037">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="110b2-2038">DXGI_FORMAT_R16G16 \_ uint<sup>фнс</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="110b2-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="110b2-2039">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2039">Target</span></span> | <span data-ttu-id="110b2-2040">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2041">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2042">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2042">32</span></span> |
| <span data-ttu-id="110b2-2043">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2043">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2044">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2044">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2045">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2046">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2047">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2052">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2053">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2054">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2055">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2056">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2057">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2059">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2060">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2061">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2062">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2063">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2064">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2065">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2066">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2067">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2068">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2069">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2070">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2071">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2072">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2073">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2074">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2075">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2076">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2077">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2078">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2079">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2080">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2081">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2082">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2083">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2084">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2085">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2086">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2087">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="110b2-2088">DXGI_FORMAT_R16G16 \_ Снорм<sup>фнс</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="110b2-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="110b2-2089">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2089">Target</span></span> | <span data-ttu-id="110b2-2090">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2091">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2092">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2092">32</span></span> |
| <span data-ttu-id="110b2-2093">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2093">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2095">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2095">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2096">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2096">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2098">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2099">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2101">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2105">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2105">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2107">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2108">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2109">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2110">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2111">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2112">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2112">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2114">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2115">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2116">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2117">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2118">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2119">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2120">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2121">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2122">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2123">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2124">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2125">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2126">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2127">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2128">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2129">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2130">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2130">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2132">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2133">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2134">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2135">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2136">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2137">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2138">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2139">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2140">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2141">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2142">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2143">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="110b2-2144">DXGI_FORMAT_R16G16 \_ Синт<sup>фнс</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="110b2-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="110b2-2145">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2145">Target</span></span> | <span data-ttu-id="110b2-2146">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2147">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2148">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2148">32</span></span> |
| <span data-ttu-id="110b2-2149">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2149">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2151">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2151">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2152">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2152">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2154">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2155">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2160">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2161">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2162">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2163">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2164">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2165">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2167">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2168">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2169">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2170">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2171">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2172">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2173">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2174">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2175">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2176">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2177">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2178">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2179">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2180">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2181">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2182">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2183">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2184">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2185">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2186">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2187">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2188">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2189">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2190">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2191">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2192">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2193">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2194">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2195">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="110b2-2196">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32 (39)</span><span class="sxs-lookup"><span data-stu-id="110b2-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="110b2-2197">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2197">Target</span></span> | <span data-ttu-id="110b2-2198">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2199">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2200">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2200">32</span></span> |
| <span data-ttu-id="110b2-2201">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2201">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2202">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2202">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2203">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2204">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2205">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2210">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2211">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2212">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2213">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2214">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2215">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2216">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2217">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2218">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2219">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2220">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2221">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2222">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2223">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2224">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2225">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2226">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2227">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2228">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2229">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2230">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2231">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2232">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2233">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2234">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2235">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2236">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2237">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2238">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2239">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2240">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2241">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2242">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2243">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2244">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2245">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="110b2-2246">DXGI_FORMAT_D32 \_ float<sup>фнс</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="110b2-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="110b2-2247">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2247">Target</span></span> | <span data-ttu-id="110b2-2248">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2249">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2250">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2250">32</span></span> |
| <span data-ttu-id="110b2-2251">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2251">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2252">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2252">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2253">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2254">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2255">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2260">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2261">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2262">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2263">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2264">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2265">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2266">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2267">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2268">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2269">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2270">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2271">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2272">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2273">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2274">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2275">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2276">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2277">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2278">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2279">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2280">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2281">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2282">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2283">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2284">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2285">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2286">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2287">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2288">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2289">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2290">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2291">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2292">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2293">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2294">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2295">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="110b2-2296">DXGI_FORMAT_R32 \_ float<sup>фнс</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="110b2-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="110b2-2297">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2297">Target</span></span> | <span data-ttu-id="110b2-2298">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2299">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2300">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2300">32</span></span> |
| <span data-ttu-id="110b2-2301">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2301">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2303">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2303">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2304">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2304">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2306">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2307">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2312">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2313">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2314">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2315">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2316">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2317">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2318">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2319">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2320">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2321">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2322">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2323">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2324">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2325">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2326">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2327">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2328">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2329">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2330">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2331">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2332">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2333">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2334">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2335">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2336">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2337">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2338">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2339">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2340">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2341">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2342">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2343">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2344">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2345">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2346">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2347">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="110b2-2348">DXGI_FORMAT_R32 \_ uint<sup>фнс</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="110b2-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="110b2-2349">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2349">Target</span></span> | <span data-ttu-id="110b2-2350">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2351">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2352">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2352">32</span></span> |
| <span data-ttu-id="110b2-2353">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2353">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2354">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2354">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2355">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2356">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2357">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2362">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2363">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2364">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2365">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2366">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2367">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2368">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2369">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2370">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2371">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2372">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2373">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2374">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2375">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2376">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2377">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2378">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2379">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2380">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2381">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2382">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2383">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2384">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2385">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2386">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2387">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2388">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2389">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2390">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2391">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2392">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2393">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2394">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2395">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2396">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2397">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="110b2-2398">DXGI_FORMAT_R32 \_ Синт<sup>фнс</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="110b2-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="110b2-2399">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2399">Target</span></span> | <span data-ttu-id="110b2-2400">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2401">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2402">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2402">32</span></span> |
| <span data-ttu-id="110b2-2403">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2403">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2404">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2404">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2405">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2406">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2407">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2412">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2413">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2414">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2415">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2416">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2417">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2419">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2420">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2421">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2422">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2423">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2424">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2425">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2426">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2427">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2428">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2429">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2430">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2431">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2432">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2433">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2434">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2435">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2436">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2437">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2438">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2439">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2440">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2441">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2442">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2443">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2444">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2445">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2446">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2447">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="110b2-2448">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R24G8 (44)</span><span class="sxs-lookup"><span data-stu-id="110b2-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="110b2-2449">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2449">Target</span></span> | <span data-ttu-id="110b2-2450">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2451">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2452">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2452">32</span></span> |
| <span data-ttu-id="110b2-2453">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2453">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2454">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2454">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2455">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2456">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2457">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2462">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2463">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2464">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2465">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2466">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2467">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2469">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2470">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2471">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2472">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2473">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2474">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2475">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2476">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2477">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2478">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2479">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2480">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2481">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2482">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2483">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2484">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2485">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2486">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2487">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2488">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2489">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2490">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2491">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2492">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2493">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2494">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2495">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2496">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2497">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="110b2-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>ФНС</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="110b2-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="110b2-2499">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2499">Target</span></span> | <span data-ttu-id="110b2-2500">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2501">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2502">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2502">32</span></span> |
| <span data-ttu-id="110b2-2503">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2503">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2505">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2505">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2506">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2507">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2508">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2510">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2514">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2515">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2516">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2517">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2518">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2519">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2521">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2522">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2523">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2524">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2525">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2525">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2527">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2528">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2529">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2530">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2531">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2532">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2533">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2534">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2535">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2536">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2537">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2538">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2539">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2539">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-2541">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2541">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-2543">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2543">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-2545">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2546">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2547">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2548">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2549">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2550">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2551">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2552">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2553">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="110b2-2554">DXGI_FORMAT_R24 \_ UNORM \_ x8 \_ нетипизированный<sup>ФНС</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="110b2-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="110b2-2555">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2555">Target</span></span> | <span data-ttu-id="110b2-2556">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2557">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2558">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2558">32</span></span> |
| <span data-ttu-id="110b2-2559">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2559">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2560">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2560">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2561">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2562">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2563">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2568">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2569">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2570">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2571">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2572">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2573">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2574">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2575">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2576">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2577">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2578">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2579">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2580">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2581">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2582">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2583">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2584">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2585">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2586">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2587">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2588">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2589">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2590">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2591">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2592">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2593">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2594">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2595">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2596">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2597">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2598">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2599">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2600">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2601">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2602">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2603">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="110b2-2604">DXGI_FORMAT_X24 без \_ типа \_ G8 \_ UINT<sup>ФНС</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="110b2-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="110b2-2605">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2605">Target</span></span> | <span data-ttu-id="110b2-2606">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2607">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2608">32</span><span class="sxs-lookup"><span data-stu-id="110b2-2608">32</span></span> |
| <span data-ttu-id="110b2-2609">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2609">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2610">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2610">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2611">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2612">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2613">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2618">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2619">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2620">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2621">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2622">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2623">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2625">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2626">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2627">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2628">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2629">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2630">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2631">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2632">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2633">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2634">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2635">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2636">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2637">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2638">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2639">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2640">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2641">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2642">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2643">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2644">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2645">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2646">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2647">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2648">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2649">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2650">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2651">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2652">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2653">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="110b2-2654">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8G8 (48)</span><span class="sxs-lookup"><span data-stu-id="110b2-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="110b2-2655">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2655">Target</span></span> | <span data-ttu-id="110b2-2656">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2657">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2658">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2658">16</span></span> |
| <span data-ttu-id="110b2-2659">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2659">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2660">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2660">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2661">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2662">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2663">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2668">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2669">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2670">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2671">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2672">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2673">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2674">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2675">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2676">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2677">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2678">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2679">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2680">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2681">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2682">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2683">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2684">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2685">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2686">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2687">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2688">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2689">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2690">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2691">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2692">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2693">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2694">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2695">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2696">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2697">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2698">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2699">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2700">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2701">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2702">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2703">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="110b2-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>фнс</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="110b2-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="110b2-2705">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2705">Target</span></span> | <span data-ttu-id="110b2-2706">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2707">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2708">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2708">16</span></span> |
| <span data-ttu-id="110b2-2709">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2709">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2711">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2711">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2712">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2713">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2714">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2716">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2720">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2720">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2722">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2722">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2724">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2725">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2726">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2727">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2728">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2729">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2730">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2730">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2732">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2732">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2734">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2735">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2736">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2737">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2738">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2739">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2740">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2741">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2742">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2743">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2744">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2745">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2746">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2747">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2747">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2749">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2750">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2751">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2752">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2753">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2754">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2755">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2756">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2757">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2758">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2759">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2759">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2761">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="110b2-2762">DXGI_FORMAT_R8G8 \_ uint<sup>фнс</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="110b2-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="110b2-2763">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2763">Target</span></span> | <span data-ttu-id="110b2-2764">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2765">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2766">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2766">16</span></span> |
| <span data-ttu-id="110b2-2767">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2767">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2768">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2768">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2769">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2770">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2771">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2776">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2777">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2778">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2779">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2780">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2781">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2782">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2783">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2784">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2785">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2786">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2787">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2788">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2789">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2790">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2791">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2792">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2793">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2794">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2795">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2796">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2797">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2798">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2799">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2800">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2801">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2802">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2803">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2804">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2805">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2806">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2807">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2808">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2809">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2810">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2811">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="110b2-2812">DXGI_FORMAT_R8G8 \_ Снорм<sup>фнс</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="110b2-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="110b2-2813">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2813">Target</span></span> | <span data-ttu-id="110b2-2814">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2815">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2816">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2816">16</span></span> |
| <span data-ttu-id="110b2-2817">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2817">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2819">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2819">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2820">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2821">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2822">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2824">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2828">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2828">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2830">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2830">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2832">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2833">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2834">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2835">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2836">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2838">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2839">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2840">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2841">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2842">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2843">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2844">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2845">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2846">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2847">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2848">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2849">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2850">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2851">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2852">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2853">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2854">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2854">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-2856">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2857">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2858">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2859">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2860">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2861">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2862">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2863">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2864">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2865">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2866">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2867">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="110b2-2868">DXGI_FORMAT_R8G8 \_ Синт<sup>фнс</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="110b2-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="110b2-2869">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2869">Target</span></span> | <span data-ttu-id="110b2-2870">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2871">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2872">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2872">16</span></span> |
| <span data-ttu-id="110b2-2873">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2873">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2874">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2874">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2875">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2876">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2877">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2882">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2883">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2884">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2885">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2886">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2887">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2889">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2890">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2891">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2892">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2893">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2894">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2895">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2896">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2897">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2898">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2899">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2900">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2901">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2902">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2903">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2904">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2905">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2906">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2907">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2908">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2909">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2910">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2911">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2912">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2913">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2914">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2915">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2916">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2917">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="110b2-2918">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16 (53)</span><span class="sxs-lookup"><span data-stu-id="110b2-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="110b2-2919">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2919">Target</span></span> | <span data-ttu-id="110b2-2920">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2921">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2922">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2922">16</span></span> |
| <span data-ttu-id="110b2-2923">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2923">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2924">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2924">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2925">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2926">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2927">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2932">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2933">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2934">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2935">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2936">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2937">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2939">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2940">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2941">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2942">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2943">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2944">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2945">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2946">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2947">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2948">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2949">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-2950">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-2951">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-2952">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-2953">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2954">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-2955">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-2956">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2957">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2958">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-2959">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-2960">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-2961">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-2962">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-2963">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-2964">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-2965">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-2966">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-2967">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="110b2-2968">DXGI_FORMAT_R16 \_ float<sup>фнс</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="110b2-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="110b2-2969">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-2969">Target</span></span> | <span data-ttu-id="110b2-2970">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-2971">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-2972">16</span><span class="sxs-lookup"><span data-stu-id="110b2-2972">16</span></span> |
| <span data-ttu-id="110b2-2973">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-2973">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-2974">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-2974">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2975">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2976">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2977">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-2982">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-2983">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-2984">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-2985">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-2986">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-2987">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-2988">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-2989">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-2990">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2991">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-2992">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-2993">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-2994">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2995">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-2996">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-2997">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-2998">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-2999">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3000">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3001">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3002">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3003">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3004">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3005">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3006">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3007">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3008">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3009">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3010">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3011">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3012">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3013">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3014">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3015">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3016">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3017">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="110b2-3018">DXGI_FORMAT_D16 \_ UNORM<sup>фнс</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="110b2-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="110b2-3019">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3019">Target</span></span> | <span data-ttu-id="110b2-3020">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3021">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3022">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3022">16</span></span> |
| <span data-ttu-id="110b2-3023">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3023">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3025">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3025">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3026">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3027">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3028">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3030">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3034">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3035">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3036">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3037">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3038">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3039">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3040">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3041">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3042">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3043">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3044">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3045">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3045">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3047">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3048">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3049">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3050">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3051">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3052">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3053">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3054">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3055">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3056">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3057">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3058">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3059">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3059">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-3061">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3061">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-3063">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3063">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-3065">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3066">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3067">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3068">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3069">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3070">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3071">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3072">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3073">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="110b2-3074">DXGI_FORMAT_R16 \_ UNORM<sup>фнс</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="110b2-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="110b2-3075">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3075">Target</span></span> | <span data-ttu-id="110b2-3076">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3077">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3078">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3078">16</span></span> |
| <span data-ttu-id="110b2-3079">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3079">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3080">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3080">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3081">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3082">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3083">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3088">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3089">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3090">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3091">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3092">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3093">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3094">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3095">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3096">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3097">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3098">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3099">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3100">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3101">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3102">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3103">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3104">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3105">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3106">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3107">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3108">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3109">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3110">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3111">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3112">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3113">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3114">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3115">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3116">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3117">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3118">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3119">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3120">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3121">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3122">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3123">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="110b2-3124">DXGI_FORMAT_R16 \_ uint<sup>фнс</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="110b2-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="110b2-3125">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3125">Target</span></span> | <span data-ttu-id="110b2-3126">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3127">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3128">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3128">16</span></span> |
| <span data-ttu-id="110b2-3129">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3129">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3131">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3131">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3132">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3133">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3133">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3135">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3140">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3141">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3142">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3143">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3144">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3145">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3146">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3147">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3148">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3149">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3150">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3151">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3152">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3153">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3154">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3155">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3156">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3157">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3158">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3159">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3160">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3161">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3162">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3163">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3164">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3165">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3166">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3167">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3168">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3169">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3170">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3171">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3172">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3173">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3174">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3175">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="110b2-3176">DXGI_FORMAT_R16 \_ Снорм<sup>фнс</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="110b2-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="110b2-3177">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3177">Target</span></span> | <span data-ttu-id="110b2-3178">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3179">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3180">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3180">16</span></span> |
| <span data-ttu-id="110b2-3181">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3181">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3182">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3182">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3183">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3184">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3185">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3190">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3191">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3192">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3193">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3194">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3195">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3196">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3197">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3198">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3199">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3200">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3201">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3202">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3203">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3204">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3205">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3206">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3207">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3208">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3209">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3210">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3211">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3212">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3213">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3214">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3215">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3216">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3217">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3218">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3219">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3220">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3221">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3222">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3223">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3224">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3225">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="110b2-3226">DXGI_FORMAT_R16 \_ Синт<sup>фнс</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="110b2-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="110b2-3227">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3227">Target</span></span> | <span data-ttu-id="110b2-3228">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3229">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3230">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3230">16</span></span> |
| <span data-ttu-id="110b2-3231">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3231">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3232">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3232">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3233">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3234">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3235">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3240">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3241">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3242">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3243">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3244">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3245">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3246">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3247">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3248">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3249">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3250">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3251">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3252">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3253">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3254">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3255">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3256">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3257">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3258">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3259">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3260">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3261">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3262">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3263">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3264">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3265">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3266">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3267">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3268">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3269">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3270">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3271">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3272">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3273">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3274">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3275">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="110b2-3276">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8 (60)</span><span class="sxs-lookup"><span data-stu-id="110b2-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="110b2-3277">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3277">Target</span></span> | <span data-ttu-id="110b2-3278">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3279">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3280">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3280">8</span></span> |
| <span data-ttu-id="110b2-3281">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3281">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3282">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3282">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3283">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3284">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3285">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3290">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3291">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3292">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3293">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3294">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3295">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3297">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3298">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3299">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3300">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3301">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3302">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3303">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3304">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3305">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3306">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3307">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3308">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3309">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3310">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3311">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3312">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3313">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3314">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3315">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3316">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3317">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3318">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3319">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3320">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3321">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3322">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3323">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3324">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3325">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="110b2-3326">DXGI_FORMAT_R8 \_ UNORM<sup>фнс</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="110b2-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="110b2-3327">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3327">Target</span></span> | <span data-ttu-id="110b2-3328">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3329">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3330">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3330">8</span></span> |
| <span data-ttu-id="110b2-3331">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3331">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3333">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3333">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3334">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3335">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3336">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3338">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3340">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3342">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3344">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3344">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3346">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3346">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3348">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3349">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3350">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3351">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3352">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3352">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3354">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3355">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3355">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3357">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3357">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3359">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3360">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3361">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3362">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3363">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3364">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3365">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3366">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3367">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3368">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3369">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3370">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3371">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3372">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3372">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3374">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3375">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3376">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3377">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3378">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3379">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3380">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3381">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3382">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3383">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3384">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3384">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3386">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="110b2-3387">DXGI_FORMAT_R8 \_ uint<sup>фнс</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="110b2-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="110b2-3388">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3388">Target</span></span> | <span data-ttu-id="110b2-3389">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3390">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3391">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3391">8</span></span> |
| <span data-ttu-id="110b2-3392">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3392">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3393">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3393">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3394">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3395">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3396">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3401">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3402">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3403">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3404">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3405">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3406">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3408">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3409">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3410">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3411">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3412">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3413">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3414">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3415">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3416">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3417">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3418">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3419">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3420">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3421">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3422">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3423">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3424">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3425">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3426">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3427">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3428">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3429">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3430">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3431">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3432">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3433">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3434">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3435">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3436">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="110b2-3437">DXGI_FORMAT_R8 \_ Снорм<sup>фнс</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="110b2-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="110b2-3438">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3438">Target</span></span> | <span data-ttu-id="110b2-3439">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3440">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3441">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3441">8</span></span> |
| <span data-ttu-id="110b2-3442">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3442">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3443">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3443">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3444">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3445">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3446">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3451">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3452">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3453">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3454">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3455">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3456">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3458">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3459">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3460">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3461">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3462">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3463">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3464">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3465">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3466">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3467">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3468">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3469">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3470">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3471">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3472">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3473">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3474">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3475">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3476">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3477">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3478">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3479">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3480">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3481">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3482">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3483">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3484">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3485">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3486">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="110b2-3487">DXGI_FORMAT_R8 \_ Синт<sup>фнс</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="110b2-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="110b2-3488">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3488">Target</span></span> | <span data-ttu-id="110b2-3489">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3490">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3491">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3491">8</span></span> |
| <span data-ttu-id="110b2-3492">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3492">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3493">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3493">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3494">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3495">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3496">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3501">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3502">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3503">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3504">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3505">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3506">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3507">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3508">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3509">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3510">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3511">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3512">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3513">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3514">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3515">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3516">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3517">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3518">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3519">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3520">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3521">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3522">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3523">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3524">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3525">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3526">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3527">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3528">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3529">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3530">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3531">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3532">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3533">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3534">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3535">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3536">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="110b2-3537">DXGI_FORMAT_A8 \_ UNORM<sup>фнс</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="110b2-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="110b2-3538">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3538">Target</span></span> | <span data-ttu-id="110b2-3539">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3540">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3541">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3541">8</span></span> |
| <span data-ttu-id="110b2-3542">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3542">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3544">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3544">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3545">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3546">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3547">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3549">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3553">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3553">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3555">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3555">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3557">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3558">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3559">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3560">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3562">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3563">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3563">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3565">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3565">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3567">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3568">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3569">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3570">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3571">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3572">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3573">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3574">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3575">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3576">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3577">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3578">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3579">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3580">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3580">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3582">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3583">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3584">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3585">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3586">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3587">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3588">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3589">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3590">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3591">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3592">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3592">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3594">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="110b2-3595">DXGI_FORMAT_R9G9B9E5 \_ Шаредексп<sup>фнк</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="110b2-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="110b2-3596">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3596">Target</span></span> | <span data-ttu-id="110b2-3597">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3598">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3599">32</span><span class="sxs-lookup"><span data-stu-id="110b2-3599">32</span></span> |
| <span data-ttu-id="110b2-3600">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3600">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3601">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3601">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3602">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3603">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3604">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3609">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3610">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3611">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3612">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3613">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3614">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3616">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3617">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3618">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3619">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3620">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3621">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3622">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3623">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3624">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3625">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3626">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3627">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3628">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3629">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3630">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3631">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3632">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3633">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3634">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3635">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3636">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3637">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3638">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3639">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3640">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3641">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3642">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3643">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3644">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="110b2-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>ФНК</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="110b2-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="110b2-3646">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3646">Target</span></span> | <span data-ttu-id="110b2-3647">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3648">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3649">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3649">16</span></span> |
| <span data-ttu-id="110b2-3650">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3650">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3651">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3651">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3652">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3653">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3654">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3659">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3660">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3661">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3662">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3663">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3664">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3665">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3666">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3667">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3668">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3669">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3670">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3671">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3672">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3673">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3674">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3675">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3676">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3677">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3678">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3679">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3680">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3681">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3682">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3683">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3684">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3685">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3686">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3687">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3688">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3689">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3690">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3691">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3692">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3693">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3694">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="110b2-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>ФНК</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="110b2-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="110b2-3696">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3696">Target</span></span> | <span data-ttu-id="110b2-3697">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3698">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3699">16</span><span class="sxs-lookup"><span data-stu-id="110b2-3699">16</span></span> |
| <span data-ttu-id="110b2-3700">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3700">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3701">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3701">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3702">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3703">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3704">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3709">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3710">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3711">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3712">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3713">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3714">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3716">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3717">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3718">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3719">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3720">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3721">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3722">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3723">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3724">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3725">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3726">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3727">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3728">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3729">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3730">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3731">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3732">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3733">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3734">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3735">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3736">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3737">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3738">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3739">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3740">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3741">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3742">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3743">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3744">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="110b2-3745">DXGI_FORMAT_BC1 \_ нетипизированных<sup>пкк</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="110b2-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="110b2-3746">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3746">Target</span></span> | <span data-ttu-id="110b2-3747">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3748">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3749">4</span><span class="sxs-lookup"><span data-stu-id="110b2-3749">4</span></span> |
| <span data-ttu-id="110b2-3750">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3750">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3751">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3751">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3752">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3753">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3754">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3759">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3760">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3761">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3762">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3763">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3764">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3765">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3766">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3767">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3768">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3769">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3770">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3771">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3772">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3773">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3774">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3775">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3776">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3777">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3778">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3779">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3780">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3781">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3782">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3783">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3784">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3785">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3786">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3787">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3788">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3789">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3790">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3791">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3792">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3793">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3794">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="110b2-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>фнк</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="110b2-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="110b2-3796">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3796">Target</span></span> | <span data-ttu-id="110b2-3797">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3798">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3799">4</span><span class="sxs-lookup"><span data-stu-id="110b2-3799">4</span></span> |
| <span data-ttu-id="110b2-3800">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3800">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3802">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3802">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3803">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3804">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3805">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3807">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3810">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3812">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3812">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3814">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3814">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3816">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3817">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3818">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3819">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3820">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3820">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3822">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3823">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3824">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3825">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3826">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3827">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3828">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3829">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3830">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3831">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3832">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3833">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3834">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3835">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3836">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3837">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3838">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3838">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3840">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3841">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3842">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3843">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3844">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3845">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3846">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3847">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3848">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3849">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3850">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3850">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3852">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="110b2-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>ФНК</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="110b2-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="110b2-3854">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3854">Target</span></span> | <span data-ttu-id="110b2-3855">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3856">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3857">4</span><span class="sxs-lookup"><span data-stu-id="110b2-3857">4</span></span> |
| <span data-ttu-id="110b2-3858">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3858">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3860">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3860">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3861">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3862">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3863">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3865">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3868">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3870">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3870">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3872">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3872">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3874">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3875">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3876">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3877">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3878">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3878">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3880">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3881">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3882">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3883">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3884">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3885">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3886">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3887">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3888">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3889">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3890">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3891">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3892">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3893">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3894">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3895">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3896">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3896">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3898">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3899">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3900">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3901">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3902">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3903">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3904">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3905">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3906">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3907">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3908">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3908">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3910">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="110b2-3911">DXGI_FORMAT_BC2 \_ нетипизированных<sup>пкк</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="110b2-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="110b2-3912">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3912">Target</span></span> | <span data-ttu-id="110b2-3913">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3914">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3915">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3915">8</span></span> |
| <span data-ttu-id="110b2-3916">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3916">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-3917">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3917">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3918">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3919">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3920">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-3925">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-3926">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-3927">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3928">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3929">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3930">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3931">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-3932">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3933">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3934">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3935">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3936">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3937">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3938">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3939">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3940">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3941">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3942">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3943">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-3944">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-3945">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-3946">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3947">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-3948">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-3949">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3950">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3951">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-3952">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-3953">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-3954">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-3955">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-3956">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-3957">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-3958">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-3959">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-3960">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="110b2-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>фнк</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="110b2-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="110b2-3962">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-3962">Target</span></span> | <span data-ttu-id="110b2-3963">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-3964">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-3965">8</span><span class="sxs-lookup"><span data-stu-id="110b2-3965">8</span></span> |
| <span data-ttu-id="110b2-3966">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-3966">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3968">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-3968">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3969">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3970">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3971">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-3973">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-3976">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3978">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-3978">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3980">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-3980">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3982">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-3983">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-3984">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-3985">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-3986">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3986">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-3988">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-3989">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3990">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-3991">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-3992">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-3993">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3994">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-3995">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-3996">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-3997">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-3998">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-3999">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4000">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4001">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4002">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4003">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4004">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4004">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4006">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4007">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4008">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4009">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4010">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4011">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4012">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4013">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4014">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4015">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4016">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4016">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4018">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="110b2-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>ФНК</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="110b2-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="110b2-4020">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4020">Target</span></span> | <span data-ttu-id="110b2-4021">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4022">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4023">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4023">8</span></span> |
| <span data-ttu-id="110b2-4024">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4024">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4026">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4026">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4027">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4028">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4029">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4031">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4034">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4036">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4036">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4038">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4038">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4040">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4041">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4042">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4043">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4044">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4044">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4046">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4047">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4048">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4049">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4050">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4051">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4052">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4053">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4054">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4055">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4056">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4057">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4058">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4059">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4060">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4061">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4062">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4062">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4064">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4065">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4066">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4067">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4068">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4069">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4070">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4071">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4072">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4073">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4074">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4074">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4076">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="110b2-4077">DXGI_FORMAT_BC3 \_ нетипизированных<sup>пкк</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="110b2-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="110b2-4078">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4078">Target</span></span> | <span data-ttu-id="110b2-4079">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4080">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4081">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4081">8</span></span> |
| <span data-ttu-id="110b2-4082">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4082">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4083">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4083">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4084">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4085">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4086">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4091">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4092">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4093">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4094">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4095">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4096">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4097">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4098">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4099">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4100">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4101">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4102">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4103">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4104">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4105">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4106">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4107">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4108">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4109">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4110">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4111">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4112">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4113">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4114">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4115">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4116">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4117">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4118">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4119">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4120">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4121">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4122">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4123">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4124">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4125">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4126">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="110b2-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>фнк</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="110b2-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="110b2-4128">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4128">Target</span></span> | <span data-ttu-id="110b2-4129">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4130">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4131">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4131">8</span></span> |
| <span data-ttu-id="110b2-4132">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4132">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4134">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4134">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4135">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4136">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4137">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4139">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4142">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4144">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4144">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4146">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4146">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4148">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4149">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4150">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4151">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4152">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4154">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4155">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4156">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4157">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4158">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4159">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4160">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4161">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4162">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4163">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4164">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4165">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4166">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4167">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4168">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4169">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4170">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4170">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4172">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4173">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4174">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4175">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4176">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4177">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4178">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4179">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4180">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4181">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4182">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4182">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4184">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="110b2-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>ФНК</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="110b2-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="110b2-4186">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4186">Target</span></span> | <span data-ttu-id="110b2-4187">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4188">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4189">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4189">8</span></span> |
| <span data-ttu-id="110b2-4190">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4190">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4192">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4192">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4193">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4194">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4195">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4197">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4200">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4202">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4202">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4204">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4204">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4206">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4207">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4208">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4209">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4210">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4212">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4213">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4214">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4215">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4216">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4217">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4218">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4219">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4220">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4221">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4222">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4223">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4224">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4225">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4226">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4227">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4228">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4228">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4230">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4231">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4232">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4233">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4234">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4235">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4236">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4237">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4238">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4239">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4240">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4240">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4242">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="110b2-4243">DXGI_FORMAT_BC4 \_ нетипизированных<sup>пкк</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="110b2-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="110b2-4244">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4244">Target</span></span> | <span data-ttu-id="110b2-4245">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4246">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4247">4</span><span class="sxs-lookup"><span data-stu-id="110b2-4247">4</span></span> |
| <span data-ttu-id="110b2-4248">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4248">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4249">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4249">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4250">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4251">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4252">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4257">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4258">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4259">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4260">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4261">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4262">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4264">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4265">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4266">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4267">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4268">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4269">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4270">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4271">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4272">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4273">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4274">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4275">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4276">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4277">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4278">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4279">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4280">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4281">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4282">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4283">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4284">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4285">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4286">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4287">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4288">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4289">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4290">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4291">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4292">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="110b2-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>фнк</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="110b2-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="110b2-4294">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4294">Target</span></span> | <span data-ttu-id="110b2-4295">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4296">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4297">4</span><span class="sxs-lookup"><span data-stu-id="110b2-4297">4</span></span> |
| <span data-ttu-id="110b2-4298">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4298">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4299">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4299">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4300">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4301">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4302">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4307">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4308">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4309">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4310">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4311">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4312">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4313">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4314">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4315">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4316">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4317">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4318">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4319">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4320">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4321">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4322">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4323">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4324">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4325">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4326">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4327">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4328">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4329">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4330">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4331">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4332">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4333">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4334">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4335">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4336">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4337">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4338">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4339">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4340">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4341">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4342">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="110b2-4343">DXGI_FORMAT_BC4 \_ Снорм<sup>фнк</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="110b2-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="110b2-4344">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4344">Target</span></span> | <span data-ttu-id="110b2-4345">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4346">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4347">4</span><span class="sxs-lookup"><span data-stu-id="110b2-4347">4</span></span> |
| <span data-ttu-id="110b2-4348">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4348">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4349">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4349">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4350">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4351">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4352">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4357">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4358">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4359">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4360">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4361">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4362">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4363">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4364">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4365">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4366">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4367">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4368">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4369">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4370">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4371">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4372">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4373">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4374">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4375">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4376">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4377">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4378">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4379">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4380">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4381">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4382">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4383">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4384">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4385">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4386">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4387">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4388">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4389">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4390">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4391">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4392">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="110b2-4393">DXGI_FORMAT_BC5 \_ нетипизированных<sup>пкк</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="110b2-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="110b2-4394">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4394">Target</span></span> | <span data-ttu-id="110b2-4395">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4396">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4397">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4397">8</span></span> |
| <span data-ttu-id="110b2-4398">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4398">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4399">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4399">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4400">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4401">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4402">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4407">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4408">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4409">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4410">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4411">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4412">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4413">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4414">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4415">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4416">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4417">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4418">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4419">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4420">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4421">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4422">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4423">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4424">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4425">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4426">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4427">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4428">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4429">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4430">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4431">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4432">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4433">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4434">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4435">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4436">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4437">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4438">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4439">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4440">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4441">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4442">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="110b2-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>фнк</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="110b2-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="110b2-4444">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4444">Target</span></span> | <span data-ttu-id="110b2-4445">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4446">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4447">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4447">8</span></span> |
| <span data-ttu-id="110b2-4448">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4448">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4449">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4449">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4450">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4451">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4452">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4457">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4458">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4459">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4460">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4461">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4462">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4464">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4465">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4466">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4467">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4468">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4469">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4470">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4471">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4472">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4473">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4474">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4475">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4476">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4477">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4478">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4479">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4480">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4481">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4482">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4483">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4484">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4485">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4486">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4487">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4488">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4489">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4490">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4491">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4492">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="110b2-4493">DXGI_FORMAT_BC5 \_ Снорм<sup>фнк</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="110b2-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="110b2-4494">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4494">Target</span></span> | <span data-ttu-id="110b2-4495">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4496">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4497">8</span><span class="sxs-lookup"><span data-stu-id="110b2-4497">8</span></span> |
| <span data-ttu-id="110b2-4498">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4498">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4499">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4499">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4500">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4501">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4502">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4507">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4508">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4509">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4510">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4511">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4512">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4513">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4514">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4515">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4516">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4517">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4518">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4519">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4520">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4521">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4522">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4523">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4524">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4525">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4526">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4527">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4528">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4529">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4530">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4531">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4532">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4533">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4534">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4535">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4536">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4537">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4538">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4539">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4540">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4541">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4542">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="110b2-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>фнс</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="110b2-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="110b2-4544">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4544">Target</span></span> | <span data-ttu-id="110b2-4545">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4546">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4547">16</span><span class="sxs-lookup"><span data-stu-id="110b2-4547">16</span></span> |
| <span data-ttu-id="110b2-4548">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4548">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4550">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4550">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4551">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4552">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4553">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4555">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4558">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4560">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4560">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4562">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4562">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4564">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4565">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4566">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4567">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4568">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4568">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4570">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4570">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4572">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4572">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4574">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4574">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4576">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4577">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4578">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4579">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4580">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4581">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4582">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4583">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4584">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4585">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4586">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4587">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4588">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4589">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4589">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4591">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4591">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4593">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4593">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4595">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4595">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4597">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4597">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4599">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4600">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4601">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4602">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4603">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4604">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4605">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4606">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="110b2-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>фнс</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="110b2-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="110b2-4608">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4608">Target</span></span> | <span data-ttu-id="110b2-4609">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4610">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4611">16</span><span class="sxs-lookup"><span data-stu-id="110b2-4611">16</span></span> |
| <span data-ttu-id="110b2-4612">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4612">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4614">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4614">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4615">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4616">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4617">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4619">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4622">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4624">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4624">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4626">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4626">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4628">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4629">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4630">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4631">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4632">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4634">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4635">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4636">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4637">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4638">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4639">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4640">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4641">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4642">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4643">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4644">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4645">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4646">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4647">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4648">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4649">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4650">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4650">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4652">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4653">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4654">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4655">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4656">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4657">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4658">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4659">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4660">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4661">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4662">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4663">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="110b2-4664">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8A8 (90)</span><span class="sxs-lookup"><span data-stu-id="110b2-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="110b2-4665">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4665">Target</span></span> | <span data-ttu-id="110b2-4666">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4667">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4668">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4668">32</span></span> |
| <span data-ttu-id="110b2-4669">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4669">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4670">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4670">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4671">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4672">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4673">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4678">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4679">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4680">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4681">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4682">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4683">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4685">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4686">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4687">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4688">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4689">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4690">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4691">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4692">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4693">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4694">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4695">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4696">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4697">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4698">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4699">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4700">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4701">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4702">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4703">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4704">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4705">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4706">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4707">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4708">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4709">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4710">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4711">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4712">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4713">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="110b2-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>фнс</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="110b2-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="110b2-4715">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4715">Target</span></span> | <span data-ttu-id="110b2-4716">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4717">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4718">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4718">32</span></span> |
| <span data-ttu-id="110b2-4719">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4719">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4721">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4721">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4722">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4723">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4724">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4726">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4728">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4730">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4732">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4732">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4734">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4734">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4736">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4737">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4738">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4739">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4740">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4742">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4742">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4744">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4744">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4746">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4746">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4748">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4749">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4750">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4751">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4752">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4753">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4754">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4755">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4756">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4757">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4758">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4759">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4760">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4761">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4761">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4763">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4763">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4765">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4765">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4767">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4767">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4769">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4769">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4771">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4772">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4772">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4774">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4775">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4776">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4776">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4778">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4778">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4780">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4780">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4782">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="110b2-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>ФНС</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="110b2-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="110b2-4784">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4784">Target</span></span> | <span data-ttu-id="110b2-4785">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4786">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4787">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4787">32</span></span> |
| <span data-ttu-id="110b2-4788">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4788">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4790">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4790">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4791">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4792">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4793">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4795">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4797">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4799">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4801">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4801">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4803">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4803">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4805">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4806">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4807">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4808">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4809">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4809">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4811">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4811">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4813">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4813">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4815">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4815">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4817">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4818">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4819">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4820">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4821">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4822">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4823">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4824">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4825">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4826">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4827">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4828">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4829">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4830">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4830">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4832">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4832">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4834">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4834">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4836">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4836">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4838">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4838">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4840">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4841">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4841">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4843">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4844">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4845">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4845">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4847">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4847">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4849">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4849">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4851">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="110b2-4852">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8X8 (92)</span><span class="sxs-lookup"><span data-stu-id="110b2-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="110b2-4853">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4853">Target</span></span> | <span data-ttu-id="110b2-4854">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4855">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4856">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4856">32</span></span> |
| <span data-ttu-id="110b2-4857">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4857">Format Support</span></span> | \- |
| <span data-ttu-id="110b2-4858">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4858">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4859">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4860">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4861">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="110b2-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-4866">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-4867">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-4868">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4869">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4870">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4871">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-4873">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-4874">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4875">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4876">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4877">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4878">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4879">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4880">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4881">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4882">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4883">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4884">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4885">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4886">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4887">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4888">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4889">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-4890">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4891">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-4892">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-4893">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-4894">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4895">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4896">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4897">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4898">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-4899">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-4900">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-4901">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="110b2-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>фнс</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="110b2-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="110b2-4903">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4903">Target</span></span> | <span data-ttu-id="110b2-4904">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4905">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4906">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4906">32</span></span> |
| <span data-ttu-id="110b2-4907">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4907">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4909">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4909">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4910">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4911">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4912">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4914">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4916">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4918">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4920">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4920">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4922">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4922">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4924">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4925">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4926">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4927">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4928">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4928">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4930">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4930">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4932">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4932">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4934">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-4934">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4936">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-4937">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-4938">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4939">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-4940">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-4941">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-4942">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-4943">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-4944">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-4945">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-4946">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-4947">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4948">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-4949">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-4949">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4951">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4951">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4953">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-4953">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4955">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-4955">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4957">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-4957">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4959">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-4960">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-4961">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-4962">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-4963">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4963">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4965">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-4965">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-4967">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4967">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4969">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="110b2-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>ФНС</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="110b2-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="110b2-4971">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-4971">Target</span></span> | <span data-ttu-id="110b2-4972">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-4973">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-4974">32</span><span class="sxs-lookup"><span data-stu-id="110b2-4974">32</span></span> |
| <span data-ttu-id="110b2-4975">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-4975">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4977">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-4977">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4978">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4979">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4980">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-4982">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-4984">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-4986">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4988">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-4988">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4990">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-4990">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4992">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-4993">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-4994">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-4995">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-4996">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4996">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-4998">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-4998">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5000">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5000">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5002">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5002">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5004">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5005">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5006">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5007">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5008">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5009">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5010">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5011">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5012">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5013">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5014">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5015">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5016">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5017">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5017">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5019">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5019">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5021">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5021">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5023">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5023">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5025">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5025">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5027">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5028">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5029">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5030">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5031">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-5032">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5033">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5033">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5035">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="110b2-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="110b2-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="110b2-5037">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5037">Target</span></span> | <span data-ttu-id="110b2-5038">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5039">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5040">32</span><span class="sxs-lookup"><span data-stu-id="110b2-5040">32</span></span> |
| <span data-ttu-id="110b2-5041">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5041">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5043">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5043">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5044">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5045">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5046">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5048">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5052">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5053">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5054">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5055">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5056">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5057">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5059">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5060">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5061">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5062">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5063">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5064">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5065">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5066">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5067">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5068">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5069">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5070">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5071">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5072">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5073">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5074">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5075">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5075">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5077">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5078">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5079">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5080">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5081">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5082">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5083">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5084">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5084">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5086">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5086">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5088">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5088">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5090">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5091">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="110b2-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="110b2-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="110b2-5093">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5093">Target</span></span> | <span data-ttu-id="110b2-5094">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5095">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5096">32</span><span class="sxs-lookup"><span data-stu-id="110b2-5096">32</span></span> |
| <span data-ttu-id="110b2-5097">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5097">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5099">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5099">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5100">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5101">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5102">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5104">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5108">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5109">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5110">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5111">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5112">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5113">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5114">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5115">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5116">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5117">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5118">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5119">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5120">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5121">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5122">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5123">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5124">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5125">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5126">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5127">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5128">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5129">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5130">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5131">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5131">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5133">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5134">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5135">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5136">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5137">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5138">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5139">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5140">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5140">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5142">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5142">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5144">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5144">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5146">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5147">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="110b2-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="110b2-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="110b2-5149">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5149">Target</span></span> | <span data-ttu-id="110b2-5150">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5151">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5152">64</span><span class="sxs-lookup"><span data-stu-id="110b2-5152">64</span></span> |
| <span data-ttu-id="110b2-5153">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5153">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5155">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5155">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5156">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5157">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5158">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5160">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5164">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5165">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5166">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5167">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5168">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5169">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5170">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5171">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5172">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5173">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5174">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5175">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5176">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5177">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5178">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5179">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5180">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5181">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5182">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5183">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5184">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5185">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5186">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5187">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5187">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5189">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5190">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5191">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5192">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5193">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5194">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5195">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5196">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5196">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5198">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5198">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5200">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5200">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5202">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5203">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="110b2-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="110b2-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="110b2-5205">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5205">Target</span></span> | <span data-ttu-id="110b2-5206">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5207">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5208">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5208">8</span></span> |
| <span data-ttu-id="110b2-5209">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5209">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5211">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5211">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5212">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5213">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5214">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5216">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5220">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5221">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5222">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5223">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5224">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5225">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5227">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5228">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5229">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5230">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5231">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5232">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5233">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5234">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5235">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5236">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5237">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5238">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5239">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5240">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5241">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5242">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5243">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5243">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5245">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5246">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5247">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5248">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5249">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5250">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5251">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5252">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5252">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5254">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5254">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5256">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5256">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5258">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5259">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="110b2-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="110b2-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="110b2-5261">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5261">Target</span></span> | <span data-ttu-id="110b2-5262">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5263">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5264">16</span><span class="sxs-lookup"><span data-stu-id="110b2-5264">16</span></span> |
| <span data-ttu-id="110b2-5265">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5265">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5267">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5267">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5268">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5269">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5270">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5272">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5276">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5277">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5278">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5279">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5280">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5281">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5283">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5284">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5285">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5286">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5287">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5288">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5289">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5290">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5291">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5292">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5293">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5294">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5295">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5296">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5297">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5298">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5299">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5299">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5301">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5302">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5303">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5304">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5305">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5306">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5307">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5308">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5308">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5310">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5310">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5312">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5312">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5314">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5315">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="110b2-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="110b2-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="110b2-5317">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5317">Target</span></span> | <span data-ttu-id="110b2-5318">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5319">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5320">16</span><span class="sxs-lookup"><span data-stu-id="110b2-5320">16</span></span> |
| <span data-ttu-id="110b2-5321">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5321">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5323">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5323">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5324">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5325">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5326">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5328">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5332">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5333">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5334">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5335">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5336">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5337">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5339">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5340">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5341">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5342">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5343">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5344">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5345">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5346">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5347">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5348">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5349">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5350">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5351">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5352">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5353">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5354">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5355">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5355">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5357">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5358">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5359">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5360">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5361">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5362">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5363">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5364">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5364">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5366">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5366">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5368">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5368">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5370">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5371">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="110b2-5372">DXGI_FORMAT_420 \_ непрозрачный<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="110b2-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="110b2-5373">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5373">Target</span></span> | <span data-ttu-id="110b2-5374">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5375">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5376">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5376">8</span></span> |
| <span data-ttu-id="110b2-5377">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5377">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5379">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5379">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5380">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5381">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5382">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5384">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5388">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5389">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5390">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5391">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5392">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5393">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5394">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5395">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5396">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5397">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5398">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5399">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5400">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5401">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5402">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5403">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5404">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5405">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5406">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5407">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5408">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5409">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5410">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5411">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="110b2-5412">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5413">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5414">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5415">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5416">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5417">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5418">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5419">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5419">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5421">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5421">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5423">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5423">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5425">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5426">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="110b2-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="110b2-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="110b2-5428">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5428">Target</span></span> | <span data-ttu-id="110b2-5429">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5430">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5431">16</span><span class="sxs-lookup"><span data-stu-id="110b2-5431">16</span></span> |
| <span data-ttu-id="110b2-5432">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5432">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5434">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5434">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5435">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5436">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5437">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5439">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5443">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5444">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5445">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5446">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5447">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5448">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5449">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5450">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5451">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5452">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5453">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5454">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5455">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5456">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5457">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5458">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5459">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5460">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5461">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5462">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5463">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5464">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5465">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5466">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5466">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5468">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5469">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5470">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5471">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5472">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5473">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5474">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5475">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5475">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5477">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5477">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5479">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5479">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5481">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5482">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="110b2-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="110b2-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="110b2-5484">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5484">Target</span></span> | <span data-ttu-id="110b2-5485">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5486">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5487">32</span><span class="sxs-lookup"><span data-stu-id="110b2-5487">32</span></span> |
| <span data-ttu-id="110b2-5488">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5488">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5490">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5490">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5491">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5492">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5493">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5495">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5499">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5500">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5501">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5502">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5503">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5504">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5505">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5506">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5507">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5508">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5509">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5510">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5511">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5512">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5513">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5514">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5515">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5516">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5517">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5518">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5519">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5520">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5521">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5522">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5522">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5524">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5525">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5526">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5527">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5528">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5529">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5530">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5531">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5531">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5533">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5533">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5535">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5535">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5537">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5538">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="110b2-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="110b2-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="110b2-5540">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5540">Target</span></span> | <span data-ttu-id="110b2-5541">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5542">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5543">32</span><span class="sxs-lookup"><span data-stu-id="110b2-5543">32</span></span> |
| <span data-ttu-id="110b2-5544">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5544">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5546">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5546">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5547">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5548">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5549">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5551">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5555">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5556">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5557">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5558">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5559">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5560">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5562">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5563">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5564">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5565">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5566">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5567">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5568">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5569">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5570">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5571">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5572">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5573">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5574">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5575">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5576">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5577">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5578">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5578">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5580">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5581">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5582">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5583">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5584">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5585">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5586">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5587">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5587">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5589">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5589">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5591">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5591">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5593">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5594">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="110b2-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="110b2-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="110b2-5596">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5596">Target</span></span> | <span data-ttu-id="110b2-5597">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5598">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5599">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5599">8</span></span> |
| <span data-ttu-id="110b2-5600">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5600">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5602">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5602">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5603">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5604">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5605">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5607">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5611">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5612">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5613">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5614">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5615">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5616">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5618">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5619">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5620">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5621">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5622">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5623">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5624">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5625">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5626">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5627">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5628">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5629">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5630">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5631">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5632">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5633">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5634">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5634">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5636">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5637">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5638">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5639">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5640">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5641">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5642">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5643">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5643">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5645">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5645">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5647">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5647">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5649">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5650">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="110b2-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="110b2-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="110b2-5652">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5652">Target</span></span> | <span data-ttu-id="110b2-5653">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5654">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5655">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5655">8</span></span> |
| <span data-ttu-id="110b2-5656">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5656">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5658">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5658">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5659">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5660">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5661">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5663">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5667">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5668">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5669">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5670">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5671">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5672">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5673">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5674">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5675">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5676">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5677">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5678">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5679">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5680">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5681">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5682">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5683">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5684">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5685">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5686">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5687">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5688">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5689">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5690">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5690">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5692">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5693">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5694">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5695">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5696">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5697">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5698">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5699">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5700">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5700">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5702">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5703">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5704">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="110b2-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="110b2-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="110b2-5706">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5706">Target</span></span> | <span data-ttu-id="110b2-5707">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5708">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5709">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5709">8</span></span> |
| <span data-ttu-id="110b2-5710">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5710">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5712">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5712">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5713">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5714">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5715">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5717">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5721">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5722">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5723">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5724">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5725">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5726">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5727">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5728">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5729">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5730">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5731">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5732">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5733">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5734">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5735">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5736">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5737">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5738">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5739">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5740">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5741">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5742">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5743">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5744">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5744">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5746">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5747">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5748">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5749">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5750">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5751">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5752">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5753">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5754">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5754">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5756">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5757">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5758">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="110b2-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="110b2-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="110b2-5760">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5760">Target</span></span> | <span data-ttu-id="110b2-5761">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5762">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5763">8</span><span class="sxs-lookup"><span data-stu-id="110b2-5763">8</span></span> |
| <span data-ttu-id="110b2-5764">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5764">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5766">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5766">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5767">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5768">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5769">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5771">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5775">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5776">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5777">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5778">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5779">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5780">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5781">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5782">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5783">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5784">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5785">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5786">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5787">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5788">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5789">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5790">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5791">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5792">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5793">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5794">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5795">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5796">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5797">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5798">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5798">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5800">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5801">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5802">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5803">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5804">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5805">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5806">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5807">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5808">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5808">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5810">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5811">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5812">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="110b2-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="110b2-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="110b2-5814">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5814">Target</span></span> | <span data-ttu-id="110b2-5815">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5816">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5817">16</span><span class="sxs-lookup"><span data-stu-id="110b2-5817">16</span></span> |
| <span data-ttu-id="110b2-5818">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5818">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="110b2-5820">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5820">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5821">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5822">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5823">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5825">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="110b2-5829">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="110b2-5830">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="110b2-5831">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5832">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5833">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5834">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5835">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="110b2-5836">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5837">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5838">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5839">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5840">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5841">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5842">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5843">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5844">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5845">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5846">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5847">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5848">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5849">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5850">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5851">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5852">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5852">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5854">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5855">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5856">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5857">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5858">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5859">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5860">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5861">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5862">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5862">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5864">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5865">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5866">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="110b2-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>фнс</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="110b2-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="110b2-5868">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="110b2-5868">Target</span></span> | <span data-ttu-id="110b2-5869">Поддержка</span><span class="sxs-lookup"><span data-stu-id="110b2-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="110b2-5870">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="110b2-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="110b2-5871">16</span><span class="sxs-lookup"><span data-stu-id="110b2-5871">16</span></span> |
| <span data-ttu-id="110b2-5872">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="110b2-5872">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5874">Буфер</span><span class="sxs-lookup"><span data-stu-id="110b2-5874">Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5875">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5876">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="110b2-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5877">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="110b2-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="110b2-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="110b2-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="110b2-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="110b2-5879">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="110b2-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="110b2-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="110b2-5882">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5884">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="110b2-5884">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5886">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="110b2-5886">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5888">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="110b2-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="110b2-5889">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="110b2-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="110b2-5890">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="110b2-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="110b2-5891">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="110b2-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="110b2-5892">Mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5892">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5894">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="110b2-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="110b2-5895">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5896">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="110b2-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5897">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="110b2-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="110b2-5898">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="110b2-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="110b2-5899">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5900">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="110b2-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="110b2-5901">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="110b2-5902">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="110b2-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="110b2-5903">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="110b2-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="110b2-5904">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="110b2-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="110b2-5905">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="110b2-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="110b2-5906">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="110b2-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="110b2-5907">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="110b2-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="110b2-5908">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5909">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="110b2-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="110b2-5910">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="110b2-5910">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="110b2-5912">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5913">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="110b2-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="110b2-5914">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="110b2-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="110b2-5915">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="110b2-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="110b2-5916">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="110b2-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="110b2-5917">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="110b2-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="110b2-5918">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="110b2-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="110b2-5919">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="110b2-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="110b2-5920">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="110b2-5921">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="110b2-5922">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="110b2-5923">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="110b2-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="110b2-5924">Форматирование заметок</span><span class="sxs-lookup"><span data-stu-id="110b2-5924">Format notes</span></span>

<span data-ttu-id="110b2-5925">Назначение формата может изменяться с одного уровня компонентов оборудования на следующий.</span><span class="sxs-lookup"><span data-stu-id="110b2-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="110b2-5926"><sup>L</sup> : нетипизированный формат</span><span class="sxs-lookup"><span data-stu-id="110b2-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="110b2-5927"><sup>ПК</sup> : частично типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="110b2-5928"><sup>FCS</sup> : полностью типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="110b2-5929"><sup>ФНС</sup> : полностью типизированный, неприведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="110b2-5930"><sup>ПКК</sup> : частично типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="110b2-5931"><sup>FCC</sup> : полностью типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="110b2-5932"><sup>ФНК</sup> : полностью типизированный, неприведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="110b2-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="110b2-5933"><sup>V</sup> : формат видео</span><span class="sxs-lookup"><span data-stu-id="110b2-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="110b2-5934">См. также</span><span class="sxs-lookup"><span data-stu-id="110b2-5934">Related topics</span></span>

[<span data-ttu-id="110b2-5935">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="110b2-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="110b2-5936">[Реализация теневых буферов для уровня функций Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="110b2-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="110b2-5937">Сопоставление форматов прежних версий</span><span class="sxs-lookup"><span data-stu-id="110b2-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="110b2-5938">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="110b2-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
