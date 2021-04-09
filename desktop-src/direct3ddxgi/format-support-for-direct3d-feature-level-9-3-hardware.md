---
description: В этом разделе указаны форматы ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,3.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Поддержка форматов для оборудования Direct3D с уровнем компонентов 9.9.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072180"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="3d78b-103">Поддержка форматов для оборудования Direct3D с уровнем компонентов 9.9.3</span><span class="sxs-lookup"><span data-stu-id="3d78b-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="3d78b-104">В этом разделе указаны форматы ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,3.</span><span class="sxs-lookup"><span data-stu-id="3d78b-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="3d78b-105">В таблице приводится сводка по поддержке функций с использованием следующего ключа.</span><span class="sxs-lookup"><span data-stu-id="3d78b-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="3d78b-106">Символ</span><span class="sxs-lookup"><span data-stu-id="3d78b-106">Symbol</span></span>                            | <span data-ttu-id="3d78b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3d78b-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3d78b-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="3d78b-108">_ *-*\*</span></span>                             | <span data-ttu-id="3d78b-109">Не разрешено или недоступно.</span><span class="sxs-lookup"><span data-stu-id="3d78b-109">Disallowed or not available.</span></span>                                                  |
| ![обязательно](images/letter-r.jpg)  | <span data-ttu-id="3d78b-111">Требуется поддержка оборудования.</span><span class="sxs-lookup"><span data-stu-id="3d78b-111">Hardware support is required.</span></span>                                                 |
| ![необязательно](images/letter-o.jpg)  | <span data-ttu-id="3d78b-113">Аппаратная поддержка необязательно. формат аппаратного ускорения может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="3d78b-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![зависимых](images/letter-d.jpg) | <span data-ttu-id="3d78b-115">Требуется, если поддерживается дополнительная функция.</span><span class="sxs-lookup"><span data-stu-id="3d78b-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="3d78b-116">Этот раздел содержит раздел для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="3d78b-116">This topic contains a section per format.</span></span> <span data-ttu-id="3d78b-117">*Цель* формата (таблицы содержат по одной строке на каждый целевой объект) может быть типом ресурса, встроенной функцией HLSL или определенной функциональностью, зависящей от конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="3d78b-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="3d78b-118">Чтобы программно проверить поддержку формата в D3D11 и D3D12, обратитесь к статье [Проверка поддержки аппаратных компонентов](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="3d78b-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="3d78b-119">Числа форматов в основном, но не все, в возрастающем числовом порядке &mdash; , некоторые из них имеют нечисловой порядок и перечислены вместе с другими соответствующими форматами.</span><span class="sxs-lookup"><span data-stu-id="3d78b-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="3d78b-120">Обратите внимание, что *тип* в имени формата может означать *частичную* типизацию, а не строго типизированный (см. раздел [Format Notes](#format-notes) в конце раздела).</span><span class="sxs-lookup"><span data-stu-id="3d78b-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="3d78b-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="3d78b-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="3d78b-122">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-122">Target</span></span> | <span data-ttu-id="3d78b-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-123">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-124">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-125">0</span><span class="sxs-lookup"><span data-stu-id="3d78b-125">0</span></span> |
| <span data-ttu-id="3d78b-126">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-126">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-127">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-127">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-128">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-129">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-130">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-131">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-132">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-133">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-134">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-135">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-136">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-137">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-138">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-139">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-140">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-141">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-142">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-143">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-144">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-145">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-146">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-147">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-148">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-149">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-150">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-151">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-152">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-153">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-154">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-155">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-156">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-157">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-158">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-159">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-160">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-161">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-162">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-163">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-164">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-165">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-166">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-167">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-168">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-169">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-170">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="3d78b-171">\_Нетипизированные<sup>ПК</sup> DXGI_FORMAT_R32G32B32A32 (1)</span><span class="sxs-lookup"><span data-stu-id="3d78b-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="3d78b-172">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-172">Target</span></span> | <span data-ttu-id="3d78b-173">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-173">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-174">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-175">128</span><span class="sxs-lookup"><span data-stu-id="3d78b-175">128</span></span> |
| <span data-ttu-id="3d78b-176">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-176">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-177">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-177">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-178">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-179">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-180">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-181">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-182">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-183">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-184">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-185">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-186">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-187">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-188">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-189">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-190">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-191">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-192">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-193">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-194">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-195">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-196">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-197">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-198">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-199">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-200">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-201">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-202">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-203">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-204">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-205">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-206">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-207">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-208">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-209">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-210">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-211">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-212">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-213">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-214">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-215">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-216">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-217">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-218">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-219">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-220">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="3d78b-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>ФНС</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="3d78b-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="3d78b-222">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-222">Target</span></span> | <span data-ttu-id="3d78b-223">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-223">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-224">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-225">128</span><span class="sxs-lookup"><span data-stu-id="3d78b-225">128</span></span> |
| <span data-ttu-id="3d78b-226">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-226">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-228">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-228">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-229">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-229">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-231">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-232">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-233">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-234">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-236">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-238">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-240">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-240">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-242">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-243">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-244">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-245">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-246">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-247">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-247">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-249">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-249">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-251">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-251">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-253">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-254">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-255">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-256">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-257">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-258">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-259">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-260">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-261">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-262">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-263">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-264">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-265">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-266">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-267">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-267">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-269">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-269">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-271">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-271">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-273">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-273">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-275">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-275">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-277">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-278">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-279">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-280">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-281">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-282">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-283">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-284">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="3d78b-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>ФНС</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="3d78b-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="3d78b-286">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-286">Target</span></span> | <span data-ttu-id="3d78b-287">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-287">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-288">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-289">128</span><span class="sxs-lookup"><span data-stu-id="3d78b-289">128</span></span> |
| <span data-ttu-id="3d78b-290">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-290">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-291">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-291">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-292">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-293">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-294">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-295">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-296">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-297">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-298">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-299">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-300">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-301">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-302">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-303">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-304">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-305">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-305">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-306">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-307">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-308">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-309">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-310">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-311">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-312">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-313">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-314">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-315">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-316">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-317">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-318">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-319">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-320">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-321">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-322">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-323">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-324">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-325">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-326">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-327">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-328">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-329">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-330">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-331">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-332">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-333">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-334">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="3d78b-335">DXGI_FORMAT_R32G32B32A32 \_ Синт<sup>ФНС</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="3d78b-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="3d78b-336">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-336">Target</span></span> | <span data-ttu-id="3d78b-337">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-337">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-338">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-339">128</span><span class="sxs-lookup"><span data-stu-id="3d78b-339">128</span></span> |
| <span data-ttu-id="3d78b-340">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-340">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-341">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-341">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-342">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-343">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-344">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-345">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-346">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-347">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-348">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-349">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-350">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-351">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-352">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-353">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-354">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-355">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-355">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-356">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-357">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-358">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-359">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-360">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-361">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-362">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-363">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-364">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-365">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-366">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-367">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-368">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-369">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-370">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-371">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-372">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-373">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-374">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-375">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-376">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-377">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-378">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-379">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-380">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-381">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-382">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-383">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-384">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="3d78b-385">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32B32 (5)</span><span class="sxs-lookup"><span data-stu-id="3d78b-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="3d78b-386">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-386">Target</span></span> | <span data-ttu-id="3d78b-387">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-387">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-388">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-389">96</span><span class="sxs-lookup"><span data-stu-id="3d78b-389">96</span></span> |
| <span data-ttu-id="3d78b-390">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-390">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-391">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-391">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-392">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-393">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-394">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-395">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-396">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-397">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-398">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-399">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-400">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-401">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-402">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-403">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-404">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-405">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-406">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-407">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-408">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-409">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-410">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-411">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-412">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-413">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-414">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-415">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-416">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-417">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-418">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-419">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-420">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-421">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-422">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-423">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-424">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-425">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-426">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-427">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-428">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-429">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-430">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-431">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-432">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-433">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-434">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="3d78b-435">DXGI_FORMAT_R32G32B32 \_ float<sup>ФНС</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="3d78b-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="3d78b-436">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-436">Target</span></span> | <span data-ttu-id="3d78b-437">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-437">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-438">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-439">96</span><span class="sxs-lookup"><span data-stu-id="3d78b-439">96</span></span> |
| <span data-ttu-id="3d78b-440">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-440">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-442">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-442">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-443">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-443">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-445">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-446">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-447">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-448">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-449">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-450">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-451">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-452">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-453">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-454">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-455">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-456">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-457">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-458">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-459">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-460">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-460">Blendable RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-462">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-463">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-464">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-465">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-466">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-467">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-468">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-469">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-470">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-471">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-472">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-473">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-474">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-475">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-476">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-476">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-478">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-478">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-480">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-481">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-482">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-483">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-484">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-485">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-486">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-487">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-488">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-489">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="3d78b-490">DXGI_FORMAT_R32G32B32 \_ uint<sup>ФНС</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="3d78b-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="3d78b-491">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-491">Target</span></span> | <span data-ttu-id="3d78b-492">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-492">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-493">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-494">96</span><span class="sxs-lookup"><span data-stu-id="3d78b-494">96</span></span> |
| <span data-ttu-id="3d78b-495">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-495">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-496">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-496">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-497">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-498">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-499">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-500">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-501">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-502">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-503">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-504">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-505">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-506">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-507">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-508">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-509">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-510">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-511">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-512">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-513">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-514">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-515">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-516">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-517">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-518">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-519">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-520">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-521">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-522">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-523">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-524">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-525">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-526">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-527">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-528">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-528">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-530">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-530">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-532">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-533">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-534">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-535">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-536">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-537">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-538">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-539">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-540">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-541">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="3d78b-542">DXGI_FORMAT_R32G32B32 \_ Синт<sup>ФНС</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="3d78b-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="3d78b-543">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-543">Target</span></span> | <span data-ttu-id="3d78b-544">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-544">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-545">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-546">96</span><span class="sxs-lookup"><span data-stu-id="3d78b-546">96</span></span> |
| <span data-ttu-id="3d78b-547">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-547">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-548">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-548">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-549">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-550">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-551">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-552">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-553">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-554">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-555">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-556">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-557">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-558">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-559">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-560">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-561">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-562">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-563">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-564">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-565">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-566">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-567">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-568">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-569">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-570">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-571">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-572">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-573">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-574">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-575">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-576">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-577">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-578">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-579">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-580">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-580">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-582">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-582">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="3d78b-584">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-585">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-586">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-587">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-588">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-589">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-590">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-591">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-592">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-593">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="3d78b-594">DXGI_FORMAT_R16G16B16A16 \_ <sup>ПК</sup> нетипизированных типов (9)</span><span class="sxs-lookup"><span data-stu-id="3d78b-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="3d78b-595">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-595">Target</span></span> | <span data-ttu-id="3d78b-596">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-596">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-597">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-598">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-598">64</span></span> |
| <span data-ttu-id="3d78b-599">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-599">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-600">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-600">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-601">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-602">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-603">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-604">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-605">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-606">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-607">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-608">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-609">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-610">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-611">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-612">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-613">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-614">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-615">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-616">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-617">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-618">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-619">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-620">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-621">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-622">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-623">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-624">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-625">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-626">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-627">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-628">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-629">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-630">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-631">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-632">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-633">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-634">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-635">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-636">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-637">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-638">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-639">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-640">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-641">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-642">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-643">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="3d78b-644">DXGI_FORMAT_R16G16B16A16 \_ float<sup>ФНС</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="3d78b-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="3d78b-645">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-645">Target</span></span> | <span data-ttu-id="3d78b-646">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-646">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-647">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-648">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-648">64</span></span> |
| <span data-ttu-id="3d78b-649">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-649">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-651">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-651">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-652">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-652">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-654">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-655">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-656">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-657">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-659">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-661">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-663">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-663">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-665">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-665">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-667">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-668">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-669">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-670">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-671">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-673">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-673">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-675">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-675">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-677">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-677">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-679">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-680">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-681">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-682">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-683">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-684">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-685">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-686">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-687">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-688">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-689">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-690">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-691">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-692">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-692">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-694">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-694">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-696">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-696">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-698">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-698">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-700">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-700">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-702">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-703">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-704">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-705">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-706">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-707">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-708">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-708">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-710">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="3d78b-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>ФНС</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="3d78b-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="3d78b-712">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-712">Target</span></span> | <span data-ttu-id="3d78b-713">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-713">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-714">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-715">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-715">64</span></span> |
| <span data-ttu-id="3d78b-716">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-716">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-718">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-718">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-719">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-720">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-721">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-722">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-723">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-725">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-727">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-729">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-729">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-731">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-731">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-733">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-734">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-735">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-736">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-737">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-737">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-739">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-739">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-741">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-741">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-743">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-744">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-745">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-746">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-747">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-748">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-749">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-750">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-751">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-752">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-753">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-754">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-755">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-756">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-757">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-757">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-759">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-759">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-761">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-761">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-763">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-763">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-765">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-765">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-767">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-768">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-769">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-770">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-771">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-772">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-773">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-774">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="3d78b-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>ФНС</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="3d78b-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="3d78b-776">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-776">Target</span></span> | <span data-ttu-id="3d78b-777">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-777">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-778">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-779">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-779">64</span></span> |
| <span data-ttu-id="3d78b-780">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-780">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-781">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-781">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-782">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-783">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-784">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-785">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-786">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-787">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-788">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-789">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-790">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-791">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-792">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-793">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-794">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-795">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-795">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-796">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-797">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-798">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-799">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-800">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-801">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-802">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-803">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-804">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-805">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-806">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-807">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-808">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-809">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-810">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-811">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-812">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-813">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-814">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-815">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-816">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-817">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-818">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-819">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-820">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-821">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-822">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-823">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-824">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="3d78b-825">DXGI_FORMAT_R16G16B16A16 \_ Снорм<sup>ФНС</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="3d78b-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="3d78b-826">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-826">Target</span></span> | <span data-ttu-id="3d78b-827">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-827">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-828">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-829">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-829">64</span></span> |
| <span data-ttu-id="3d78b-830">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-830">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-832">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-832">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-833">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-833">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-835">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-836">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-837">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-838">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-839">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-840">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-841">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-842">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-843">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-844">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-845">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-846">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-847">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-848">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-849">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-850">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-851">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-852">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-853">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-854">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-855">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-856">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-857">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-858">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-859">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-860">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-861">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-862">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-863">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-864">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-865">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-866">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-867">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-868">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-869">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-870">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-871">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-872">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-873">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-874">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-875">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-876">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="3d78b-877">DXGI_FORMAT_R16G16B16A16 \_ Синт<sup>ФНС</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="3d78b-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="3d78b-878">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-878">Target</span></span> | <span data-ttu-id="3d78b-879">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-879">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-880">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-881">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-881">64</span></span> |
| <span data-ttu-id="3d78b-882">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-882">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-884">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-884">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-885">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-885">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-887">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-888">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-889">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-890">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-891">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-892">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-893">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-894">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-895">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-896">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-897">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-898">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-899">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-899">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-900">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-901">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-902">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-903">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-904">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-905">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-906">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-907">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-908">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-909">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-910">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-911">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-912">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-913">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-914">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-915">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-916">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-917">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-918">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-919">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-920">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-921">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-922">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-923">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-924">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-925">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-926">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-927">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-928">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="3d78b-929">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32 (15)</span><span class="sxs-lookup"><span data-stu-id="3d78b-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="3d78b-930">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-930">Target</span></span> | <span data-ttu-id="3d78b-931">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-931">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-932">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-933">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-933">64</span></span> |
| <span data-ttu-id="3d78b-934">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-934">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-935">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-935">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-936">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-937">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-938">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-939">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-940">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-941">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-942">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-943">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-944">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-945">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-946">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-947">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-948">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-949">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-949">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-950">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-951">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-952">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-953">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-954">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-955">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-956">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-957">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-958">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-959">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-960">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-961">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-962">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-963">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-964">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-965">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-966">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-967">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-968">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-969">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-970">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-971">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-972">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-973">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-974">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-975">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-976">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-977">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-978">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="3d78b-979">DXGI_FORMAT_R32G32 \_ float<sup>ФНС</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="3d78b-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="3d78b-980">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-980">Target</span></span> | <span data-ttu-id="3d78b-981">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-981">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-982">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-983">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-983">64</span></span> |
| <span data-ttu-id="3d78b-984">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-984">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-986">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-986">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-987">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-987">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-989">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-990">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-991">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-992">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-994">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-996">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-998">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-998">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1000">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1001">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1002">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1003">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1004">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1005">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1006">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1007">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1007">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1009">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1010">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1011">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1012">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1013">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1014">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1015">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1016">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1017">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1018">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1019">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1020">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1021">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1022">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1023">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1023">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1025">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1025">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1027">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1027">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1029">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1029">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1031">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1031">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1033">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1034">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1035">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1036">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1037">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1038">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1039">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1040">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="3d78b-1041">DXGI_FORMAT_R32G32 \_ uint<sup>ФНС</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="3d78b-1042">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1042">Target</span></span> | <span data-ttu-id="3d78b-1043">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1044">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1045">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1045">64</span></span> |
| <span data-ttu-id="3d78b-1046">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1046">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1047">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1047">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1048">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1049">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1050">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1055">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1056">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1057">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1058">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1059">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1060">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1061">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1062">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1063">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1064">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1065">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1066">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1067">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1068">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1069">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1070">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1071">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1072">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1073">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1074">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1075">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1076">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1077">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1078">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1079">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1080">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1081">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1082">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1083">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1084">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1085">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1086">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1087">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1088">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1089">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1090">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="3d78b-1091">DXGI_FORMAT_R32G32 \_ Синт<sup>ФНС</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="3d78b-1092">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1092">Target</span></span> | <span data-ttu-id="3d78b-1093">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1094">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1095">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1095">64</span></span> |
| <span data-ttu-id="3d78b-1096">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1096">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1097">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1097">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1098">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1099">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1100">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1105">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1106">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1107">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1108">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1109">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1110">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1111">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1112">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1113">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1114">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1115">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1116">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1117">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1118">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1119">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1120">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1121">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1122">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1123">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1124">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1125">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1126">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1127">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1128">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1129">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1130">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1131">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1132">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1133">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1134">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1135">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1136">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1137">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1138">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1139">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1140">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="3d78b-1141">DXGI_FORMAT_R32G8X24 \_ <sup>ПК</sup> нетипизированного типа (19)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="3d78b-1142">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1142">Target</span></span> | <span data-ttu-id="3d78b-1143">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1144">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1145">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1145">64</span></span> |
| <span data-ttu-id="3d78b-1146">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1146">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1147">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1147">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1148">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1149">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1150">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1155">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1156">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1157">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1158">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1159">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1160">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1161">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1162">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1163">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1164">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1165">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1166">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1167">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1168">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1169">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1170">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1171">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1172">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1173">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1174">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1175">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1176">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1177">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1178">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1179">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1180">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1181">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1182">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1183">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1184">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1185">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1186">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1187">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1188">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1189">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1190">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="3d78b-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>ФНС</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="3d78b-1192">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1192">Target</span></span> | <span data-ttu-id="3d78b-1193">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1194">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1195">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1195">64</span></span> |
| <span data-ttu-id="3d78b-1196">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1196">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1197">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1197">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1198">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1199">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1200">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1205">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1206">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1207">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1208">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1209">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1210">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1211">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1212">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1213">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1214">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1215">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1216">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1217">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1218">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1219">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1220">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1221">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1222">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1223">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1224">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1225">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1226">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1227">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1228">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1229">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1230">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1231">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1232">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1233">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1234">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1235">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1236">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1237">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1238">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1239">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1240">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="3d78b-1241">DXGI_FORMAT_R32 \_ \_ ФНС с типом float X8X24 \_ (21)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="3d78b-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="3d78b-1242">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1242">Target</span></span> | <span data-ttu-id="3d78b-1243">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1244">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1245">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1245">64</span></span> |
| <span data-ttu-id="3d78b-1246">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1246">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1247">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1247">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1248">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1249">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1250">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1255">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1256">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1257">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1258">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1259">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1260">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1261">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1262">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1263">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1264">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1265">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1266">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1267">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1268">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1269">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1270">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1271">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1272">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1273">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1274">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1275">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1276">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1277">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1278">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1279">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1280">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1281">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1282">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1283">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1284">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1285">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1286">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1287">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1288">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1289">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1290">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="3d78b-1291">DXGI_FORMAT_X32 без \_ типа \_ G8X24 \_ uint<sup>ФНС</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="3d78b-1292">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1292">Target</span></span> | <span data-ttu-id="3d78b-1293">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1294">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1295">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-1295">64</span></span> |
| <span data-ttu-id="3d78b-1296">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1296">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1297">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1297">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1298">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1299">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1300">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1305">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1306">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1307">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1308">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1309">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1310">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1312">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1313">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1314">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1315">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1316">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1317">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1318">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1319">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1320">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1321">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1322">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1323">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1324">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1325">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1326">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1327">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1328">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1329">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1330">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1331">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1332">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1333">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1334">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1335">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1336">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1337">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1338">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1339">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1340">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="3d78b-1341">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R10G10B10A2 (23)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="3d78b-1342">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1342">Target</span></span> | <span data-ttu-id="3d78b-1343">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1344">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1345">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1345">32</span></span> |
| <span data-ttu-id="3d78b-1346">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1346">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1347">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1347">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1348">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1349">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1350">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1355">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1356">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1357">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1358">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1359">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1360">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1361">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1362">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1363">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1364">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1365">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1366">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1367">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1368">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1369">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1370">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1371">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1372">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1373">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1374">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1375">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1376">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1377">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1378">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1379">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1380">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1381">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1382">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1383">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1384">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1385">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1386">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1387">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1388">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1389">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1390">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="3d78b-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>ФНС</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="3d78b-1392">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1392">Target</span></span> | <span data-ttu-id="3d78b-1393">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1394">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1395">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1395">32</span></span> |
| <span data-ttu-id="3d78b-1396">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1396">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1397">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1397">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1398">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1399">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1400">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1405">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1406">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1407">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1408">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1409">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1410">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1412">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1413">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1414">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1415">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1416">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1417">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1418">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1419">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1420">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1421">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1422">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1423">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1424">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1425">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1426">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1427">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1428">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1429">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1430">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1431">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1432">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1433">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1434">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1435">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1436">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1437">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1438">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1439">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1439">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1441">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="3d78b-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>ФНС</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="3d78b-1443">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1443">Target</span></span> | <span data-ttu-id="3d78b-1444">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1445">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1446">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1446">32</span></span> |
| <span data-ttu-id="3d78b-1447">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1447">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1448">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1448">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1449">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1450">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1451">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1456">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1457">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1458">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1459">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1460">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1461">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1462">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1463">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1464">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1465">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1466">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1467">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1468">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1469">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1470">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1471">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1472">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1473">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1474">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1475">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1476">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1477">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1478">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1479">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1480">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1481">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1482">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1483">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1484">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1485">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1486">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1487">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1488">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1489">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1490">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1491">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="3d78b-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ смещение \_ a2 \_ UNORM<sup>ФНС</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="3d78b-1493">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1493">Target</span></span> | <span data-ttu-id="3d78b-1494">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1495">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1496">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1496">32</span></span> |
| <span data-ttu-id="3d78b-1497">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1497">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1498">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1498">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1499">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1500">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1501">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1506">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1507">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1508">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1509">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1510">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1511">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1513">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1514">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1515">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1516">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1517">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1518">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1519">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1520">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1521">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1522">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1523">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1524">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1525">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1526">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1527">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1528">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1529">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1530">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1531">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1532">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1533">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1534">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1535">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1536">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1537">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1538">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1539">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1540">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1541">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="3d78b-1542">DXGI_FORMAT_R11G11B10 \_ <sup>ФНС</sup> с плавающей запятой (26)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="3d78b-1543">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1543">Target</span></span> | <span data-ttu-id="3d78b-1544">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1545">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1546">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1546">32</span></span> |
| <span data-ttu-id="3d78b-1547">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1547">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1548">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1548">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1549">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1550">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1551">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1556">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1557">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1558">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1559">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1560">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1561">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1563">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1564">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1565">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1566">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1567">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1568">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1569">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1570">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1571">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1572">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1573">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1574">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1575">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1576">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1577">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1578">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1579">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1580">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1581">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1582">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1583">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1584">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1585">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1586">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1587">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1588">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1589">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1590">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1591">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="3d78b-1592">DXGI_FORMAT_R8G8B8A8 \_ <sup>ПК</sup> нетипизированных типов (27)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="3d78b-1593">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1593">Target</span></span> | <span data-ttu-id="3d78b-1594">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1595">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1596">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1596">32</span></span> |
| <span data-ttu-id="3d78b-1597">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1597">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1598">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1598">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1599">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1600">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1601">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1606">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1607">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1608">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1609">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1610">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1611">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1613">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1614">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1615">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1616">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1617">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1618">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1619">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1620">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1621">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1622">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1623">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1624">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1625">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1626">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1627">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1628">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1629">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1630">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1631">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1632">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1633">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1634">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1635">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1636">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1637">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1638">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1639">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1640">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1641">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="3d78b-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>ФНС</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="3d78b-1643">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1643">Target</span></span> | <span data-ttu-id="3d78b-1644">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1645">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1646">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1646">32</span></span> |
| <span data-ttu-id="3d78b-1647">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1647">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1649">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1649">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1650">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1650">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1652">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1653">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1655">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1657">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1659">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1661">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1661">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1663">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1663">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1665">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1666">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1667">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1668">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1669">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1669">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1671">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1671">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1673">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1673">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1675">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1675">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1677">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1678">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1679">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1680">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1681">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1682">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1683">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1684">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1685">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1686">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1687">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1688">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1689">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1690">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1690">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1692">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1692">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1694">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1694">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1696">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1696">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1698">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1698">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1700">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1701">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1701">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1703">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1704">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1705">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1705">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1707">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1707">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1709">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1709">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1711">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="3d78b-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>ФНС</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="3d78b-1713">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1713">Target</span></span> | <span data-ttu-id="3d78b-1714">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1715">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1716">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1716">32</span></span> |
| <span data-ttu-id="3d78b-1717">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1717">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1719">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1719">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1720">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1721">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1722">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1724">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1726">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1728">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1730">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1730">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1732">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1732">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1734">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1735">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1736">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1737">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1738">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1738">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1740">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1740">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1742">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1742">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1744">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1744">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1746">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1747">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1748">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1749">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1750">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1751">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1752">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1753">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1754">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1755">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1756">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1757">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1758">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1759">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1759">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1761">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1761">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1763">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1763">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1765">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1765">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1767">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1767">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1769">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1770">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1770">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1772">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1773">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1774">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1774">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-1776">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1776">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1778">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1778">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1780">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="3d78b-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>ФНС</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="3d78b-1782">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1782">Target</span></span> | <span data-ttu-id="3d78b-1783">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1784">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1785">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1785">32</span></span> |
| <span data-ttu-id="3d78b-1786">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1786">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1788">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1788">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1789">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1789">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1791">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1792">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1797">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1798">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1799">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1800">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1801">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1802">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1804">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1805">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1806">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1807">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1808">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1809">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1810">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1811">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1812">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1813">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1814">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1815">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1816">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1817">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1818">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1819">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1820">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1821">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1822">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1823">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1824">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1825">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1826">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1827">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1828">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1829">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1830">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1831">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1832">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="3d78b-1833">DXGI_FORMAT_R8G8B8A8 \_ Снорм<sup>ФНС</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="3d78b-1834">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1834">Target</span></span> | <span data-ttu-id="3d78b-1835">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1836">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1837">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1837">32</span></span> |
| <span data-ttu-id="3d78b-1838">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1838">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1840">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1840">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1841">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1842">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1843">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1845">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1848">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1850">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1850">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1852">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1852">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1854">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1855">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1856">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1857">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1858">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1860">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1861">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1862">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1863">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1864">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1865">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1866">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1867">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1868">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1869">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1870">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1871">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1872">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1873">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1874">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1875">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1876">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1876">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1878">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1879">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1880">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1881">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1882">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1883">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1884">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1885">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1886">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1887">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1888">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1889">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="3d78b-1890">DXGI_FORMAT_R8G8B8A8 \_ Синт<sup>фнс</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="3d78b-1891">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1891">Target</span></span> | <span data-ttu-id="3d78b-1892">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1893">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1894">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1894">32</span></span> |
| <span data-ttu-id="3d78b-1895">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1895">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1896">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1896">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1897">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1898">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1899">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1904">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1905">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1906">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1907">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1908">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1909">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1910">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1911">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1912">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1913">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1914">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1915">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1916">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1917">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1918">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1919">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1920">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1921">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1922">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1923">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1924">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1925">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1926">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1927">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1928">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1929">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1930">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1931">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1932">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1933">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1934">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1935">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1936">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1937">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1938">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1939">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="3d78b-1940">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16G16 (33)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="3d78b-1941">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1941">Target</span></span> | <span data-ttu-id="3d78b-1942">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1943">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1944">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1944">32</span></span> |
| <span data-ttu-id="3d78b-1945">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1945">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-1946">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1946">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1947">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1948">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1949">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-1954">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-1955">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1956">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1957">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-1958">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-1959">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-1960">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-1961">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-1962">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1963">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1964">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-1965">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-1966">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1967">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-1968">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-1969">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-1970">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-1971">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-1972">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-1973">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-1974">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-1975">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1976">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-1977">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-1978">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1979">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-1980">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-1981">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-1982">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-1983">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-1984">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-1985">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-1986">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-1987">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-1988">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-1989">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="3d78b-1990">DXGI_FORMAT_R16G16 \_ float<sup>фнс</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="3d78b-1991">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-1991">Target</span></span> | <span data-ttu-id="3d78b-1992">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-1993">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-1994">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-1994">32</span></span> |
| <span data-ttu-id="3d78b-1995">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-1995">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-1997">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-1997">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-1998">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-1998">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2000">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2001">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2003">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2005">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2007">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2009">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2009">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2011">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2012">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2013">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2014">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2015">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2016">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2016">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2018">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2018">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2020">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2020">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2022">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2023">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2024">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2025">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2026">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2027">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2028">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2029">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2030">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2031">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2032">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2033">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2034">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2035">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2036">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2036">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2038">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2038">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2040">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2040">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2042">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2042">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2044">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2044">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2046">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2047">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2048">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2049">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2050">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2051">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2052">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2053">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="3d78b-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>фнс</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="3d78b-2055">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2055">Target</span></span> | <span data-ttu-id="3d78b-2056">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2057">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2058">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2058">32</span></span> |
| <span data-ttu-id="3d78b-2059">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2059">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2061">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2061">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2062">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2063">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2064">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2066">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2068">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2070">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2072">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2072">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2074">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2074">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2076">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2077">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2078">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2079">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2080">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2080">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2082">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2082">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2084">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2084">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2086">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2087">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2088">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2089">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2090">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2091">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2092">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2093">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2094">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2095">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2096">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2097">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2098">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2099">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2100">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2100">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2102">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2102">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2104">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2104">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2106">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2106">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2108">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2108">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2110">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2111">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2112">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2113">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2114">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2115">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2116">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2117">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="3d78b-2118">DXGI_FORMAT_R16G16 \_ uint<sup>фнс</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="3d78b-2119">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2119">Target</span></span> | <span data-ttu-id="3d78b-2120">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2121">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2122">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2122">32</span></span> |
| <span data-ttu-id="3d78b-2123">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2123">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2124">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2124">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2125">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2126">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2127">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2132">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2133">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2134">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2135">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2136">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2137">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2138">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2139">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2140">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2141">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2142">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2143">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2144">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2145">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2146">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2147">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2148">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2149">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2150">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2151">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2152">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2153">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2154">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2155">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2156">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2157">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2158">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2159">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2160">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2161">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2162">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2163">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2164">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2165">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2166">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2167">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="3d78b-2168">DXGI_FORMAT_R16G16 \_ Снорм<sup>фнс</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="3d78b-2169">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2169">Target</span></span> | <span data-ttu-id="3d78b-2170">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2171">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2172">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2172">32</span></span> |
| <span data-ttu-id="3d78b-2173">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2173">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2175">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2175">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2176">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2176">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2178">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2179">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2181">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2183">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2185">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2187">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2187">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2189">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2189">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2191">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2192">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2193">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2194">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2195">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2195">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2197">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2198">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2199">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2200">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2201">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2202">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2203">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2204">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2205">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2206">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2207">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2208">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2209">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2210">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2211">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2212">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2213">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2213">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2215">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2216">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2217">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2218">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2219">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2220">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2221">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2222">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2223">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2224">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2225">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2226">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="3d78b-2227">DXGI_FORMAT_R16G16 \_ Синт<sup>фнс</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="3d78b-2228">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2228">Target</span></span> | <span data-ttu-id="3d78b-2229">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2230">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2231">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2231">32</span></span> |
| <span data-ttu-id="3d78b-2232">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2232">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2234">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2234">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2235">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2235">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2237">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2238">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2243">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2244">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2245">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2246">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2247">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2248">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2250">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2251">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2252">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2253">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2254">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2255">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2256">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2257">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2258">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2259">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2260">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2261">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2262">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2263">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2264">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2265">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2266">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2267">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2268">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2269">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2270">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2271">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2272">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2273">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2274">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2275">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2276">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2277">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2278">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="3d78b-2279">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32 (39)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="3d78b-2280">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2280">Target</span></span> | <span data-ttu-id="3d78b-2281">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2282">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2283">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2283">32</span></span> |
| <span data-ttu-id="3d78b-2284">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2284">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2285">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2285">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2286">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2287">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2288">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2293">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2294">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2295">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2296">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2297">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2298">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2299">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2300">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2301">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2302">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2303">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2304">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2305">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2306">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2307">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2308">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2309">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2310">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2311">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2312">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2313">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2314">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2315">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2316">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2317">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2318">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2319">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2320">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2321">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2322">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2323">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2324">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2325">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2326">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2327">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2328">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="3d78b-2329">DXGI_FORMAT_D32 \_ float<sup>фнс</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="3d78b-2330">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2330">Target</span></span> | <span data-ttu-id="3d78b-2331">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2332">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2333">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2333">32</span></span> |
| <span data-ttu-id="3d78b-2334">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2334">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2335">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2335">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2336">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2337">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2338">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2343">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2344">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2345">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2346">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2347">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2348">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2350">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2351">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2352">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2353">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2354">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2355">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2356">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2357">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2358">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2359">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2360">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2361">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2362">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2363">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2364">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2365">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2366">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2367">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2368">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2369">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2370">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2371">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2372">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2373">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2374">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2375">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2376">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2377">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2378">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="3d78b-2379">DXGI_FORMAT_R32 \_ float<sup>фнс</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="3d78b-2380">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2380">Target</span></span> | <span data-ttu-id="3d78b-2381">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2382">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2383">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2383">32</span></span> |
| <span data-ttu-id="3d78b-2384">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2384">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2386">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2386">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2387">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2387">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2389">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2390">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2392">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2394">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2396">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2398">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2398">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2400">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2401">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2402">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2403">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2404">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2405">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2407">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2407">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2409">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2409">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2411">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2412">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2413">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2414">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2415">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2416">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2417">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2418">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2419">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2420">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2421">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2422">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2423">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2424">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2425">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2425">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2427">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2427">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2429">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2429">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2431">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2431">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2433">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2433">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2435">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2436">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2437">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2438">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2439">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2440">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2441">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2442">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="3d78b-2443">DXGI_FORMAT_R32 \_ uint<sup>фнс</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="3d78b-2444">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2444">Target</span></span> | <span data-ttu-id="3d78b-2445">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2446">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2447">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2447">32</span></span> |
| <span data-ttu-id="3d78b-2448">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2448">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2450">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2450">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2451">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2452">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2452">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2454">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2459">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2460">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2461">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2462">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2463">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2464">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2465">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2466">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2467">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2468">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2469">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2470">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2471">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2472">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2473">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2474">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2475">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2476">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2477">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2478">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2479">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2480">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2481">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2482">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2483">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2484">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2485">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2486">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2487">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2488">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2489">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2490">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2491">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2492">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2493">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2494">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="3d78b-2495">DXGI_FORMAT_R32 \_ Синт<sup>фнс</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="3d78b-2496">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2496">Target</span></span> | <span data-ttu-id="3d78b-2497">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2498">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2499">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2499">32</span></span> |
| <span data-ttu-id="3d78b-2500">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2500">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2501">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2501">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2502">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2503">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2504">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2509">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2510">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2511">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2512">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2513">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2514">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2516">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2517">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2518">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2519">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2520">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2521">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2522">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2523">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2524">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2525">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2526">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2527">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2528">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2529">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2530">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2531">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2532">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2533">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2534">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2535">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2536">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2537">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2538">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2539">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2540">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2541">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2542">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2543">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2544">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="3d78b-2545">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R24G8 (44)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="3d78b-2546">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2546">Target</span></span> | <span data-ttu-id="3d78b-2547">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2548">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2549">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2549">32</span></span> |
| <span data-ttu-id="3d78b-2550">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2550">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2551">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2551">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2552">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2553">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2554">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2559">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2560">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2561">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2562">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2563">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2564">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2565">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2566">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2567">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2568">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2569">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2570">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2571">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2572">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2573">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2574">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2575">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2576">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2577">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2578">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2579">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2580">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2581">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2582">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2583">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2584">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2585">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2586">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2587">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2588">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2589">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2590">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2591">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2592">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2593">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2594">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="3d78b-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>ФНС</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="3d78b-2596">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2596">Target</span></span> | <span data-ttu-id="3d78b-2597">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2598">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2599">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2599">32</span></span> |
| <span data-ttu-id="3d78b-2600">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2600">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2602">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2602">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2603">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2604">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2605">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2607">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2611">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2612">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2613">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2614">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2615">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2616">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2618">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2619">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2620">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2621">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2622">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2622">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2624">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2625">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2626">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2627">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2628">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2629">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2630">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2631">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2632">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2633">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2634">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2635">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2636">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2636">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2638">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2638">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2640">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2640">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-2642">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2643">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2644">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2645">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2646">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2647">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2648">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2649">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2650">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="3d78b-2651">DXGI_FORMAT_R24 \_ UNORM \_ x8 \_ нетипизированный<sup>ФНС</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="3d78b-2652">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2652">Target</span></span> | <span data-ttu-id="3d78b-2653">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2654">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2655">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2655">32</span></span> |
| <span data-ttu-id="3d78b-2656">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2656">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2657">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2657">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2658">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2659">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2660">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2665">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2666">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2667">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2668">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2669">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2670">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2672">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2673">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2674">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2675">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2676">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2677">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2678">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2679">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2680">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2681">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2682">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2683">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2684">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2685">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2686">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2687">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2688">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2689">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2690">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2691">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2692">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2693">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2694">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2695">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2696">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2697">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2698">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2699">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2700">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="3d78b-2701">DXGI_FORMAT_X24 без \_ типа \_ G8 \_ UINT<sup>ФНС</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="3d78b-2702">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2702">Target</span></span> | <span data-ttu-id="3d78b-2703">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2704">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2705">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-2705">32</span></span> |
| <span data-ttu-id="3d78b-2706">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2706">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2707">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2707">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2708">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2709">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2710">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2715">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2716">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2717">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2718">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2719">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2720">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2722">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2723">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2724">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2725">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2726">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2727">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2728">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2729">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2730">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2731">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2732">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2733">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2734">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2735">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2736">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2737">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2738">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2739">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2740">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2741">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2742">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2743">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2744">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2745">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2746">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2747">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2748">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2749">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2750">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="3d78b-2751">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8G8 (48)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="3d78b-2752">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2752">Target</span></span> | <span data-ttu-id="3d78b-2753">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2754">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2755">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-2755">16</span></span> |
| <span data-ttu-id="3d78b-2756">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2756">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2757">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2757">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2758">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2759">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2760">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2765">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2766">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2767">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2768">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2769">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2770">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2771">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2772">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2773">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2774">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2775">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2776">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2777">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2778">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2779">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2780">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2781">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2782">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2783">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2784">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2785">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2786">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2787">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2788">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2789">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2790">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2791">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2792">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2793">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2794">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2795">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2796">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2797">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2798">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2799">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2800">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="3d78b-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>фнс</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="3d78b-2802">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2802">Target</span></span> | <span data-ttu-id="3d78b-2803">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2804">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2805">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-2805">16</span></span> |
| <span data-ttu-id="3d78b-2806">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2806">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2808">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2808">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2809">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2810">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2811">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2813">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2817">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2817">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2819">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2819">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2821">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2822">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2823">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2824">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2825">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2826">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2827">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2827">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2829">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2829">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2831">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2832">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2833">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2834">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2835">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2836">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2837">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2838">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2839">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2840">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2841">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2842">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2843">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2844">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2844">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2846">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2847">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2848">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2849">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2850">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2851">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2852">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2853">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2854">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2855">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2856">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2856">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2858">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="3d78b-2859">DXGI_FORMAT_R8G8 \_ uint<sup>фнс</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="3d78b-2860">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2860">Target</span></span> | <span data-ttu-id="3d78b-2861">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2862">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2863">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-2863">16</span></span> |
| <span data-ttu-id="3d78b-2864">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2864">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2865">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2865">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2866">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2867">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2868">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2873">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2874">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2875">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2876">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2877">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2878">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2879">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2880">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2881">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2882">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2883">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2884">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2885">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2886">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2887">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2888">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2889">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2890">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2891">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2892">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2893">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2894">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2895">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2896">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-2897">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2898">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2899">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2900">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2901">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2902">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2903">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2904">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2905">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2906">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2907">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2908">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="3d78b-2909">DXGI_FORMAT_R8G8 \_ Снорм<sup>фнс</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="3d78b-2910">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2910">Target</span></span> | <span data-ttu-id="3d78b-2911">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2912">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2913">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-2913">16</span></span> |
| <span data-ttu-id="3d78b-2914">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2914">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2916">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2916">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2917">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2918">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2919">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2921">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2925">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2925">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2927">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2927">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2929">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2930">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2931">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2932">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2933">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2933">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2935">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2936">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2937">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2938">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2939">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2940">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2941">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2942">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2943">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2944">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2945">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2946">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2947">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2948">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-2949">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2950">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-2951">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-2951">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-2953">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2954">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2955">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-2956">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-2957">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-2958">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-2959">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-2960">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-2961">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-2962">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-2963">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-2964">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="3d78b-2965">DXGI_FORMAT_R8G8 \_ Синт<sup>фнс</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="3d78b-2966">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-2966">Target</span></span> | <span data-ttu-id="3d78b-2967">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-2968">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-2969">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-2969">16</span></span> |
| <span data-ttu-id="3d78b-2970">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-2970">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-2971">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-2971">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2972">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2973">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2974">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-2979">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-2980">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2981">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2982">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-2983">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-2984">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-2985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-2986">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-2987">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2988">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-2989">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-2990">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-2991">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2992">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-2993">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-2994">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-2995">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-2996">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-2997">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-2998">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-2999">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3000">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3001">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3002">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3003">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3004">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3005">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3006">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3007">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3008">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3009">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3010">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3011">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3012">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3013">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3014">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="3d78b-3015">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16 (53)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="3d78b-3016">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3016">Target</span></span> | <span data-ttu-id="3d78b-3017">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3018">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3019">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3019">16</span></span> |
| <span data-ttu-id="3d78b-3020">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3020">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3021">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3021">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3022">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3023">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3024">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3029">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3030">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3031">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3032">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3033">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3034">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3036">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3037">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3038">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3039">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3040">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3041">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3042">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3043">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3044">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3045">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3046">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3047">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3048">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3049">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3050">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3051">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3052">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3053">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3054">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3055">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3056">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3057">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3058">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3059">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3060">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3061">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3062">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3063">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3064">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="3d78b-3065">DXGI_FORMAT_R16 \_ float<sup>фнс</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="3d78b-3066">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3066">Target</span></span> | <span data-ttu-id="3d78b-3067">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3068">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3069">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3069">16</span></span> |
| <span data-ttu-id="3d78b-3070">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3070">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3071">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3071">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3072">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3073">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3074">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3079">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3080">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3081">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3082">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3083">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3084">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3085">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3086">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3087">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3088">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3089">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3090">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3091">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3092">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3093">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3094">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3095">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3096">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3097">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3098">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3099">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3100">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3101">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3102">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3103">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3104">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3105">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3106">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3107">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3108">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3109">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3110">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3111">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3112">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3113">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3114">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="3d78b-3115">DXGI_FORMAT_D16 \_ UNORM<sup>фнс</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="3d78b-3116">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3116">Target</span></span> | <span data-ttu-id="3d78b-3117">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3118">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3119">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3119">16</span></span> |
| <span data-ttu-id="3d78b-3120">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3120">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3122">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3122">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3123">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3124">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3125">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3127">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3131">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3132">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3133">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3134">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3135">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3136">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3137">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3138">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3139">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3140">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3141">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3142">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3142">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3144">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3145">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3146">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3147">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3148">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3149">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3150">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3151">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3152">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3153">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3154">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3155">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3156">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3156">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-3158">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3158">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-3160">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3160">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-3162">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3163">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3164">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3165">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3166">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3167">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3168">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3169">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3170">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="3d78b-3171">DXGI_FORMAT_R16 \_ UNORM<sup>фнс</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="3d78b-3172">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3172">Target</span></span> | <span data-ttu-id="3d78b-3173">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3174">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3175">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3175">16</span></span> |
| <span data-ttu-id="3d78b-3176">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3176">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3178">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3178">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3179">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3180">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3181">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3183">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3185">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3187">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3189">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3189">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3191">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3191">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3193">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3194">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3195">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3196">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3197">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3199">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3200">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3201">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3202">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3203">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3204">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3205">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3206">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3207">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3208">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3209">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3210">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3211">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3212">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3213">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3214">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3215">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3215">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3217">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3218">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3219">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3220">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3221">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3222">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3223">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3224">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3225">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3226">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3227">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3228">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="3d78b-3229">DXGI_FORMAT_R16 \_ uint<sup>фнс</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="3d78b-3230">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3230">Target</span></span> | <span data-ttu-id="3d78b-3231">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3232">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3233">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3233">16</span></span> |
| <span data-ttu-id="3d78b-3234">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3234">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3236">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3236">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3237">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3238">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3238">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3240">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3245">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3246">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3247">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3248">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3249">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3250">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3251">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3252">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3253">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3254">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3255">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3256">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3257">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3258">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3259">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3260">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3261">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3262">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3263">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3264">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3265">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3266">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3267">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3268">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3269">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3270">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3271">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3272">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3273">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3274">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3275">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3276">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3277">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3278">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3279">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3280">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="3d78b-3281">DXGI_FORMAT_R16 \_ Снорм<sup>фнс</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="3d78b-3282">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3282">Target</span></span> | <span data-ttu-id="3d78b-3283">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3284">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3285">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3285">16</span></span> |
| <span data-ttu-id="3d78b-3286">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3286">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3287">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3287">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3288">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3289">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3290">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3295">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3296">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3297">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3298">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3299">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3300">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3301">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3302">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3303">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3304">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3305">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3306">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3307">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3308">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3309">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3310">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3311">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3312">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3313">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3314">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3315">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3316">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3317">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3318">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3319">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3320">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3321">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3322">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3323">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3324">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3325">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3326">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3327">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3328">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3329">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3330">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="3d78b-3331">DXGI_FORMAT_R16 \_ Синт<sup>фнс</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="3d78b-3332">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3332">Target</span></span> | <span data-ttu-id="3d78b-3333">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3334">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3335">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3335">16</span></span> |
| <span data-ttu-id="3d78b-3336">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3336">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3337">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3337">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3338">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3339">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3340">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3345">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3346">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3347">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3348">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3349">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3350">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3351">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3352">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3353">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3354">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3355">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3356">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3357">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3358">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3359">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3360">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3361">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3362">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3363">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3364">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3365">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3366">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3367">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3368">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3369">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3370">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3371">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3372">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3373">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3374">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3375">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3376">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3377">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3378">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3379">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3380">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="3d78b-3381">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8 (60)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="3d78b-3382">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3382">Target</span></span> | <span data-ttu-id="3d78b-3383">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3384">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3385">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3385">8</span></span> |
| <span data-ttu-id="3d78b-3386">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3386">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3387">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3387">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3388">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3389">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3390">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3395">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3396">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3397">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3398">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3399">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3400">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3401">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3402">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3403">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3404">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3405">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3406">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3407">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3408">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3409">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3410">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3411">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3412">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3413">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3414">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3415">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3416">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3417">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3418">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3419">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3420">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3421">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3422">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3423">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3424">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3425">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3426">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3427">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3428">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3429">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3430">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="3d78b-3431">DXGI_FORMAT_R8 \_ UNORM<sup>фнс</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="3d78b-3432">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3432">Target</span></span> | <span data-ttu-id="3d78b-3433">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3434">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3435">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3435">8</span></span> |
| <span data-ttu-id="3d78b-3436">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3436">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3438">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3438">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3439">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3440">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3441">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3443">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3445">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3447">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3449">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3449">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3451">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3451">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3453">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3454">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3455">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3456">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3457">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3459">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3460">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3460">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3462">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3462">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3464">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3465">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3466">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3467">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3468">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3469">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3470">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3471">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3472">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3473">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3474">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3475">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3476">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3477">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3477">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3479">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3480">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3481">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3482">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3483">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3484">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3485">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3486">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3487">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3488">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3489">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3489">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3491">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="3d78b-3492">DXGI_FORMAT_R8 \_ uint<sup>фнс</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="3d78b-3493">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3493">Target</span></span> | <span data-ttu-id="3d78b-3494">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3495">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3496">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3496">8</span></span> |
| <span data-ttu-id="3d78b-3497">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3497">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3498">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3498">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3499">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3500">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3501">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3506">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3507">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3508">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3509">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3510">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3511">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3513">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3514">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3515">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3516">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3517">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3518">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3519">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3520">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3521">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3522">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3523">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3524">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3525">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3526">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3527">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3528">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3529">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3530">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3531">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3532">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3533">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3534">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3535">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3536">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3537">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3538">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3539">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3540">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3541">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="3d78b-3542">DXGI_FORMAT_R8 \_ Снорм<sup>фнс</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="3d78b-3543">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3543">Target</span></span> | <span data-ttu-id="3d78b-3544">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3545">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3546">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3546">8</span></span> |
| <span data-ttu-id="3d78b-3547">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3547">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3548">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3548">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3549">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3550">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3551">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3556">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3557">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3558">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3559">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3560">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3561">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3563">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3564">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3565">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3566">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3567">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3568">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3569">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3570">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3571">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3572">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3573">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3574">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3575">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3576">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3577">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3578">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3579">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3580">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3581">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3582">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3583">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3584">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3585">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3586">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3587">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3588">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3589">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3590">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3591">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="3d78b-3592">DXGI_FORMAT_R8 \_ Синт<sup>фнс</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="3d78b-3593">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3593">Target</span></span> | <span data-ttu-id="3d78b-3594">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3595">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3596">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3596">8</span></span> |
| <span data-ttu-id="3d78b-3597">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3597">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3598">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3598">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3599">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3600">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3601">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3606">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3607">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3608">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3609">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3610">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3611">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3613">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3614">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3615">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3616">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3617">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3618">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3619">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3620">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3621">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3622">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3623">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3624">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3625">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3626">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3627">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3628">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3629">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3630">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3631">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3632">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3633">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3634">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3635">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3636">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3637">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3638">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3639">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3640">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3641">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="3d78b-3642">DXGI_FORMAT_A8 \_ UNORM<sup>фнс</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="3d78b-3643">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3643">Target</span></span> | <span data-ttu-id="3d78b-3644">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3645">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3646">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-3646">8</span></span> |
| <span data-ttu-id="3d78b-3647">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3647">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3649">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3649">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3650">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3651">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3652">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3654">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3656">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3658">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3660">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3660">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3662">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3662">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3664">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3665">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3666">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3667">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3669">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3670">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3670">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3672">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3672">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3674">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3675">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3676">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3677">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3678">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3679">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3680">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3681">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3682">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3683">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3684">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3685">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3686">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3687">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3687">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3689">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3690">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3691">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3692">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3693">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3694">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3695">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3696">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3697">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3698">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3699">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3699">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3701">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="3d78b-3702">DXGI_FORMAT_R9G9B9E5 \_ Шаредексп<sup>фнк</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="3d78b-3703">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3703">Target</span></span> | <span data-ttu-id="3d78b-3704">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3705">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3706">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-3706">32</span></span> |
| <span data-ttu-id="3d78b-3707">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3707">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3708">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3708">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3709">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3710">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3711">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3716">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3717">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3718">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3719">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3720">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3721">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3722">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3723">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3724">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3725">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3726">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3727">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3728">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3729">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3730">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3731">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3732">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3733">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3734">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3735">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3736">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3737">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3738">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3739">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3740">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3741">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3742">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3743">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3744">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3745">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3746">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3747">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3748">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3749">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3750">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3751">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="3d78b-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>ФНК</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="3d78b-3753">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3753">Target</span></span> | <span data-ttu-id="3d78b-3754">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3755">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3756">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3756">16</span></span> |
| <span data-ttu-id="3d78b-3757">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3757">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3758">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3758">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3759">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3760">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3761">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3766">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3767">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3768">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3769">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3770">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3771">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3772">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3773">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3774">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3775">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3776">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3777">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3778">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3779">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3780">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3781">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3782">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3783">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3784">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3785">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3786">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3787">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3788">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3789">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3790">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3791">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3792">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3793">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3794">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3795">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3796">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3797">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3798">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3799">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3800">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3801">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="3d78b-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>ФНК</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="3d78b-3803">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3803">Target</span></span> | <span data-ttu-id="3d78b-3804">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3805">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3806">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-3806">16</span></span> |
| <span data-ttu-id="3d78b-3807">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3807">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3808">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3808">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3809">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3810">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3811">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3816">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3817">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3818">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3819">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3820">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3821">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3822">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3823">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3824">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3825">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3826">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3827">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3828">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3829">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3830">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3831">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3832">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3833">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3834">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3835">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3836">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3837">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3838">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3839">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3840">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3841">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3842">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3843">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3844">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3845">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3846">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3847">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3848">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3849">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3850">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3851">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="3d78b-3852">DXGI_FORMAT_BC1 \_ нетипизированных<sup>пкк</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="3d78b-3853">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3853">Target</span></span> | <span data-ttu-id="3d78b-3854">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3855">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3856">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-3856">4</span></span> |
| <span data-ttu-id="3d78b-3857">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3857">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-3858">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3858">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3859">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3860">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3861">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-3866">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-3867">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3868">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3869">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3870">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3871">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-3873">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3874">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3875">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3876">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3877">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3878">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3879">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3880">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3881">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3882">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3883">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3884">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3885">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3886">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3887">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3888">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3889">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-3890">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3891">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3892">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3893">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3894">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3895">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3896">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3897">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3898">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3899">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3900">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-3901">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="3d78b-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>фнк</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="3d78b-3903">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3903">Target</span></span> | <span data-ttu-id="3d78b-3904">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3905">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3906">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-3906">4</span></span> |
| <span data-ttu-id="3d78b-3907">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3907">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3909">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3909">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3910">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3911">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3912">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3914">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3917">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3919">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3919">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3921">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3921">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3923">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3924">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3925">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3926">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3927">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3927">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3929">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3930">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3931">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3932">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3933">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3934">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3935">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3936">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3937">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3938">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3939">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3940">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3941">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-3942">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-3943">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3944">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-3945">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-3945">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3947">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3948">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3949">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-3950">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-3951">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-3952">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-3953">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-3954">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-3955">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-3956">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-3957">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3957">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3959">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="3d78b-3960">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>ФНК</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="3d78b-3961">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-3961">Target</span></span> | <span data-ttu-id="3d78b-3962">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-3963">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-3964">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-3964">4</span></span> |
| <span data-ttu-id="3d78b-3965">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-3965">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3967">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-3967">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3968">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3969">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3970">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3972">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-3975">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3977">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3977">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3979">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3979">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3981">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3982">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-3983">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-3984">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-3985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3985">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-3987">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-3988">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3989">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-3990">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-3991">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-3992">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3993">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-3994">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-3995">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-3996">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-3997">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-3998">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-3999">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4000">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4001">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4002">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4003">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4003">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4005">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4006">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4007">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4008">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4009">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4010">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4011">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4012">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4013">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4014">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4015">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4015">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4017">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="3d78b-4018">DXGI_FORMAT_BC2 \_ нетипизированных<sup>пкк</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="3d78b-4019">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4019">Target</span></span> | <span data-ttu-id="3d78b-4020">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4021">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4022">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4022">8</span></span> |
| <span data-ttu-id="3d78b-4023">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4023">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4024">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4024">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4025">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4026">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4027">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4032">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4033">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4034">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4035">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4036">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4037">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4039">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4040">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4041">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4042">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4043">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4044">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4045">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4046">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4047">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4048">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4049">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4050">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4051">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4052">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4053">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4054">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4055">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4056">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4057">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4058">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4059">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4060">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4061">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4062">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4063">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4064">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4065">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4066">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4067">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="3d78b-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>фнк</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="3d78b-4069">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4069">Target</span></span> | <span data-ttu-id="3d78b-4070">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4071">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4072">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4072">8</span></span> |
| <span data-ttu-id="3d78b-4073">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4073">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4075">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4075">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4076">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4077">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4078">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4080">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4083">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4085">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4085">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4087">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4087">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4089">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4090">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4091">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4092">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4093">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4093">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4095">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4096">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4097">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4098">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4099">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4100">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4101">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4102">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4103">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4104">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4105">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4106">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4107">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4108">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4109">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4110">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4111">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4111">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4113">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4114">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4115">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4116">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4117">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4118">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4119">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4120">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4121">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4122">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4123">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4123">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4125">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="3d78b-4126">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>ФНК</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="3d78b-4127">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4127">Target</span></span> | <span data-ttu-id="3d78b-4128">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4129">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4130">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4130">8</span></span> |
| <span data-ttu-id="3d78b-4131">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4131">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4133">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4133">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4134">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4135">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4136">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4138">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4141">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4143">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4143">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4145">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4145">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4147">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4148">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4149">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4150">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4151">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4151">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4153">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4154">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4155">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4156">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4157">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4158">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4159">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4160">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4161">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4162">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4163">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4164">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4165">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4166">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4167">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4168">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4169">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4169">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4171">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4172">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4173">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4174">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4175">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4176">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4177">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4178">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4179">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4180">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4181">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4181">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4183">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="3d78b-4184">DXGI_FORMAT_BC3 \_ нетипизированных<sup>пкк</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="3d78b-4185">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4185">Target</span></span> | <span data-ttu-id="3d78b-4186">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4187">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4188">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4188">8</span></span> |
| <span data-ttu-id="3d78b-4189">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4189">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4190">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4190">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4191">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4192">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4193">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4198">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4199">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4200">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4201">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4202">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4203">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4205">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4206">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4207">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4208">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4209">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4210">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4211">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4212">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4213">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4214">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4215">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4216">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4217">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4218">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4219">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4220">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4221">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4222">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4223">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4224">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4225">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4226">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4227">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4228">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4229">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4230">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4231">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4232">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4233">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="3d78b-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>фнк</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="3d78b-4235">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4235">Target</span></span> | <span data-ttu-id="3d78b-4236">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4237">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4238">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4238">8</span></span> |
| <span data-ttu-id="3d78b-4239">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4239">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4241">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4241">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4242">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4243">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4244">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4246">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4249">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4251">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4251">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4253">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4253">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4255">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4256">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4257">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4258">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4259">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4261">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4262">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4263">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4264">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4265">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4266">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4267">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4268">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4269">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4270">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4271">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4272">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4273">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4274">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4275">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4276">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4277">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4277">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4279">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4280">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4281">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4282">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4283">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4284">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4285">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4286">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4287">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4288">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4289">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4289">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4291">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="3d78b-4292">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>ФНК</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="3d78b-4293">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4293">Target</span></span> | <span data-ttu-id="3d78b-4294">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4295">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4296">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4296">8</span></span> |
| <span data-ttu-id="3d78b-4297">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4297">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4299">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4299">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4300">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4301">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4302">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4304">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4307">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4309">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4309">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4311">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4311">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4313">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4314">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4315">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4316">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4317">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4317">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4319">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4320">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4321">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4322">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4323">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4324">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4325">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4326">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4327">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4328">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4329">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4330">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4331">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4332">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4333">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4334">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4335">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4335">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4337">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4338">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4339">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4340">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4341">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4342">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4343">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4344">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4345">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4346">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4347">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4347">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4349">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="3d78b-4350">DXGI_FORMAT_BC4 \_ нетипизированных<sup>пкк</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="3d78b-4351">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4351">Target</span></span> | <span data-ttu-id="3d78b-4352">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4353">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4354">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-4354">4</span></span> |
| <span data-ttu-id="3d78b-4355">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4355">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4356">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4356">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4357">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4358">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4359">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4364">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4365">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4366">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4367">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4368">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4369">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4371">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4372">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4373">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4374">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4375">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4376">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4377">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4378">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4379">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4380">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4381">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4382">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4383">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4384">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4385">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4386">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4387">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4388">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4389">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4390">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4391">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4392">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4393">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4394">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4395">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4396">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4397">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4398">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4399">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="3d78b-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>фнк</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="3d78b-4401">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4401">Target</span></span> | <span data-ttu-id="3d78b-4402">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4403">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4404">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-4404">4</span></span> |
| <span data-ttu-id="3d78b-4405">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4405">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4406">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4406">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4407">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4408">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4409">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4414">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4415">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4416">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4417">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4418">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4419">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4421">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4422">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4423">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4424">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4425">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4426">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4427">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4428">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4429">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4430">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4431">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4432">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4433">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4434">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4435">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4436">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4437">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4438">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4439">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4440">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4441">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4442">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4443">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4444">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4445">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4446">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4447">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4448">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4449">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="3d78b-4450">DXGI_FORMAT_BC4 \_ Снорм<sup>фнк</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="3d78b-4451">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4451">Target</span></span> | <span data-ttu-id="3d78b-4452">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4453">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4454">4</span><span class="sxs-lookup"><span data-stu-id="3d78b-4454">4</span></span> |
| <span data-ttu-id="3d78b-4455">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4455">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4456">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4456">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4457">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4458">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4459">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4464">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4465">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4466">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4467">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4468">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4469">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4471">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4472">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4473">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4474">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4475">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4476">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4477">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4478">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4479">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4480">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4481">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4482">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4483">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4484">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4485">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4486">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4487">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4488">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4489">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4490">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4491">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4492">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4493">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4494">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4495">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4496">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4497">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4498">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4499">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="3d78b-4500">DXGI_FORMAT_BC5 \_ нетипизированных<sup>пкк</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="3d78b-4501">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4501">Target</span></span> | <span data-ttu-id="3d78b-4502">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4503">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4504">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4504">8</span></span> |
| <span data-ttu-id="3d78b-4505">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4505">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4506">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4506">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4507">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4508">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4509">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4514">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4515">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4516">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4517">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4518">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4519">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4521">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4522">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4523">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4524">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4525">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4526">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4527">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4528">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4529">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4530">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4531">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4532">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4533">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4534">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4535">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4536">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4537">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4538">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4539">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4540">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4541">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4542">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4543">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4544">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4545">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4546">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4547">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4548">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4549">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="3d78b-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>фнк</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="3d78b-4551">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4551">Target</span></span> | <span data-ttu-id="3d78b-4552">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4553">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4554">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4554">8</span></span> |
| <span data-ttu-id="3d78b-4555">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4555">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4556">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4556">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4557">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4558">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4559">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4564">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4565">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4566">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4567">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4568">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4569">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4571">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4572">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4573">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4574">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4575">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4576">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4577">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4578">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4579">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4580">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4581">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4582">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4583">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4584">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4585">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4586">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4587">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4588">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4589">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4590">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4591">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4592">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4593">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4594">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4595">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4596">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4597">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4598">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4599">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="3d78b-4600">DXGI_FORMAT_BC5 \_ Снорм<sup>фнк</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="3d78b-4601">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4601">Target</span></span> | <span data-ttu-id="3d78b-4602">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4603">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4604">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-4604">8</span></span> |
| <span data-ttu-id="3d78b-4605">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4605">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4606">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4606">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4607">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4608">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4609">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4614">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4615">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4616">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4617">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4618">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4619">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4620">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4621">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4622">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4623">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4624">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4625">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4626">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4627">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4628">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4629">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4630">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4631">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4632">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4633">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4634">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4635">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4636">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4637">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4638">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4639">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4640">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4641">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4642">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4643">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4644">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4645">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4646">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4647">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4648">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4649">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="3d78b-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>фнс</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="3d78b-4651">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4651">Target</span></span> | <span data-ttu-id="3d78b-4652">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4653">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4654">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-4654">16</span></span> |
| <span data-ttu-id="3d78b-4655">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4655">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4657">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4657">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4658">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4659">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4660">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4662">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4665">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4667">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4667">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4669">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4669">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4671">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4672">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4673">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4674">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4675">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4675">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4677">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4677">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4679">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4679">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4681">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4681">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4683">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4684">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4685">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4686">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4687">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4688">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4689">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4690">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4691">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4692">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4693">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4694">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4695">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4696">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4696">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4698">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4698">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4700">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4700">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4702">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4702">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4704">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4704">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4706">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4707">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4708">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4709">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4710">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4711">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4712">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4713">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="3d78b-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>фнс</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="3d78b-4715">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4715">Target</span></span> | <span data-ttu-id="3d78b-4716">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4717">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4718">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-4718">16</span></span> |
| <span data-ttu-id="3d78b-4719">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4719">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4721">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4721">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4722">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4723">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4724">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4726">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4729">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4731">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4731">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4733">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4733">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4735">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4736">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4737">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4738">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4739">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4739">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4741">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4742">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4743">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4744">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4745">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4746">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4747">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4748">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4749">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4750">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4751">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4752">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4753">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4754">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4755">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4756">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4757">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4757">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4759">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4760">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4761">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4762">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4763">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4764">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4765">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4766">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4767">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4768">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4769">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4770">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="3d78b-4771">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8A8 (90)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="3d78b-4772">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4772">Target</span></span> | <span data-ttu-id="3d78b-4773">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4774">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4775">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-4775">32</span></span> |
| <span data-ttu-id="3d78b-4776">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4776">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4777">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4777">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4778">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4779">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4780">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4785">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4786">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4787">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4788">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4789">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4790">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4791">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4792">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4793">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4794">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4795">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4796">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4797">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4798">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4799">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4800">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4801">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4802">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4803">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4804">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4805">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4806">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4807">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4808">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4809">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4810">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4811">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-4812">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-4813">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4814">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-4815">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4816">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4817">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-4818">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-4819">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-4820">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="3d78b-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>фнс</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="3d78b-4822">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4822">Target</span></span> | <span data-ttu-id="3d78b-4823">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4824">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4825">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-4825">32</span></span> |
| <span data-ttu-id="3d78b-4826">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4826">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4828">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4828">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4829">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4830">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4831">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4833">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4835">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4837">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4839">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4839">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4841">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4841">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4843">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4844">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4845">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4846">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4847">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4849">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4849">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4851">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4851">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4853">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4853">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4855">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4856">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4857">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4858">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4859">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4860">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4861">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4862">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4863">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4864">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4865">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4866">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4867">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4868">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4868">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4870">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4870">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4872">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4872">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4874">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4874">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4876">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4876">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4878">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4879">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4879">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4881">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4882">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4883">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4883">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4885">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4885">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4887">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4887">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4889">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="3d78b-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>ФНС</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="3d78b-4891">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4891">Target</span></span> | <span data-ttu-id="3d78b-4892">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4893">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4894">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-4894">32</span></span> |
| <span data-ttu-id="3d78b-4895">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4895">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4897">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4897">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4898">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4899">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4900">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4902">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4904">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4906">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4908">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4908">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4910">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4910">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4912">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4913">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4914">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4915">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4916">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4916">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4918">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4918">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4920">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4920">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4922">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4922">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4924">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4925">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4926">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4927">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4928">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4929">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4930">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4931">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4932">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4933">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4934">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4935">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4936">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4937">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4937">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4939">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4939">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4941">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4941">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4943">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4943">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4945">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-4945">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4947">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-4948">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-4948">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4950">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-4951">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-4952">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4952">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-4954">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-4954">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4956">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4956">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-4958">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="3d78b-4959">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8X8 (92)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="3d78b-4960">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-4960">Target</span></span> | <span data-ttu-id="3d78b-4961">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-4962">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-4963">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-4963">32</span></span> |
| <span data-ttu-id="3d78b-4964">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-4964">Format Support</span></span> | \- |
| <span data-ttu-id="3d78b-4965">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-4965">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4966">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4967">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4968">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="3d78b-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-4973">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-4974">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4975">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4976">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-4977">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-4978">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-4979">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-4980">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-4981">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4982">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4983">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-4984">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-4985">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4986">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-4987">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-4988">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-4989">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-4990">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-4991">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-4992">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-4993">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-4994">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4995">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-4996">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-4997">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4998">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-4999">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5000">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5001">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5002">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5003">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5004">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5005">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-5006">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5007">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5008">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="3d78b-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>фнс</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="3d78b-5010">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5010">Target</span></span> | <span data-ttu-id="3d78b-5011">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5012">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5013">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5013">32</span></span> |
| <span data-ttu-id="3d78b-5014">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5014">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5016">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5016">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5017">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5018">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5019">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5021">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5023">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5025">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5027">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5027">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5029">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5029">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5031">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5032">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5033">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5034">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5035">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5037">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5037">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5039">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5039">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5041">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5041">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5043">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5044">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5045">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5046">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5047">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5048">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5049">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5050">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5051">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5052">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5053">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5054">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5055">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5056">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5056">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5058">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5058">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5060">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5060">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5062">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5062">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5064">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5064">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5066">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5067">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5068">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5069">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5070">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5070">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5072">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5072">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5074">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5074">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5076">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="3d78b-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>ФНС</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="3d78b-5078">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5078">Target</span></span> | <span data-ttu-id="3d78b-5079">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5080">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5081">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5081">32</span></span> |
| <span data-ttu-id="3d78b-5082">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5082">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5084">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5084">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5085">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5086">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5087">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5089">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5091">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5093">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5095">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5095">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5097">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5097">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5099">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5100">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5101">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5102">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5103">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5105">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5105">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5107">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5107">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5109">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5109">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5111">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5112">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5113">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5114">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5115">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5116">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5117">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5118">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5119">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5120">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5121">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5122">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5123">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5124">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5124">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5126">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5126">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5128">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5128">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5130">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5130">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5132">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5132">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5134">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5135">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5136">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5137">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5138">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-5139">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5140">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5140">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5142">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="3d78b-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="3d78b-5144">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5144">Target</span></span> | <span data-ttu-id="3d78b-5145">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5146">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5147">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5147">32</span></span> |
| <span data-ttu-id="3d78b-5148">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5148">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5150">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5150">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5151">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5152">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5153">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5155">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5159">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5160">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5161">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5162">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5163">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5164">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5165">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5166">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5167">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5168">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5169">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5170">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5171">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5172">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5173">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5174">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5175">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5176">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5177">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5178">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5179">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5180">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5181">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5182">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5182">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5184">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5185">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5186">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5187">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5188">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5189">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5190">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5191">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5191">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5193">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5193">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5195">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5195">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5197">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5198">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="3d78b-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="3d78b-5200">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5200">Target</span></span> | <span data-ttu-id="3d78b-5201">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5202">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5203">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5203">32</span></span> |
| <span data-ttu-id="3d78b-5204">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5204">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5206">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5206">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5207">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5208">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5209">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5211">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5215">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5216">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5217">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5218">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5219">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5220">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5221">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5222">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5223">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5224">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5225">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5226">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5227">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5228">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5229">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5230">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5231">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5232">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5233">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5234">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5235">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5236">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5237">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5238">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5238">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5240">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5241">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5242">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5243">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5244">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5245">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5246">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5247">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5247">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5249">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5249">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5251">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5251">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5253">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5254">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="3d78b-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="3d78b-5256">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5256">Target</span></span> | <span data-ttu-id="3d78b-5257">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5258">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5259">64</span><span class="sxs-lookup"><span data-stu-id="3d78b-5259">64</span></span> |
| <span data-ttu-id="3d78b-5260">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5260">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5262">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5262">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5263">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5264">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5265">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5267">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5271">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5272">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5273">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5274">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5275">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5276">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5277">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5278">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5279">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5280">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5281">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5282">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5283">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5284">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5285">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5286">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5287">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5288">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5289">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5290">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5291">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5292">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5293">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5294">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5294">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5296">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5297">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5298">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5299">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5300">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5301">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5302">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5303">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5303">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5305">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5305">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5307">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5307">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5309">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5310">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="3d78b-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="3d78b-5312">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5312">Target</span></span> | <span data-ttu-id="3d78b-5313">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5314">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5315">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5315">8</span></span> |
| <span data-ttu-id="3d78b-5316">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5316">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5318">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5318">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5319">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5320">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5321">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5323">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5327">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5328">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5329">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5330">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5331">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5332">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5333">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5334">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5335">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5336">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5337">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5338">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5339">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5340">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5341">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5342">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5343">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5344">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5345">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5346">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5347">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5348">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5349">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5350">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5350">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5352">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5353">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5354">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5355">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5356">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5357">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5358">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5359">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5359">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5361">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5361">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5363">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5363">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5365">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5366">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="3d78b-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="3d78b-5368">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5368">Target</span></span> | <span data-ttu-id="3d78b-5369">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5370">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5371">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-5371">16</span></span> |
| <span data-ttu-id="3d78b-5372">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5372">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5374">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5374">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5375">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5376">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5377">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5379">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5383">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5384">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5385">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5386">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5387">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5388">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5390">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5391">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5392">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5393">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5394">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5395">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5396">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5397">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5398">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5399">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5400">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5401">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5402">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5403">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5404">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5405">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5406">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5406">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5408">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5409">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5410">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5411">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5412">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5413">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5414">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5415">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5415">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5417">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5417">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5419">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5419">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5421">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5422">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="3d78b-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="3d78b-5424">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5424">Target</span></span> | <span data-ttu-id="3d78b-5425">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5426">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5427">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-5427">16</span></span> |
| <span data-ttu-id="3d78b-5428">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5428">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5430">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5430">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5431">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5432">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5433">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5435">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5439">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5440">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5441">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5442">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5443">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5444">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5446">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5447">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5448">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5449">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5450">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5451">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5452">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5453">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5454">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5455">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5456">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5457">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5458">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5459">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5460">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5461">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5462">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5462">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5464">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5465">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5466">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5467">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5468">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5469">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5470">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5471">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5471">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5473">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5473">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5475">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5475">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5477">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5478">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="3d78b-5479">DXGI_FORMAT_420 \_ непрозрачный<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="3d78b-5480">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5480">Target</span></span> | <span data-ttu-id="3d78b-5481">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5482">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5483">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5483">8</span></span> |
| <span data-ttu-id="3d78b-5484">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5484">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5486">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5486">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5487">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5488">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5489">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5491">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5495">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5496">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5497">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5498">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5499">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5500">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5501">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5502">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5503">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5504">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5505">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5506">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5507">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5508">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5509">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5510">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5511">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5512">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5513">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5514">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5515">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5516">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5517">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5518">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="3d78b-5519">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5520">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5521">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5522">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5523">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5524">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5525">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5526">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5526">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5528">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5528">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5530">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5530">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5532">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5533">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="3d78b-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="3d78b-5535">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5535">Target</span></span> | <span data-ttu-id="3d78b-5536">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5537">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5538">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-5538">16</span></span> |
| <span data-ttu-id="3d78b-5539">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5539">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5541">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5541">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5542">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5543">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5544">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5546">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5550">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5551">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5552">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5553">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5554">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5555">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5557">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5558">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5559">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5560">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5561">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5562">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5563">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5564">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5565">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5566">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5567">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5568">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5569">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5570">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5571">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5572">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5573">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5573">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5575">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5576">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5577">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5578">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5579">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5580">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5581">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5582">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5582">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5584">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5584">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5586">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5586">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5588">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5589">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="3d78b-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="3d78b-5591">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5591">Target</span></span> | <span data-ttu-id="3d78b-5592">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5593">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5594">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5594">32</span></span> |
| <span data-ttu-id="3d78b-5595">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5595">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5597">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5597">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5598">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5599">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5600">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5602">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5606">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5607">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5608">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5609">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5610">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5611">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5613">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5614">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5615">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5616">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5617">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5618">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5619">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5620">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5621">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5622">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5623">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5624">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5625">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5626">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5627">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5628">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5629">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5629">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5631">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5632">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5633">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5634">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5635">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5636">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5637">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5638">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5638">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5640">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5640">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5642">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5642">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5644">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5645">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="3d78b-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="3d78b-5647">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5647">Target</span></span> | <span data-ttu-id="3d78b-5648">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5649">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5650">32</span><span class="sxs-lookup"><span data-stu-id="3d78b-5650">32</span></span> |
| <span data-ttu-id="3d78b-5651">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5651">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5653">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5653">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5654">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5655">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5656">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5658">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5662">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5663">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5664">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5665">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5666">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5667">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5669">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5670">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5671">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5672">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5673">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5674">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5675">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5676">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5677">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5678">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5679">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5680">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5681">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5682">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5683">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5684">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5685">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5685">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5687">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5688">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5689">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5690">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5691">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5692">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5693">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5694">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5694">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5696">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5696">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5698">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5698">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5700">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5701">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="3d78b-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="3d78b-5703">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5703">Target</span></span> | <span data-ttu-id="3d78b-5704">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5705">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5706">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5706">8</span></span> |
| <span data-ttu-id="3d78b-5707">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5707">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5709">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5709">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5710">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5711">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5712">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5714">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5718">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5719">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5720">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5721">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5722">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5723">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5724">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5725">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5726">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5727">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5728">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5729">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5730">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5731">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5732">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5733">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5734">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5735">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5736">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5737">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5738">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5739">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5740">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5741">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5741">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5743">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5744">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5745">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5746">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5747">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5748">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5749">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5750">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5750">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5752">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5752">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5754">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5754">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5756">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5757">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="3d78b-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="3d78b-5759">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5759">Target</span></span> | <span data-ttu-id="3d78b-5760">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5761">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5762">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5762">8</span></span> |
| <span data-ttu-id="3d78b-5763">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5763">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5765">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5765">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5766">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5767">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5768">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5770">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5774">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5775">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5776">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5777">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5778">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5779">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5781">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5782">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5783">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5784">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5785">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5786">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5787">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5788">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5789">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5790">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5791">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5792">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5793">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5794">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5795">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5796">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5797">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5797">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5799">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5800">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5801">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5802">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5803">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5804">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5805">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5806">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5807">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5807">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5809">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5810">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5811">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="3d78b-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="3d78b-5813">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5813">Target</span></span> | <span data-ttu-id="3d78b-5814">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5815">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5816">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5816">8</span></span> |
| <span data-ttu-id="3d78b-5817">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5817">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5819">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5819">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5820">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5821">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5822">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5824">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5828">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5829">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5830">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5831">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5832">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5833">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5834">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5835">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5836">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5837">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5838">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5839">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5840">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5841">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5842">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5843">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5844">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5845">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5846">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5847">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5848">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5849">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5850">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5851">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5851">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5853">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5854">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5855">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5856">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5857">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5858">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5859">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5860">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5861">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5861">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5863">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5864">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5865">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="3d78b-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="3d78b-5867">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5867">Target</span></span> | <span data-ttu-id="3d78b-5868">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5869">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5870">8</span><span class="sxs-lookup"><span data-stu-id="3d78b-5870">8</span></span> |
| <span data-ttu-id="3d78b-5871">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5871">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5873">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5873">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5874">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5875">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5876">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5878">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5882">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5883">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5884">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5885">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5886">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5887">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5889">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5890">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5891">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5892">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5893">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5894">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5895">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5896">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5897">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5898">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5899">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5900">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5901">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5902">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5903">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5904">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5905">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5905">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5907">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5908">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5909">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5910">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5911">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5912">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5913">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5914">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5915">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5915">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5917">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5918">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5919">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="3d78b-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="3d78b-5921">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5921">Target</span></span> | <span data-ttu-id="3d78b-5922">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5923">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5924">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-5924">16</span></span> |
| <span data-ttu-id="3d78b-5925">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5925">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-5927">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5927">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5928">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5929">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5930">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5932">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="3d78b-5936">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="3d78b-5937">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5938">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5939">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5940">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5941">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5942">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="3d78b-5943">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="3d78b-5944">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5945">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5946">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-5947">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-5948">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5949">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-5950">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-5951">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-5952">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-5953">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-5954">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-5955">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-5956">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-5957">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5958">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-5959">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-5959">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5961">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5962">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-5963">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-5964">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-5965">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-5966">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-5967">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-5968">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-5969">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5969">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5971">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-5972">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-5973">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="3d78b-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>фнс</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="3d78b-5975">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d78b-5975">Target</span></span> | <span data-ttu-id="3d78b-5976">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3d78b-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="3d78b-5977">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="3d78b-5978">16</span><span class="sxs-lookup"><span data-stu-id="3d78b-5978">16</span></span> |
| <span data-ttu-id="3d78b-5979">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="3d78b-5979">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5981">Буфер</span><span class="sxs-lookup"><span data-stu-id="3d78b-5981">Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5982">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5983">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5984">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="3d78b-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="3d78b-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="3d78b-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5986">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3d78b-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="3d78b-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d78b-5989">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5991">Образец шейдера (только точечная выборка)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5991">Shader sample (point sample only)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5993">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5993">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-5995">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5996">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="3d78b-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="3d78b-5997">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="3d78b-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="3d78b-5998">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="3d78b-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="3d78b-5999">Mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-5999">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-6001">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="3d78b-6001">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="3d78b-6003">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-6004">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="3d78b-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-6005">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="3d78b-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="3d78b-6006">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="3d78b-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="3d78b-6007">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-6008">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="3d78b-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="3d78b-6009">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="3d78b-6010">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="3d78b-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="3d78b-6011">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="3d78b-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="3d78b-6012">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="3d78b-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="3d78b-6013">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="3d78b-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="3d78b-6014">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="3d78b-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="3d78b-6015">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="3d78b-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="3d78b-6016">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-6017">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="3d78b-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="3d78b-6018">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="3d78b-6018">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="3d78b-6020">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-6021">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="3d78b-6022">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="3d78b-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="3d78b-6023">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="3d78b-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="3d78b-6024">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="3d78b-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="3d78b-6025">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="3d78b-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="3d78b-6026">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="3d78b-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="3d78b-6027">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="3d78b-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="3d78b-6028">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="3d78b-6029">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="3d78b-6030">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="3d78b-6031">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="3d78b-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="3d78b-6032">Форматирование заметок</span><span class="sxs-lookup"><span data-stu-id="3d78b-6032">Format notes</span></span>

<span data-ttu-id="3d78b-6033">Назначение формата может изменяться с одного уровня компонентов оборудования на следующий.</span><span class="sxs-lookup"><span data-stu-id="3d78b-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="3d78b-6034"><sup>L</sup> : нетипизированный формат</span><span class="sxs-lookup"><span data-stu-id="3d78b-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="3d78b-6035"><sup>ПК</sup> : частично типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="3d78b-6036"><sup>FCS</sup> : полностью типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="3d78b-6037"><sup>ФНС</sup> : полностью типизированный, неприведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="3d78b-6038"><sup>ПКК</sup> : частично типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="3d78b-6039"><sup>FCC</sup> : полностью типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="3d78b-6040"><sup>ФНК</sup> : полностью типизированный, неприведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="3d78b-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="3d78b-6041"><sup>V</sup> : формат видео</span><span class="sxs-lookup"><span data-stu-id="3d78b-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="3d78b-6042">См. также</span><span class="sxs-lookup"><span data-stu-id="3d78b-6042">Related topics</span></span>

[<span data-ttu-id="3d78b-6043">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="3d78b-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="3d78b-6044">[Реализация теневых буферов для уровня функций Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3d78b-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="3d78b-6045">Сопоставление форматов прежних версий</span><span class="sxs-lookup"><span data-stu-id="3d78b-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="3d78b-6046">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="3d78b-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
