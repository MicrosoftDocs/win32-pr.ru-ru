---
description: В этом разделе указаны форматы ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 10,0.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Поддержка форматов для оборудования Direct3D с уровнем компонентов 10.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262335"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="d8e8a-103">Поддержка форматов для оборудования Direct3D с уровнем компонентов 10.0</span><span class="sxs-lookup"><span data-stu-id="d8e8a-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="d8e8a-104">В этом разделе указаны форматы ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="d8e8a-105">В таблице приводится сводка по поддержке функций с использованием следующего ключа.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="d8e8a-106">Символ</span><span class="sxs-lookup"><span data-stu-id="d8e8a-106">Symbol</span></span>                            | <span data-ttu-id="d8e8a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d8e8a-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d8e8a-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="d8e8a-108">_ *-*\*</span></span>                             | <span data-ttu-id="d8e8a-109">Не разрешено или недоступно.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-109">Disallowed or not available.</span></span>                                                  |
| ![обязательно](images/letter-r.jpg)  | <span data-ttu-id="d8e8a-111">Требуется поддержка оборудования.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-111">Hardware support is required.</span></span>                                                 |
| ![необязательно](images/letter-o.jpg)  | <span data-ttu-id="d8e8a-113">Аппаратная поддержка необязательно. формат аппаратного ускорения может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![зависимых](images/letter-d.jpg) | <span data-ttu-id="d8e8a-115">Требуется, если поддерживается дополнительная функция.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="d8e8a-116">Этот раздел содержит раздел для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-116">This topic contains a section per format.</span></span> <span data-ttu-id="d8e8a-117">*Цель* формата (таблицы содержат по одной строке на каждый целевой объект) может быть типом ресурса, встроенной функцией HLSL или определенной функциональностью, зависящей от конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="d8e8a-118">Чтобы программно проверить поддержку формата в D3D11 и D3D12, обратитесь к статье [Проверка поддержки аппаратных компонентов](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="d8e8a-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="d8e8a-119">Числа форматов в основном, но не все, в возрастающем числовом порядке &mdash; , некоторые из них имеют нечисловой порядок и перечислены вместе с другими соответствующими форматами.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="d8e8a-120">Обратите внимание, что *тип* в имени формата может означать *частичную* типизацию, а не строго типизированный (см. раздел [Format Notes](#format-notes) в конце раздела).</span><span class="sxs-lookup"><span data-stu-id="d8e8a-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="d8e8a-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="d8e8a-122">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-122">Target</span></span> | <span data-ttu-id="d8e8a-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-123">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-124">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-125">0</span><span class="sxs-lookup"><span data-stu-id="d8e8a-125">0</span></span> |
| <span data-ttu-id="d8e8a-126">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-126">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-128">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-128">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-130">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-131">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-132">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-133">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-134">Texture2D</span></span> | \- |
| <span data-ttu-id="d8e8a-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-135">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-136">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-137">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-137">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-138">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-139">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-140">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-141">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-142">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-143">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-144">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-145">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-146">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-147">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-148">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-149">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-150">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-151">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-152">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-153">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-154">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-155">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-156">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-157">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-158">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-159">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-160">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-160">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-162">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-163">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-164">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-165">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-166">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-167">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-168">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-169">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-170">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-171">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-172">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-173">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="d8e8a-174">\_Нетипизированные<sup>ПК</sup> DXGI_FORMAT_R32G32B32A32 (1)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="d8e8a-175">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-175">Target</span></span> | <span data-ttu-id="d8e8a-176">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-176">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-177">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-178">128</span><span class="sxs-lookup"><span data-stu-id="d8e8a-178">128</span></span> |
| <span data-ttu-id="d8e8a-179">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-179">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-181">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-181">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-182">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-183">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-184">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-185">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-187">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-189">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-191">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-193">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-193">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-194">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-195">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-196">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-197">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-198">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-199">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-201">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-202">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-203">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-204">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-205">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-206">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-207">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-208">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-209">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-210">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-211">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-212">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-213">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-214">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-215">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-216">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-217">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-217">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-219">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-220">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-221">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-222">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-223">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-224">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-225">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-225">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-227">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-228">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-229">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-230">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-230">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-232">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="d8e8a-233">DXGI_FORMAT_R32G32B32A32 \_ с<sup></sup> плавающей запятой (2)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="d8e8a-234">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-234">Target</span></span> | <span data-ttu-id="d8e8a-235">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-235">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-236">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-237">128</span><span class="sxs-lookup"><span data-stu-id="d8e8a-237">128</span></span> |
| <span data-ttu-id="d8e8a-238">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-238">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-240">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-240">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-242">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-242">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-244">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-245">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-245">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-247">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-249">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-251">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-253">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-255">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-255">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-257">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-257">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-259">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-260">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-261">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-262">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-263">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-265">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-265">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-267">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-267">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-269">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-269">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-271">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-272">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-273">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-274">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-275">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-276">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-277">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-278">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-279">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-280">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-281">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-282">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-283">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-284">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-284">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-286">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-286">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-288">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-288">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-290">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-290">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-292">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-292">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-294">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-294">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-296">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-297">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-297">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-299">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-300">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-301">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-302">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-302">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-304">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="d8e8a-305">DXGI_FORMAT_R32G32B32A32ое \_ <sup>FCS</sup> /uint (3)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="d8e8a-306">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-306">Target</span></span> | <span data-ttu-id="d8e8a-307">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-307">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-308">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-309">128</span><span class="sxs-lookup"><span data-stu-id="d8e8a-309">128</span></span> |
| <span data-ttu-id="d8e8a-310">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-310">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-312">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-312">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-314">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-314">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-316">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-317">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-317">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-319">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-321">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-323">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-325">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-327">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-327">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-329">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-330">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-331">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-332">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-333">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-334">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-336">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-337">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-337">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-339">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-340">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-340">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-342">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-343">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-344">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-345">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-346">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-347">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-348">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-349">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-350">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-351">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-352">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-353">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-354">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-354">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-356">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-356">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-358">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-358">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-360">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-360">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-362">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-363">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-363">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-365">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-366">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-366">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-368">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-369">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-370">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-371">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-371">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-373">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="d8e8a-374">DXGI_FORMAT_R32G32B32A32 \_ Синт-<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="d8e8a-375">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-375">Target</span></span> | <span data-ttu-id="d8e8a-376">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-376">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-377">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-378">128</span><span class="sxs-lookup"><span data-stu-id="d8e8a-378">128</span></span> |
| <span data-ttu-id="d8e8a-379">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-379">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-381">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-381">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-383">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-383">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-385">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-386">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-386">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-388">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-390">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-392">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-394">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-396">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-396">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-398">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-399">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-400">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-401">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-402">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-403">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-405">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-406">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-406">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-408">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-409">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-410">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-411">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-412">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-413">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-414">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-415">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-416">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-417">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-418">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-419">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-420">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-421">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-422">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-422">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-424">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-424">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-426">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-426">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-428">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-428">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-430">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-431">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-431">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-433">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-434">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-434">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-436">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-437">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-438">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-439">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-439">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-441">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="d8e8a-442">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32B32 (5)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="d8e8a-443">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-443">Target</span></span> | <span data-ttu-id="d8e8a-444">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-444">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-445">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-446">96</span><span class="sxs-lookup"><span data-stu-id="d8e8a-446">96</span></span> |
| <span data-ttu-id="d8e8a-447">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-447">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-449">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-449">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-450">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-451">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-452">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-453">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-455">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-457">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-459">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-461">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-461">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-462">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-463">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-464">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-465">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-466">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-467">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-469">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-470">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-471">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-472">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-473">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-474">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-475">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-476">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-477">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-478">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-479">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-480">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-481">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-482">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-483">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-484">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-485">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-485">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-487">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-488">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-489">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-490">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-491">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-492">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-493">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-493">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-495">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-496">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-497">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-498">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-499">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="d8e8a-500">DXGI_FORMAT_R32G32B32 \_ с<sup></sup> плавающей запятой (6)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="d8e8a-501">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-501">Target</span></span> | <span data-ttu-id="d8e8a-502">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-502">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-503">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-504">96</span><span class="sxs-lookup"><span data-stu-id="d8e8a-504">96</span></span> |
| <span data-ttu-id="d8e8a-505">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-505">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-507">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-507">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-509">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-509">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-511">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-512">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-512">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-514">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-516">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-518">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-520">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-522">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-522">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-524">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-524">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-526">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-527">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-528">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-529">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-530">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-532">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-532">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-534">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-534">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-536">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-536">Blendable RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-538">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-539">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-540">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-541">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-542">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-543">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-544">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-545">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-546">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-547">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-548">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-549">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-550">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-551">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-551">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-553">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-553">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-555">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-555">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-557">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-557">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-559">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-559">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-561">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-561">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-563">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-564">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-564">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-566">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-567">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-568">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-569">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-570">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="d8e8a-571">DXGI_FORMAT_R32G32B32ости \_ uint (7)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="d8e8a-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="d8e8a-572">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-572">Target</span></span> | <span data-ttu-id="d8e8a-573">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-573">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-574">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-575">96</span><span class="sxs-lookup"><span data-stu-id="d8e8a-575">96</span></span> |
| <span data-ttu-id="d8e8a-576">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-576">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-578">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-578">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-580">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-580">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-582">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-583">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-583">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-585">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-587">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-589">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-591">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-593">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-593">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-595">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-596">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-597">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-598">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-599">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-600">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-602">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-603">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-603">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-605">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-606">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-606">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-608">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-609">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-610">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-611">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-612">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-613">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-614">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-615">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-616">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-617">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-618">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-619">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-620">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-620">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-622">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-622">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-624">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-624">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-626">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-626">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-628">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-629">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-629">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-631">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-632">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-632">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-634">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-635">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-636">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-637">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-638">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="d8e8a-639">DXGI_FORMAT_R32G32B32 \_ Синт-<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="d8e8a-640">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-640">Target</span></span> | <span data-ttu-id="d8e8a-641">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-641">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-642">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-643">96</span><span class="sxs-lookup"><span data-stu-id="d8e8a-643">96</span></span> |
| <span data-ttu-id="d8e8a-644">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-644">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-646">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-646">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-648">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-648">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-650">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-651">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-651">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-653">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-655">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-657">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-659">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-661">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-661">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-663">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-664">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-665">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-666">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-667">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-668">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-670">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-671">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-671">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-673">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-674">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-675">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-676">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-677">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-678">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-679">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-680">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-681">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-682">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-683">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-684">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-685">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-686">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-687">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-687">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-689">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-689">4x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-691">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-691">8x Multisample RenderTarget</span></span> | ![зависимых](images/letter-d.jpg) |
| <span data-ttu-id="d8e8a-693">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-693">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-695">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-696">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-696">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-698">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-699">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-699">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-701">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-702">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-703">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-704">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-705">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="d8e8a-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>ПК</sup> нетипизированных типов (9)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="d8e8a-707">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-707">Target</span></span> | <span data-ttu-id="d8e8a-708">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-708">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-709">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-710">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-710">64</span></span> |
| <span data-ttu-id="d8e8a-711">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-711">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-713">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-713">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-714">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-715">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-716">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-717">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-719">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-721">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-723">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-725">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-725">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-726">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-727">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-728">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-729">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-730">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-731">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-733">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-734">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-735">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-736">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-737">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-738">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-739">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-740">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-741">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-742">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-743">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-744">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-745">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-746">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-747">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-748">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-749">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-749">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-751">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-752">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-753">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-754">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-755">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-756">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-757">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-757">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-759">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-760">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-761">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-762">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-762">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-764">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="d8e8a-765">DXGI_FORMAT_R16G16B16A16 \_ с<sup></sup> плавающей запятой (10)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="d8e8a-766">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-766">Target</span></span> | <span data-ttu-id="d8e8a-767">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-767">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-768">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-769">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-769">64</span></span> |
| <span data-ttu-id="d8e8a-770">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-770">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-772">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-772">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-774">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-774">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-776">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-777">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-778">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-780">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-782">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-784">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-786">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-786">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-788">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-788">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-790">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-791">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-792">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-793">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-794">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-796">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-796">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-798">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-798">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-800">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-800">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-802">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-803">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-804">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-805">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-806">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-807">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-808">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-809">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-810">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-811">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-812">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-813">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-814">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-815">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-815">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-817">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-817">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-819">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-819">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-821">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-821">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-823">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-823">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-825">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-825">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-827">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-827">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-829">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-829">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-831">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-832">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-832">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-834">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-834">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-836">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-836">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-838">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="d8e8a-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="d8e8a-840">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-840">Target</span></span> | <span data-ttu-id="d8e8a-841">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-841">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-842">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-843">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-843">64</span></span> |
| <span data-ttu-id="d8e8a-844">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-844">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-846">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-846">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-848">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-848">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-850">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-851">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-852">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-854">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-856">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-858">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-860">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-860">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-862">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-862">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-864">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-865">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-866">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-867">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-868">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-870">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-870">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-872">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-872">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-874">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-874">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-876">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-877">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-878">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-879">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-880">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-881">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-882">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-883">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-884">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-885">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-886">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-887">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-888">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-889">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-889">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-891">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-891">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-893">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-893">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-895">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-895">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-897">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-897">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-899">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-899">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-901">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-902">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-902">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-904">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-905">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-906">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-907">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-907">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-909">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="d8e8a-910">DXGI_FORMAT_R16G16B16A16ое \_ <sup>FCS</sup> /uint (12)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="d8e8a-911">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-911">Target</span></span> | <span data-ttu-id="d8e8a-912">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-912">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-913">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-914">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-914">64</span></span> |
| <span data-ttu-id="d8e8a-915">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-915">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-917">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-917">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-919">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-919">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-921">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-922">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-923">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-925">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-927">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-929">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-931">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-931">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-933">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-934">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-935">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-936">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-937">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-938">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-940">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-941">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-941">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-943">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-944">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-944">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-946">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-947">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-948">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-949">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-950">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-951">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-952">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-953">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-954">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-955">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-956">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-957">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-958">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-958">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-960">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-960">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-962">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-962">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-964">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-964">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-966">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-967">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-967">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-969">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-970">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-970">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-972">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-973">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-974">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-975">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-975">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-977">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="d8e8a-978">DXGI_FORMAT_R16G16B16A16 \_ Снорм<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="d8e8a-979">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-979">Target</span></span> | <span data-ttu-id="d8e8a-980">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-980">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-981">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-982">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-982">64</span></span> |
| <span data-ttu-id="d8e8a-983">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-983">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-985">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-985">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-987">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-987">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-989">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-990">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-991">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-993">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-995">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-997">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-999">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-999">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1001">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1001">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1003">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1004">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1005">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1006">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1007">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1009">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1009">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1011">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1011">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1013">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1014">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1015">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1016">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1017">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1018">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1019">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1020">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1021">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1022">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1023">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1024">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1025">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1026">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1027">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1027">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1029">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1029">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1031">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1031">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1033">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1033">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1035">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1035">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1037">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1037">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1039">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1040">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1040">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1042">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1043">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1044">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1045">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1045">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1047">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="d8e8a-1048">DXGI_FORMAT_R16G16B16A16 \_ Синт-<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="d8e8a-1049">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1049">Target</span></span> | <span data-ttu-id="d8e8a-1050">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1051">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1052">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1052">64</span></span> |
| <span data-ttu-id="d8e8a-1053">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1053">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1055">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1055">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1057">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1057">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1059">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1060">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1061">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1063">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1065">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1067">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1069">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1069">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1071">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1072">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1073">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1074">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1075">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1076">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1076">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1078">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1079">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1079">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1081">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1082">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1083">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1084">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1085">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1086">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1087">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1088">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1089">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1090">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1091">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1092">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1093">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1094">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1095">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1095">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1097">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1097">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1099">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1099">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1101">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1101">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1103">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1104">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1104">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1106">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1107">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1107">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1109">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1110">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1111">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1112">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1112">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1114">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="d8e8a-1115">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32G32 (15)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="d8e8a-1116">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1116">Target</span></span> | <span data-ttu-id="d8e8a-1117">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1118">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1119">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1119">64</span></span> |
| <span data-ttu-id="d8e8a-1120">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1120">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1122">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1122">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1123">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1124">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1125">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1126">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1128">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1130">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1132">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1134">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1135">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1136">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1137">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1138">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1139">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1140">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1142">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1143">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1144">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1145">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1146">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1147">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1148">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1149">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1150">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1151">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1152">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1153">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1154">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1155">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1156">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1157">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1158">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1158">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1160">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1161">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1162">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1163">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1164">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1165">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1166">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1166">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1168">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1169">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1170">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1171">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1172">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="d8e8a-1173">DXGI_FORMAT_R32G32 \_ с<sup></sup> плавающей запятой (16)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="d8e8a-1174">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1174">Target</span></span> | <span data-ttu-id="d8e8a-1175">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1176">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1177">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1177">64</span></span> |
| <span data-ttu-id="d8e8a-1178">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1178">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1180">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1180">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1182">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1182">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1184">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1185">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1185">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1187">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1189">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1191">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1193">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1195">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1195">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1197">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1197">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1199">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1200">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1201">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1202">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1203">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1203">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1205">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1205">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1207">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1207">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1209">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1209">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1211">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1212">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1213">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1214">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1215">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1216">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1217">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1218">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1219">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1220">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1221">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1222">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1223">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1224">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1224">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1226">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1226">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1228">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1228">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1230">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1230">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1232">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1232">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1234">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1234">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1236">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1237">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1237">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1239">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1240">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1241">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1242">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1243">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="d8e8a-1244">DXGI_FORMAT_R32G32 \_ с<sup>FCS</sup> /uint (17)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="d8e8a-1245">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1245">Target</span></span> | <span data-ttu-id="d8e8a-1246">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1247">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1248">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1248">64</span></span> |
| <span data-ttu-id="d8e8a-1249">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1249">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1251">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1251">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1253">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1253">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1255">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1256">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1256">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1258">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1260">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1262">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1264">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1266">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1266">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1268">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1269">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1270">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1271">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1272">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1273">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1273">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1275">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1276">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1276">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1278">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1279">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1279">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1281">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1282">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1283">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1284">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1285">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1286">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1287">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1288">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1289">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1290">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1291">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1292">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1293">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1293">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1295">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1295">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1297">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1297">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1299">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1299">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1301">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1302">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1302">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1304">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1305">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1305">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1307">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1308">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1309">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1310">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1311">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="d8e8a-1312">DXGI_FORMAT_R32G32 \_ Синт-<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="d8e8a-1313">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1313">Target</span></span> | <span data-ttu-id="d8e8a-1314">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1315">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1316">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1316">64</span></span> |
| <span data-ttu-id="d8e8a-1317">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1317">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1319">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1319">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1321">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1321">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1323">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1324">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1324">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1326">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1328">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1330">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1332">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1334">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1334">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1336">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1337">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1338">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1339">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1340">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1341">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1341">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1343">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1344">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1344">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1346">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1347">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1348">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1349">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1350">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1351">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1352">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1353">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1354">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1355">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1356">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1357">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1358">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1359">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1360">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1360">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1362">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1362">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1364">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1364">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1366">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1366">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1368">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1369">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1369">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1371">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1372">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1372">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1374">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1375">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1376">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1377">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1378">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="d8e8a-1379">DXGI_FORMAT_R32G8X24 \_ <sup>ПК</sup> нетипизированного типа (19)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="d8e8a-1380">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1380">Target</span></span> | <span data-ttu-id="d8e8a-1381">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1382">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1383">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1383">64</span></span> |
| <span data-ttu-id="d8e8a-1384">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1384">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1386">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1386">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1387">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1388">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1389">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1390">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1392">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1395">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1397">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1398">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1399">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1400">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1401">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1402">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1403">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1405">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1406">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1407">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1408">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1409">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1410">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1411">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1412">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1413">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1414">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1415">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1416">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1417">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1418">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1419">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1420">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1421">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1421">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1423">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1424">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1425">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1426">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1427">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1428">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1429">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1429">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1431">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1432">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1433">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1434">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1435">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="d8e8a-1436">DXGI_FORMAT_D32 с \_ плавающей запятой \_ S8X24 \_ uint (20)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="d8e8a-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="d8e8a-1437">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1437">Target</span></span> | <span data-ttu-id="d8e8a-1438">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1439">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1440">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1440">64</span></span> |
| <span data-ttu-id="d8e8a-1441">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1441">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1443">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1443">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1444">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1445">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1446">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1447">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1449">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1452">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1454">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1455">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1456">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1457">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1458">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1459">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1460">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1462">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1463">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1464">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1465">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1466">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1466">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1468">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1469">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1470">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1471">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1472">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1473">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1474">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1475">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1476">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1477">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1478">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1479">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1479">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1481">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1481">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1483">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1483">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1485">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1485">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1487">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1488">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1489">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1490">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1490">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1492">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1493">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1494">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1495">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1496">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="d8e8a-1497">\_Нетипизированный X8X24 с плавающей запятой \_ \_ (21)<sup></sup> DXGI_FORMAT_R32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="d8e8a-1498">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1498">Target</span></span> | <span data-ttu-id="d8e8a-1499">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1500">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1501">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1501">64</span></span> |
| <span data-ttu-id="d8e8a-1502">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1502">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1504">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1504">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1505">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1506">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1507">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1508">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1510">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1513">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1515">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1515">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1517">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1517">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1519">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1519">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1521">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1522">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1523">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1524">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1524">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1526">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1527">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1528">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1529">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1530">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1531">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1532">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1533">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1534">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1535">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1536">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1537">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1538">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1539">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1540">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1541">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1542">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1542">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1544">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1545">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1546">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1547">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1548">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1549">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1550">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1550">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1552">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1553">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1554">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1555">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1556">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="d8e8a-1557">DXGI_FORMAT_X32 без \_ типов, \_ G8X24 \_ (22)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="d8e8a-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="d8e8a-1558">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1558">Target</span></span> | <span data-ttu-id="d8e8a-1559">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1560">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1561">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1561">64</span></span> |
| <span data-ttu-id="d8e8a-1562">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1562">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1564">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1564">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1565">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1566">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1567">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1568">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1570">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1573">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1575">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1575">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1577">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1578">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1579">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1580">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1581">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1582">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1582">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1584">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1585">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1586">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1587">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1588">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1589">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1590">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1591">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1592">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1593">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1594">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1595">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1596">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1597">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1598">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1599">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1600">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1600">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1602">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1603">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1604">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1605">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1606">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1607">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1608">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1608">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1610">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1611">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1612">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1613">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1614">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="d8e8a-1615">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R10G10B10A2 (23)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="d8e8a-1616">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1616">Target</span></span> | <span data-ttu-id="d8e8a-1617">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1618">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1619">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1619">32</span></span> |
| <span data-ttu-id="d8e8a-1620">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1620">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1622">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1622">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1623">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1624">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1625">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1626">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1628">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1630">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1632">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1634">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1635">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1636">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1637">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1638">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1639">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1640">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1640">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1642">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1643">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1644">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1645">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1646">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1647">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1648">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1649">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1650">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1651">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1652">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1653">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1654">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1655">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1656">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1657">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1658">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1658">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1660">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1661">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1662">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1663">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1664">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1665">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1666">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1666">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1668">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1669">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1670">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1671">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1671">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1673">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="d8e8a-1674">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="d8e8a-1675">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1675">Target</span></span> | <span data-ttu-id="d8e8a-1676">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1677">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1678">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1678">32</span></span> |
| <span data-ttu-id="d8e8a-1679">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1679">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1681">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1681">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1683">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1683">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1685">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1686">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1687">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1689">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1691">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1693">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1695">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1695">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1697">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1697">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1699">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1700">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1701">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1702">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1703">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1705">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1705">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1707">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1707">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1709">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1709">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1711">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1712">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1713">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1714">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1715">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1716">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1717">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1718">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1719">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1720">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1721">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1722">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1723">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1724">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1724">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1726">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1726">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1728">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1728">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1730">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1730">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1732">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1732">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1734">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1734">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1736">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1736">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1738">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1738">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1740">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1741">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1741">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1743">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1743">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1745">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1745">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1747">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="d8e8a-1748">DXGI_FORMAT_R10G10B10A2ое \_ <sup>FCS</sup> /uint (25)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="d8e8a-1749">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1749">Target</span></span> | <span data-ttu-id="d8e8a-1750">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1751">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1752">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1752">32</span></span> |
| <span data-ttu-id="d8e8a-1753">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1753">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1755">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1755">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1757">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1757">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1759">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1760">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1761">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1763">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1765">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1767">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1769">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1769">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1771">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1772">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1773">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1774">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1775">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1776">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1778">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1779">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1779">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1781">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1782">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1782">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1784">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1785">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1786">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1787">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1788">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1789">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1790">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1791">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1792">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1793">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1794">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1795">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1796">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1796">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1798">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1798">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1800">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1800">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1802">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1802">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1804">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1805">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1805">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1807">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1808">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1808">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1810">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1811">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1812">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1813">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1813">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1815">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="d8e8a-1816">DXGI_FORMAT_R10G10B10 \_ XR \_ смещение \_ A2 \_ UNORM<sup></sup> (89)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="d8e8a-1817">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1817">Target</span></span> | <span data-ttu-id="d8e8a-1818">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1819">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1820">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1820">32</span></span> |
| <span data-ttu-id="d8e8a-1821">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1821">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1823">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1823">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1824">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1825">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1826">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1828">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-1832">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1833">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1834">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1835">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1836">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1837">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-1839">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1840">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1841">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1842">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1843">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1844">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1845">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1846">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1847">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1848">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1849">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1850">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1851">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1852">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1853">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1854">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1855">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1855">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1857">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1858">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1859">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1860">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1861">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1862">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1862">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1864">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1864">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1866">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1867">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1867">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1869">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1869">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1871">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1871">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1873">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="d8e8a-1874">DXGI_FORMAT_R11G11B10 \_ <sup>ФНС</sup> с плавающей запятой (26)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="d8e8a-1875">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1875">Target</span></span> | <span data-ttu-id="d8e8a-1876">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1877">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1878">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1878">32</span></span> |
| <span data-ttu-id="d8e8a-1879">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1879">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1881">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1881">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1883">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1883">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1885">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1886">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1887">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1889">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1891">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1893">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1895">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1895">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1897">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1897">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1899">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1900">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1901">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1902">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1903">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1905">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1905">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1907">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1907">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1909">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1909">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1911">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1912">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1913">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1914">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1915">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1916">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1917">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1918">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1919">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1920">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1921">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1922">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1923">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1924">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1924">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1926">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1926">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1928">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1928">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1930">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1930">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1932">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1932">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1934">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1934">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-1936">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1937">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-1938">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1939">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1940">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1941">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-1942">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="d8e8a-1943">DXGI_FORMAT_R8G8B8A8 \_ <sup>ПК</sup> нетипизированных типов (27)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="d8e8a-1944">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1944">Target</span></span> | <span data-ttu-id="d8e8a-1945">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-1946">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-1947">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1947">32</span></span> |
| <span data-ttu-id="d8e8a-1948">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1948">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1950">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1950">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1951">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1952">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1953">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1954">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1956">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1958">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1960">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1962">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-1963">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1964">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1965">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-1966">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-1967">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-1968">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1968">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1970">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-1971">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1972">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1973">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-1974">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-1975">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1976">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-1977">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-1978">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-1979">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1980">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-1981">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-1982">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-1983">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-1984">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1985">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-1986">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1986">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1988">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1989">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-1990">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-1991">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-1992">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-1993">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-1994">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1994">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-1996">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-1997">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-1998">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-1999">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-1999">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2001">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="d8e8a-2002">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="d8e8a-2003">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2003">Target</span></span> | <span data-ttu-id="d8e8a-2004">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2005">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2006">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2006">32</span></span> |
| <span data-ttu-id="d8e8a-2007">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2007">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2009">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2009">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2011">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2011">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2013">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2014">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2015">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2017">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2019">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2021">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2023">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2023">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2025">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2025">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2027">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2028">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2029">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2030">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2031">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2031">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2033">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2033">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2035">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2035">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2037">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2037">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2039">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2040">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2041">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2042">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2043">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2044">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2045">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2046">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2047">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2048">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2049">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2050">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2051">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2052">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2052">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2054">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2054">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2056">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2056">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2058">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2058">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2060">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2060">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2062">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2062">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2064">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2064">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2066">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2066">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2068">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2069">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2069">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2071">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2071">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2073">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2073">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2075">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="d8e8a-2076">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="d8e8a-2077">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2077">Target</span></span> | <span data-ttu-id="d8e8a-2078">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2079">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2080">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2080">32</span></span> |
| <span data-ttu-id="d8e8a-2081">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2081">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2083">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2083">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2084">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2085">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2086">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2087">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2089">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2091">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2093">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2095">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2095">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2097">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2097">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2099">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2100">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2101">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2102">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2103">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2105">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2105">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2107">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2107">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2109">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2109">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2111">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2112">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2113">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2114">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2115">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2116">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2117">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2118">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2119">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2120">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2121">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2122">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2123">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2124">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2124">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2126">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2126">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2128">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2128">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2130">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2130">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2132">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2132">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2134">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2134">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2136">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2136">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2138">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2138">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2140">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2141">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2141">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2143">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2143">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2145">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2145">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2147">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="d8e8a-2148">DXGI_FORMAT_R8G8B8A8ое \_ <sup>FCS</sup> /uint (30)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="d8e8a-2149">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2149">Target</span></span> | <span data-ttu-id="d8e8a-2150">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2151">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2152">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2152">32</span></span> |
| <span data-ttu-id="d8e8a-2153">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2153">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2155">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2155">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2157">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2157">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2159">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2160">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2161">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2163">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2165">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2167">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2169">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2169">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2171">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2172">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2173">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2174">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2175">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2176">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2176">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2178">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2179">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2179">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2181">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2182">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2182">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2184">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2185">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2186">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2187">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2188">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2189">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2190">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2191">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2192">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2193">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2194">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2195">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2196">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2196">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2198">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2198">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2200">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2200">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2202">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2202">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2204">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2205">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2205">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2207">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2208">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2208">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2210">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2211">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2212">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2213">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2213">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2215">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="d8e8a-2216">DXGI_FORMAT_R8G8B8A8 \_ снормного<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="d8e8a-2217">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2217">Target</span></span> | <span data-ttu-id="d8e8a-2218">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2219">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2220">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2220">32</span></span> |
| <span data-ttu-id="d8e8a-2221">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2221">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2223">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2223">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2225">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2225">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2227">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2228">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2229">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2231">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2233">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2235">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2237">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2237">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2239">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2239">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2241">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2242">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2243">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2244">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2245">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2245">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2247">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2247">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2249">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2249">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2251">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2252">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2253">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2254">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2255">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2256">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2257">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2258">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2259">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2260">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2261">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2262">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2263">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2264">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2265">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2265">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2267">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2267">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2269">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2269">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2271">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2271">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2273">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2273">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2275">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2275">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2277">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2278">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2278">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2280">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2281">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2282">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2283">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2283">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2285">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="d8e8a-2286">DXGI_FORMAT_R8G8B8A8 \_ Синт-<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="d8e8a-2287">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2287">Target</span></span> | <span data-ttu-id="d8e8a-2288">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2289">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2290">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2290">32</span></span> |
| <span data-ttu-id="d8e8a-2291">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2291">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2293">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2293">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2295">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2295">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2297">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2298">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2299">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2301">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2303">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2305">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2307">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2307">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2309">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2310">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2311">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2312">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2313">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2314">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2314">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2316">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2317">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2317">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2319">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2320">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2321">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2322">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2323">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2324">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2325">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2326">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2327">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2328">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2329">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2330">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2331">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2332">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2333">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2333">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2335">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2335">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2337">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2337">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2339">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2339">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2341">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2342">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2342">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2344">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2345">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2345">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2347">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2348">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2349">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2350">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2350">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2352">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="d8e8a-2353">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16G16 (33)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="d8e8a-2354">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2354">Target</span></span> | <span data-ttu-id="d8e8a-2355">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2356">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2357">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2357">32</span></span> |
| <span data-ttu-id="d8e8a-2358">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2358">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2360">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2360">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2361">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2362">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2363">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2364">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2366">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2368">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2370">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2372">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-2373">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2374">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2375">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2376">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2377">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2378">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2380">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2381">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2382">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2383">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2384">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2385">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2386">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2387">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2388">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2389">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2390">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2391">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2392">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2393">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2394">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2395">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2396">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2396">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2398">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2399">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2400">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-2401">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2402">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2403">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2404">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2404">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2406">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2407">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2408">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2409">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2410">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="d8e8a-2411">DXGI_FORMAT_R16G16 \_ с<sup></sup> плавающей запятой (34)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="d8e8a-2412">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2412">Target</span></span> | <span data-ttu-id="d8e8a-2413">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2414">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2415">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2415">32</span></span> |
| <span data-ttu-id="d8e8a-2416">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2416">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2418">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2418">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2420">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2420">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2422">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2423">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2424">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2426">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2428">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2430">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2432">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2432">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2434">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2434">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2436">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2437">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2438">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2439">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2440">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2440">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2442">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2442">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2444">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2444">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2446">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2446">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2448">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2449">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2450">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2451">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2452">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2453">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2454">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2455">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2456">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2457">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2458">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2459">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2460">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2461">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2461">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2463">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2463">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2465">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2465">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2467">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2467">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2469">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2469">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2471">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2471">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2473">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2474">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2474">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2476">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2477">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2478">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2479">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2480">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="d8e8a-2481">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="d8e8a-2482">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2482">Target</span></span> | <span data-ttu-id="d8e8a-2483">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2484">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2485">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2485">32</span></span> |
| <span data-ttu-id="d8e8a-2486">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2486">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2488">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2488">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2490">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2490">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2492">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2493">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2494">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2496">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2498">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2500">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2502">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2502">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2504">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2504">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2506">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2507">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2508">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2509">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2510">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2512">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2512">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2514">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2514">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2516">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2516">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2518">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2519">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2520">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2521">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2522">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2523">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2524">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2525">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2526">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2527">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2528">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2529">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2530">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2531">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2531">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2533">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2533">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2535">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2535">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2537">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2537">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2539">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2539">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2541">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2541">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2543">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2544">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2544">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2546">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2547">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2548">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2549">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2550">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="d8e8a-2551">DXGI_FORMAT_R16G16ое \_ <sup>FCS</sup> /uint (36)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="d8e8a-2552">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2552">Target</span></span> | <span data-ttu-id="d8e8a-2553">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2554">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2555">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2555">32</span></span> |
| <span data-ttu-id="d8e8a-2556">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2556">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2558">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2558">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2560">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2560">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2562">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2563">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2564">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2566">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2568">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2570">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2572">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2572">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2574">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2575">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2576">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2577">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2578">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2579">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2581">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2582">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2582">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2584">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2585">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2585">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2587">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2588">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2589">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2590">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2591">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2592">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2593">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2594">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2595">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2596">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2597">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2598">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2599">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2599">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2601">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2601">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2603">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2603">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2605">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2605">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2607">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2608">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2608">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2610">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2611">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2611">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2613">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2614">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2615">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2616">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2617">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="d8e8a-2618">DXGI_FORMAT_R16G16 \_ Снорм<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="d8e8a-2619">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2619">Target</span></span> | <span data-ttu-id="d8e8a-2620">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2621">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2622">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2622">32</span></span> |
| <span data-ttu-id="d8e8a-2623">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2623">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2625">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2625">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2627">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2627">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2629">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2630">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2631">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2633">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2635">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2637">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2639">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2639">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2641">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2641">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2643">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2644">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2645">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2646">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2647">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2647">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2649">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2649">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2651">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2651">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2653">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2654">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2655">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2656">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2657">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2658">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2659">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2660">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2661">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2662">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2663">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2664">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2665">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2666">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2667">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2667">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2669">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2669">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2671">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2671">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2673">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2673">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2675">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2675">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2677">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2677">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2679">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2680">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2680">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2682">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2683">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2684">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2685">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2686">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="d8e8a-2687">DXGI_FORMAT_R16G16 \_ Синт-<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="d8e8a-2688">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2688">Target</span></span> | <span data-ttu-id="d8e8a-2689">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2690">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2691">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2691">32</span></span> |
| <span data-ttu-id="d8e8a-2692">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2692">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2694">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2694">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2696">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2696">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2698">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2699">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2700">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2702">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2704">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2706">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2708">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2708">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2710">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2711">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2712">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2713">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2714">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2715">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2717">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2718">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2718">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2720">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2721">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2722">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2723">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2724">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2725">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2726">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2727">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2728">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2729">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2730">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2731">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2732">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2733">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2734">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2734">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2736">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2736">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2738">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2738">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2740">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2740">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2742">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2743">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2743">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2745">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2746">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2746">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2748">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2749">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2750">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2751">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-2752">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="d8e8a-2753">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R32 (39)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="d8e8a-2754">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2754">Target</span></span> | <span data-ttu-id="d8e8a-2755">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2756">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2757">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2757">32</span></span> |
| <span data-ttu-id="d8e8a-2758">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2758">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2760">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2760">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2761">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2762">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2763">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2764">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2766">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2768">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2770">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2772">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-2773">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2774">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2775">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2776">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2777">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2778">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2778">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2780">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2781">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2782">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2783">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2784">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2785">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2786">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2787">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2788">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2789">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2790">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2791">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2792">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2793">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2794">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2795">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2796">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2796">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2798">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2799">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2800">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-2801">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2802">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2803">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2804">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2804">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2806">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2807">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2808">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2809">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2809">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2811">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="d8e8a-2812">DXGI_FORMAT_D32 \_ с<sup></sup> плавающей запятой (40)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="d8e8a-2813">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2813">Target</span></span> | <span data-ttu-id="d8e8a-2814">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2815">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2816">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2816">32</span></span> |
| <span data-ttu-id="d8e8a-2817">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2817">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2819">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2819">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2820">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2821">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2822">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2823">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2825">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2828">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2830">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-2831">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2832">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2833">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2834">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2835">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2836">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2838">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2839">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2840">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2841">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2842">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2842">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2844">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2845">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2846">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2847">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2848">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2849">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2850">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2851">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2852">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2853">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2854">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2855">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2855">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2857">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2857">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2859">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2859">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2861">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2861">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2863">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-2864">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2865">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2866">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2866">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2868">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2869">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2870">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2871">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2871">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2873">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="d8e8a-2874">DXGI_FORMAT_R32 \_ с<sup></sup> плавающей запятой (41)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="d8e8a-2875">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2875">Target</span></span> | <span data-ttu-id="d8e8a-2876">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2877">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2878">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2878">32</span></span> |
| <span data-ttu-id="d8e8a-2879">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2879">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2881">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2881">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2883">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2883">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2885">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-2886">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2886">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2888">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2890">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2892">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2894">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2896">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2896">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2898">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2898">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2900">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2900">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2902">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2903">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2904">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2905">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2905">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2907">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2907">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2909">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2909">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2911">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2911">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2913">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-2914">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2915">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2916">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2917">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2918">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2919">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2920">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2921">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2922">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2923">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2924">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2925">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2926">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2926">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2928">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2928">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2930">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2930">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2932">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2932">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2934">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2934">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2936">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2936">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2938">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-2939">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2939">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2941">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-2942">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-2943">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-2944">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2944">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2946">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="d8e8a-2947">DXGI_FORMAT_R32ое \_ <sup>FCS</sup> /uint (42)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="d8e8a-2948">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2948">Target</span></span> | <span data-ttu-id="d8e8a-2949">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-2950">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-2951">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2951">32</span></span> |
| <span data-ttu-id="d8e8a-2952">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2952">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2954">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2954">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2956">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2956">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2958">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2958">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2960">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2960">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2962">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2964">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2966">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2968">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2970">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2970">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2972">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2973">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2974">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-2975">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-2976">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-2977">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2977">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2979">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-2980">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2980">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2982">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-2983">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2983">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-2985">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-2986">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2987">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-2988">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-2989">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-2990">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-2991">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-2992">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-2993">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-2994">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-2995">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2996">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-2997">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2997">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-2999">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-2999">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3001">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3001">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3003">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3003">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3005">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3006">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3006">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3008">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3009">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3009">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3011">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3012">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3013">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3014">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3014">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3016">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="d8e8a-3017">DXGI_FORMAT_R32 \_ Синт-<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="d8e8a-3018">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3018">Target</span></span> | <span data-ttu-id="d8e8a-3019">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3020">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3021">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3021">32</span></span> |
| <span data-ttu-id="d8e8a-3022">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3022">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3024">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3024">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3026">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3026">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3028">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3029">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3029">Stream Output Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3031">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3033">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3035">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3037">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3039">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3039">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3041">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3042">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3043">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3044">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3045">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3046">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3046">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3048">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3049">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3049">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3051">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3052">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3053">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3054">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3055">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3056">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3057">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3058">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3059">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3060">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3061">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3062">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3063">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3064">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3065">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3065">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3067">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3067">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3069">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3069">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3071">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3071">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3073">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3074">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3074">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3076">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3077">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3077">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3079">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3080">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3081">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3082">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3082">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3084">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="d8e8a-3085">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R24G8 (44)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="d8e8a-3086">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3086">Target</span></span> | <span data-ttu-id="d8e8a-3087">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3088">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3089">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3089">32</span></span> |
| <span data-ttu-id="d8e8a-3090">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3090">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3092">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3092">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3093">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3094">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3095">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3096">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3098">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3101">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3103">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-3104">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3105">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3106">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3107">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3108">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3109">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3111">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3112">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3113">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3114">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3115">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3116">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3117">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3118">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3119">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3120">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3121">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3122">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3123">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3124">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3125">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3126">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3127">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3127">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3129">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3130">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3131">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-3132">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3133">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3134">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3135">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3135">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3137">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3138">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3139">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3140">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3141">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="d8e8a-3142">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="d8e8a-3143">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3143">Target</span></span> | <span data-ttu-id="d8e8a-3144">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3145">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3146">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3146">32</span></span> |
| <span data-ttu-id="d8e8a-3147">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3147">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3149">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3149">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3150">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3151">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3152">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3153">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3155">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3158">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3160">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-3161">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3162">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3163">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3164">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3165">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3166">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3168">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3169">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3170">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3171">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3172">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3172">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3174">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3175">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3176">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3177">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3178">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3179">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3180">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3181">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3182">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3183">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3184">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3185">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3185">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3187">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3187">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3189">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3189">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3191">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3191">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3193">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3194">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3195">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3196">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3196">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3198">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3199">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3200">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3201">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3202">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="d8e8a-3203">DXGI_FORMAT_R24 \_ UNORM \_ x8 с \_ нетипизированным типом (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="d8e8a-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="d8e8a-3204">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3204">Target</span></span> | <span data-ttu-id="d8e8a-3205">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3206">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3207">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3207">32</span></span> |
| <span data-ttu-id="d8e8a-3208">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3208">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3210">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3210">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3211">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3212">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3213">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3214">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3216">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3219">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3221">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3221">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3223">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3223">Shader sample (any filter)</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3225">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3225">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3227">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3228">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3229">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3230">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3230">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3232">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3233">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3234">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3235">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3236">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3237">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3238">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3239">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3240">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3241">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3242">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3243">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3244">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3245">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3246">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3247">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3248">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3248">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3250">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3251">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3252">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-3253">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3254">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3255">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3256">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3256">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3258">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3259">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3260">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3261">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3262">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="d8e8a-3263">DXGI_FORMAT_X24 \_ нетипизированного \_ G8ого типа \_ uint (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="d8e8a-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="d8e8a-3264">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3264">Target</span></span> | <span data-ttu-id="d8e8a-3265">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3266">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3267">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3267">32</span></span> |
| <span data-ttu-id="d8e8a-3268">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3268">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3270">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3270">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3271">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3272">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3273">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3274">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3276">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3279">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3281">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3281">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3283">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3284">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3285">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3286">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3287">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3288">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3288">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3290">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3291">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3292">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3293">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3294">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3295">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3296">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3297">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3298">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3299">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3300">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3301">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3302">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3303">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3304">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3305">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3306">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3306">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3308">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3309">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3310">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-3311">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3312">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3313">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3314">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3314">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3316">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3317">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3318">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3319">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3320">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="d8e8a-3321">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8G8 (48)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="d8e8a-3322">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3322">Target</span></span> | <span data-ttu-id="d8e8a-3323">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3324">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3325">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3325">16</span></span> |
| <span data-ttu-id="d8e8a-3326">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3326">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3328">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3328">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3329">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3330">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3331">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3332">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3334">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3336">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3338">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3340">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-3341">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3342">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3343">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3344">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3345">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3346">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3346">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3348">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3349">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3350">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3351">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3352">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3353">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3354">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3355">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3356">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3357">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3358">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3359">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3360">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3361">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3362">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3363">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3364">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3364">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3366">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3367">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3368">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-3369">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3370">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3371">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3372">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3372">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3374">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3375">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3376">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3377">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3378">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="d8e8a-3379">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="d8e8a-3380">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3380">Target</span></span> | <span data-ttu-id="d8e8a-3381">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3382">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3383">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3383">16</span></span> |
| <span data-ttu-id="d8e8a-3384">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3384">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3386">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3386">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3388">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3388">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3390">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3391">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3392">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3394">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3396">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3398">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3400">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3400">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3402">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3402">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3404">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3405">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3406">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3407">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3408">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3408">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3410">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3410">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3412">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3412">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3414">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3414">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3416">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3417">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3418">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3419">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3420">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3421">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3422">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3423">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3424">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3425">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3426">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3427">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3428">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3429">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3429">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3431">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3431">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3433">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3433">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3435">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3435">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3437">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3437">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3439">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3439">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3441">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3442">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3442">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3444">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3445">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3446">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3447">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3447">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3449">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="d8e8a-3450">DXGI_FORMAT_R8G8ое \_ <sup>FCS</sup> /uint (50)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="d8e8a-3451">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3451">Target</span></span> | <span data-ttu-id="d8e8a-3452">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3453">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3454">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3454">16</span></span> |
| <span data-ttu-id="d8e8a-3455">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3455">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3457">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3457">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3459">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3459">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3461">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3462">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3463">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3465">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3467">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3469">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3471">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3471">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3473">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3474">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3475">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3476">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3477">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3478">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3480">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3481">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3481">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3483">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3484">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3484">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3486">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3487">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3488">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3489">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3490">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3491">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3492">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3493">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3494">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3495">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3496">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3497">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3498">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3498">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3500">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3500">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3502">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3502">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3504">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3504">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3506">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3507">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3507">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3509">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3510">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3510">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3512">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3513">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3514">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3515">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3516">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="d8e8a-3517">DXGI_FORMAT_R8G8 \_ Снорм<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="d8e8a-3518">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3518">Target</span></span> | <span data-ttu-id="d8e8a-3519">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3520">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3521">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3521">16</span></span> |
| <span data-ttu-id="d8e8a-3522">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3522">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3524">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3524">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3526">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3526">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3528">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3529">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3530">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3532">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3534">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3536">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3538">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3538">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3540">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3540">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3542">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3543">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3544">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3545">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3546">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3546">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3548">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3548">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3550">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3550">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3552">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3553">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3554">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3555">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3556">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3557">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3558">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3559">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3560">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3561">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3562">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3563">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3564">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3565">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3566">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3566">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3568">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3568">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3570">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3570">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3572">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3572">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3574">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3574">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3576">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3576">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3578">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3579">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3579">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3581">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3582">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3583">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3584">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3585">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="d8e8a-3586">DXGI_FORMAT_R8G8 \_ Синт-<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="d8e8a-3587">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3587">Target</span></span> | <span data-ttu-id="d8e8a-3588">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3589">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3590">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3590">16</span></span> |
| <span data-ttu-id="d8e8a-3591">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3591">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3593">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3593">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3595">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3595">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3597">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3598">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3599">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3601">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3603">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3605">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3607">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3607">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3609">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3610">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3611">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3612">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3613">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3614">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3616">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3617">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3617">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3619">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3620">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3621">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3622">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3623">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3624">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3625">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3626">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3627">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3628">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3629">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3630">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3631">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3632">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3633">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3633">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3635">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3635">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3637">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3637">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3639">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3639">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3641">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3642">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3642">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3644">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3645">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3645">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3647">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3648">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3649">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3650">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-3651">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="d8e8a-3652">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R16 (53)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="d8e8a-3653">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3653">Target</span></span> | <span data-ttu-id="d8e8a-3654">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3655">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3656">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3656">16</span></span> |
| <span data-ttu-id="d8e8a-3657">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3657">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3659">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3659">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3660">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3661">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3662">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3663">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3665">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3667">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3669">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3671">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-3672">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3673">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3674">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3675">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3676">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3677">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3677">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3679">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3680">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3681">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3682">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3683">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3684">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3685">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3686">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3687">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3688">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3689">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3690">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3691">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3692">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3693">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3694">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3695">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3695">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3697">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3698">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3699">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-3700">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3701">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3702">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3703">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3703">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3705">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3706">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3707">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3708">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3708">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3710">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="d8e8a-3711">DXGI_FORMAT_R16 \_ с<sup></sup> плавающей запятой (54)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="d8e8a-3712">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3712">Target</span></span> | <span data-ttu-id="d8e8a-3713">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3714">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3715">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3715">16</span></span> |
| <span data-ttu-id="d8e8a-3716">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3716">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3718">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3718">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3720">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3720">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3722">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3723">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3724">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3726">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3728">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3730">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3732">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3732">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3734">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3734">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3736">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3737">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3738">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3739">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3740">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3742">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3742">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3744">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3744">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3746">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3746">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3748">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3749">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3750">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3751">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3752">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3753">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3754">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3755">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3756">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3757">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3758">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3759">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3760">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3761">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3761">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3763">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3763">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3765">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3765">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3767">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3767">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3769">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3769">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3771">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3771">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3773">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3774">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3774">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3776">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3777">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3778">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3779">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3779">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3781">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="d8e8a-3782">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="d8e8a-3783">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3783">Target</span></span> | <span data-ttu-id="d8e8a-3784">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3785">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3786">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3786">16</span></span> |
| <span data-ttu-id="d8e8a-3787">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3787">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3789">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3789">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3790">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3791">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3792">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3793">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3795">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3798">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3800">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-3801">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3802">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3803">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3804">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3805">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3806">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3808">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3809">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3810">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3811">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3812">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3812">Depth/Stencil Target</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3814">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3815">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3816">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3817">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3818">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3819">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3820">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3821">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3822">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3823">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3824">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3825">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3825">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3827">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3827">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3829">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3829">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3831">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3831">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3833">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3834">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3835">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3836">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3836">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3838">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3839">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3840">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3841">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3841">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3843">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="d8e8a-3844">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="d8e8a-3845">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3845">Target</span></span> | <span data-ttu-id="d8e8a-3846">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3847">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3848">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3848">16</span></span> |
| <span data-ttu-id="d8e8a-3849">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3849">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3851">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3851">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3853">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3853">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3855">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3856">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3857">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3859">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3861">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3863">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3865">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3865">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3867">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3867">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3869">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3869">Shader sample\_c (comparison filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3871">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3872">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3873">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3874">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3874">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3876">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3876">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3878">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3878">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3880">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3880">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3882">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-3883">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3884">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3885">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3886">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3887">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3888">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3889">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3890">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3891">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3892">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3893">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3894">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3895">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3895">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3897">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3897">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3899">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3899">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3901">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3901">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3903">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3903">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3905">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3905">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3907">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3908">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3908">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3910">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3911">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3912">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3913">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3913">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3915">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="d8e8a-3916">DXGI_FORMAT_R16ое \_ <sup>FCS</sup> /uint (57)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="d8e8a-3917">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3917">Target</span></span> | <span data-ttu-id="d8e8a-3918">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3919">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3920">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3920">16</span></span> |
| <span data-ttu-id="d8e8a-3921">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3921">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3923">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3923">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3925">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3925">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3927">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3927">Input Assembler Index Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3929">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3930">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3932">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3934">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3936">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3938">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3938">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3940">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3941">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3942">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-3943">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-3944">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-3945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3945">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3947">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-3948">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3948">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3950">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-3951">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3951">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3953">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-3954">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3955">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-3956">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-3957">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-3958">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-3959">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-3960">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-3961">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-3962">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-3963">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3964">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-3965">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3965">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3967">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3967">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3969">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3969">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3971">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3971">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3973">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-3974">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3974">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-3976">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-3977">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3977">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3979">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-3980">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-3981">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-3982">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3982">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3984">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="d8e8a-3985">DXGI_FORMAT_R16 \_ Снорм<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="d8e8a-3986">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3986">Target</span></span> | <span data-ttu-id="d8e8a-3987">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-3988">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-3989">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3989">16</span></span> |
| <span data-ttu-id="d8e8a-3990">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3990">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3992">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3992">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3994">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3994">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-3996">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3997">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-3998">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4000">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4002">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4004">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4006">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4006">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4008">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4008">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4010">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4011">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4012">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4013">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4014">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4014">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4016">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4016">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4018">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4018">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4020">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4021">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4022">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4023">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4024">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4025">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4026">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4027">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4028">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4029">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4030">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4031">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4032">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4033">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4034">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4034">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4036">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4036">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4038">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4038">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4040">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4040">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4042">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4042">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4044">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4044">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4046">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4047">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4047">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4049">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4050">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4051">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4052">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4052">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4054">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="d8e8a-4055">DXGI_FORMAT_R16 \_ Синт-<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="d8e8a-4056">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4056">Target</span></span> | <span data-ttu-id="d8e8a-4057">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4058">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4059">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4059">16</span></span> |
| <span data-ttu-id="d8e8a-4060">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4060">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4062">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4062">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4064">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4064">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4066">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4067">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4068">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4070">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4072">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4074">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4076">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4076">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4078">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4079">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4080">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4081">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4082">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4083">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4083">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4085">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4086">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4086">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4088">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4089">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4090">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4091">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4092">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4093">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4094">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4095">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4096">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4097">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4098">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4099">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4100">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4101">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4102">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4102">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4104">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4104">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4106">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4106">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4108">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4108">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4110">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4111">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4111">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4113">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4114">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4114">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4116">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4117">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4118">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4119">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4119">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4121">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="d8e8a-4122">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_R8 (60)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="d8e8a-4123">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4123">Target</span></span> | <span data-ttu-id="d8e8a-4124">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4125">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4126">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4126">8</span></span> |
| <span data-ttu-id="d8e8a-4127">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4127">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4129">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4129">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4130">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4131">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4132">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4133">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4135">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4137">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4139">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4141">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-4142">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4143">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4144">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4145">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4146">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4147">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4147">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4149">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4150">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4151">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4152">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4153">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4154">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4155">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4156">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4157">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4158">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4159">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4160">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4161">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4162">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4163">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4164">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4165">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4165">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4167">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4168">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4169">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4170">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4171">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4172">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4173">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4173">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4175">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4176">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4177">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4178">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4178">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4180">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="d8e8a-4181">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="d8e8a-4182">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4182">Target</span></span> | <span data-ttu-id="d8e8a-4183">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4184">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4185">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4185">8</span></span> |
| <span data-ttu-id="d8e8a-4186">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4186">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4188">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4188">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4190">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4190">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4192">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4193">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4194">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4196">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4198">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4200">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4202">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4202">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4204">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4204">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4206">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4207">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4208">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4209">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4210">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4212">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4212">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4214">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4214">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4216">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4216">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4218">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4219">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4220">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4221">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4222">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4223">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4224">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4225">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4226">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4227">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4228">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4229">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4230">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4231">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4231">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4233">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4233">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4235">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4235">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4237">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4237">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4239">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4239">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4241">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4241">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4243">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4244">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4244">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4246">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4247">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4248">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4249">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4249">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4251">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="d8e8a-4252">DXGI_FORMAT_R8ое \_ <sup>FCS</sup> /uint (62)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="d8e8a-4253">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4253">Target</span></span> | <span data-ttu-id="d8e8a-4254">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4255">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4256">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4256">8</span></span> |
| <span data-ttu-id="d8e8a-4257">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4257">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4259">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4259">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4261">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4261">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4263">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4264">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4265">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4267">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4269">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4271">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4273">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4273">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4275">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4276">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4277">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4278">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4279">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4280">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4280">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4282">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4283">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4283">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4285">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4286">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4286">Output Merger Logic Op</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4288">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4289">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4290">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4291">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4292">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4293">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4294">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4295">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4296">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4297">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4298">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4299">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4300">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4300">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4302">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4302">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4304">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4304">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4306">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4306">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4308">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4309">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4309">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4311">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4312">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4312">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4314">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4315">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4316">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4317">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4317">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4319">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="d8e8a-4320">DXGI_FORMAT_R8 \_ Снорм<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="d8e8a-4321">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4321">Target</span></span> | <span data-ttu-id="d8e8a-4322">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4323">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4324">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4324">8</span></span> |
| <span data-ttu-id="d8e8a-4325">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4325">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4327">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4327">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4329">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4329">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4331">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4332">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4333">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4335">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4337">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4339">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4341">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4341">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4343">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4343">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4345">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4346">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4347">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4348">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4349">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4351">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4351">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4353">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4353">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4355">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4356">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4357">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4358">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4359">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4360">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4361">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4362">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4363">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4364">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4365">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4366">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4367">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4368">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4369">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4369">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4371">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4371">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4373">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4373">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4375">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4375">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4377">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4377">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4379">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4379">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4381">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4382">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4382">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4384">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4385">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4386">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4387">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4387">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4389">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="d8e8a-4390">DXGI_FORMAT_R8 \_ Синт-<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="d8e8a-4391">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4391">Target</span></span> | <span data-ttu-id="d8e8a-4392">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4393">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4394">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4394">8</span></span> |
| <span data-ttu-id="d8e8a-4395">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4395">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4397">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4397">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4399">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4399">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4401">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4402">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4403">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4405">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4407">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4409">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4411">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4411">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4413">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4414">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4415">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4416">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4417">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4418">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4420">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4421">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4421">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4423">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4424">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4425">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4426">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4427">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4428">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4429">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4430">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4431">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4432">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4433">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4434">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4435">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4436">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4437">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4437">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4439">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4439">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4441">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4441">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4443">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4443">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4445">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4446">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4446">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4448">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4449">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4449">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4451">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4452">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4453">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4454">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4454">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4456">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="d8e8a-4457">DXGI_FORMAT_A8 \_ UNORM<sup>фнс</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="d8e8a-4458">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4458">Target</span></span> | <span data-ttu-id="d8e8a-4459">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4460">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4461">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4461">8</span></span> |
| <span data-ttu-id="d8e8a-4462">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4462">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4464">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4464">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4465">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4466">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4467">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4468">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4470">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4472">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4474">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4476">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4476">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4478">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4478">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4480">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4481">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4482">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4483">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4484">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4484">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4486">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4486">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4488">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4488">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4490">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4490">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4492">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4493">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4494">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4495">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4496">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4497">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4498">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4499">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4500">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4501">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4502">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4503">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4504">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4505">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4505">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4507">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4507">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4509">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4509">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4511">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4511">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4513">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4513">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4515">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4515">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-4517">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4518">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-4519">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4520">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4521">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4522">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4522">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4524">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="d8e8a-4525">DXGI_FORMAT_R9G9B9E5 \_ Шаредексп<sup>фнк</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="d8e8a-4526">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4526">Target</span></span> | <span data-ttu-id="d8e8a-4527">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4528">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4529">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4529">32</span></span> |
| <span data-ttu-id="d8e8a-4530">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4530">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4532">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4532">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4533">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4534">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4535">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4536">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4538">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4540">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4542">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4544">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4544">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4546">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4546">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4548">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4549">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4550">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4551">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4552">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4552">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4554">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4555">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4556">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4557">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4558">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4559">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4560">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4561">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4562">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4563">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4564">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4565">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4566">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4567">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4568">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4569">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4570">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4570">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4572">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4573">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4574">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4575">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4576">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4577">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4578">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-4579">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4580">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4581">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4582">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-4583">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="d8e8a-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>ФНК</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="d8e8a-4585">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4585">Target</span></span> | <span data-ttu-id="d8e8a-4586">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4587">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4588">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4588">16</span></span> |
| <span data-ttu-id="d8e8a-4589">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4589">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4591">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4591">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4592">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4593">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4594">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4595">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4597">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4599">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4601">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4603">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4603">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4605">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4605">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4607">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4608">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4609">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4610">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4611">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4611">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4613">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4614">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4615">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4616">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4617">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4618">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4619">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4620">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4621">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4622">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4623">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4624">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4625">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4626">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4627">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4628">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4629">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4629">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4631">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4632">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4633">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4634">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4635">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4636">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4637">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-4638">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4639">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4640">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4641">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-4642">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="d8e8a-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>ФНК</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="d8e8a-4644">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4644">Target</span></span> | <span data-ttu-id="d8e8a-4645">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4646">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4647">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4647">16</span></span> |
| <span data-ttu-id="d8e8a-4648">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4648">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4650">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4650">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4651">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4652">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4653">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4654">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4656">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4658">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4660">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4662">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4662">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4664">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4664">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4666">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4667">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4668">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4669">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4670">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4670">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4672">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4673">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4674">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4675">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4676">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4677">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4678">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4679">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4680">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4681">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4682">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4683">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4684">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4685">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4686">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4687">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4688">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4688">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4690">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4691">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4692">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4693">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4694">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4695">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4696">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-4697">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4698">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4699">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4700">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-4701">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="d8e8a-4702">DXGI_FORMAT_BC1 \_ нетипизированных<sup>пкк</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="d8e8a-4703">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4703">Target</span></span> | <span data-ttu-id="d8e8a-4704">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4705">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4706">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4706">4</span></span> |
| <span data-ttu-id="d8e8a-4707">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4707">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4709">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4709">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4710">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4711">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4712">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4714">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4716">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4718">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4720">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-4721">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4722">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4723">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4724">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4725">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4726">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4726">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4728">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4729">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4730">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4731">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4732">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4733">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4734">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4735">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4736">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4737">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4738">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4739">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4740">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4741">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4742">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4743">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4744">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4744">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4746">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4747">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4748">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4749">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4750">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4751">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4752">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4752">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4754">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4755">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4756">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4757">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4757">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4759">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="d8e8a-4760">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="d8e8a-4761">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4761">Target</span></span> | <span data-ttu-id="d8e8a-4762">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4763">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4764">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4764">4</span></span> |
| <span data-ttu-id="d8e8a-4765">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4765">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4767">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4767">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4768">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4769">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4770">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4772">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4774">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4776">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4778">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4778">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4780">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4780">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4782">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4783">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4784">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4785">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4786">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4786">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4788">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4789">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4790">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4791">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4792">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4793">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4794">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4795">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4796">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4797">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4798">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4799">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4800">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4801">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4802">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4803">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4804">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4804">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4806">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4807">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4808">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4809">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4810">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4811">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4812">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4812">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4814">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4815">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4816">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4817">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4817">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4819">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="d8e8a-4820">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="d8e8a-4821">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4821">Target</span></span> | <span data-ttu-id="d8e8a-4822">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4823">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4824">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4824">4</span></span> |
| <span data-ttu-id="d8e8a-4825">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4825">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4827">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4827">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4828">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4829">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4830">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4832">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4834">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4836">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4838">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4838">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4840">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4840">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4842">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4843">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4844">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4845">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4846">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4846">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4848">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4849">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4850">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4851">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4852">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4853">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4854">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4855">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4856">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4857">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4858">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4859">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4860">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4861">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4862">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4863">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4864">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4864">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4866">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4867">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4868">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4869">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4870">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4871">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4872">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4872">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4874">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4875">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4876">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4877">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4877">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4879">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="d8e8a-4880">DXGI_FORMAT_BC2 \_ нетипизированных<sup>пкк</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="d8e8a-4881">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4881">Target</span></span> | <span data-ttu-id="d8e8a-4882">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4883">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4884">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4884">8</span></span> |
| <span data-ttu-id="d8e8a-4885">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4885">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4887">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4887">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4888">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4889">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4890">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4892">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4894">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4896">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4898">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-4899">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4900">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4901">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4902">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4903">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4904">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4904">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4906">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4907">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4908">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4909">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4910">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4911">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4912">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4913">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4914">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4915">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4916">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4917">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4918">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4919">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4920">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4921">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4922">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4922">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4924">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4925">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4926">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4927">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4928">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4929">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4930">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4930">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4932">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4933">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4934">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4935">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4935">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4937">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="d8e8a-4938">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="d8e8a-4939">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4939">Target</span></span> | <span data-ttu-id="d8e8a-4940">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-4941">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-4942">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4942">8</span></span> |
| <span data-ttu-id="d8e8a-4943">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4943">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4945">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4945">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4946">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4947">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4948">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4950">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4952">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4954">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4956">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4956">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4958">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4958">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4960">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4961">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-4962">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-4963">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-4964">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4964">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4966">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-4967">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4968">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4969">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-4970">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-4971">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4972">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-4973">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-4974">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-4975">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4976">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-4977">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-4978">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-4979">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-4980">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4981">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-4982">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4982">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4984">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4985">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-4986">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-4987">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-4988">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-4989">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-4990">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4990">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4992">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-4993">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-4994">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-4995">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4995">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-4997">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="d8e8a-4998">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="d8e8a-4999">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-4999">Target</span></span> | <span data-ttu-id="d8e8a-5000">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5001">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5002">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5002">8</span></span> |
| <span data-ttu-id="d8e8a-5003">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5003">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5005">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5005">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5006">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5007">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5008">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5010">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5012">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5014">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5016">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5016">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5018">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5018">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5020">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5021">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5022">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5023">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5024">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5024">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5026">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5027">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5028">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5029">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5030">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5031">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5032">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5033">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5034">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5035">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5036">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5037">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5038">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5039">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5040">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5041">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5042">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5042">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5044">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5045">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5046">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5047">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5048">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5049">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5050">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5050">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5052">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5053">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5054">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5055">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5055">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5057">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="d8e8a-5058">DXGI_FORMAT_BC3 \_ нетипизированных<sup>пкк</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="d8e8a-5059">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5059">Target</span></span> | <span data-ttu-id="d8e8a-5060">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5061">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5062">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5062">8</span></span> |
| <span data-ttu-id="d8e8a-5063">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5063">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5065">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5065">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5066">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5067">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5068">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5070">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5072">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5074">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5076">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-5077">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5078">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5079">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5080">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5081">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5082">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5082">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5084">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5085">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5086">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5087">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5088">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5089">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5090">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5091">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5092">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5093">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5094">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5095">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5096">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5097">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5098">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5099">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5100">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5100">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5102">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5103">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5104">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5105">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5106">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5107">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5108">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5108">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5110">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5111">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5112">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5113">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5113">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5115">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="d8e8a-5116">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="d8e8a-5117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5117">Target</span></span> | <span data-ttu-id="d8e8a-5118">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5119">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5120">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5120">8</span></span> |
| <span data-ttu-id="d8e8a-5121">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5121">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5123">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5123">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5124">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5125">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5126">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5128">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5130">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5132">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5134">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5134">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5136">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5136">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5138">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5139">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5140">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5141">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5142">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5142">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5144">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5145">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5146">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5147">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5148">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5149">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5150">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5151">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5152">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5153">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5154">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5155">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5156">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5157">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5158">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5159">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5160">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5160">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5162">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5163">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5164">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5165">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5166">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5167">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5168">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5168">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5170">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5171">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5172">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5173">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5173">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5175">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="d8e8a-5176">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="d8e8a-5177">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5177">Target</span></span> | <span data-ttu-id="d8e8a-5178">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5179">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5180">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5180">8</span></span> |
| <span data-ttu-id="d8e8a-5181">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5181">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5183">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5183">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5184">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5185">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5186">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5188">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5190">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5192">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5194">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5194">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5196">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5196">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5198">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5199">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5200">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5201">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5202">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5204">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5205">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5206">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5207">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5208">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5209">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5210">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5211">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5212">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5213">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5214">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5215">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5216">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5217">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5218">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5219">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5220">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5220">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5222">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5223">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5224">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5225">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5226">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5227">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5228">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5228">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5230">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5231">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5232">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5233">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5233">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5235">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="d8e8a-5236">DXGI_FORMAT_BC4 \_ нетипизированных<sup>пкк</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="d8e8a-5237">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5237">Target</span></span> | <span data-ttu-id="d8e8a-5238">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5239">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5240">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5240">4</span></span> |
| <span data-ttu-id="d8e8a-5241">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5241">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5243">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5243">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5244">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5245">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5246">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5248">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5250">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5252">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5254">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-5255">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5256">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5257">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5258">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5259">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5260">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5260">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5262">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5263">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5264">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5265">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5266">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5267">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5268">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5269">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5270">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5271">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5272">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5273">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5274">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5275">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5276">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5277">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5278">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5278">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5280">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5281">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5282">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5283">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5284">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5285">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5286">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5286">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5288">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5289">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5290">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5291">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5292">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="d8e8a-5293">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="d8e8a-5294">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5294">Target</span></span> | <span data-ttu-id="d8e8a-5295">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5296">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5297">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5297">4</span></span> |
| <span data-ttu-id="d8e8a-5298">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5298">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5300">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5300">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5301">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5302">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5303">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5305">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5307">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5309">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5311">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5311">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5313">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5313">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5315">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5316">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5317">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5318">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5319">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5321">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5322">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5323">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5324">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5325">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5326">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5327">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5328">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5329">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5330">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5331">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5332">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5333">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5334">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5335">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5336">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5337">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5337">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5339">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5340">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5341">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5342">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5343">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5344">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5345">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5345">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5347">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5348">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5349">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5350">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5351">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="d8e8a-5352">DXGI_FORMAT_BC4 \_ Снорм<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="d8e8a-5353">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5353">Target</span></span> | <span data-ttu-id="d8e8a-5354">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5355">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5356">4</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5356">4</span></span> |
| <span data-ttu-id="d8e8a-5357">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5357">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5359">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5359">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5360">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5361">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5362">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5364">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5366">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5368">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5370">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5370">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5372">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5372">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5374">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5375">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5376">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5377">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5378">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5380">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5381">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5382">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5383">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5384">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5385">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5386">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5387">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5388">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5389">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5390">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5391">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5392">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5393">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5394">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5395">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5396">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5396">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5398">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5399">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5400">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5401">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5402">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5403">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5404">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5404">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5406">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5407">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5408">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5409">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5410">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="d8e8a-5411">DXGI_FORMAT_BC5 \_ нетипизированных<sup>пкк</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="d8e8a-5412">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5412">Target</span></span> | <span data-ttu-id="d8e8a-5413">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5414">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5415">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5415">8</span></span> |
| <span data-ttu-id="d8e8a-5416">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5416">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5418">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5418">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5419">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5420">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5421">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5423">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5425">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5427">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5429">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-5430">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5431">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5432">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5433">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5434">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5435">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5435">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5437">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5438">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5439">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5440">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5441">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5442">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5443">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5444">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5445">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5446">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5447">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5448">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5449">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5450">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5451">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5452">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5453">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5453">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5455">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5456">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5457">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5458">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5459">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5460">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5461">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5461">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5463">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5464">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5465">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5466">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5467">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="d8e8a-5468">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="d8e8a-5469">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5469">Target</span></span> | <span data-ttu-id="d8e8a-5470">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5471">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5472">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5472">8</span></span> |
| <span data-ttu-id="d8e8a-5473">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5473">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5475">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5475">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5476">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5477">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5478">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5480">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5482">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5484">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5486">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5486">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5488">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5488">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5490">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5491">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5492">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5493">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5494">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5494">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5496">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5497">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5498">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5499">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5500">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5501">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5502">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5503">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5504">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5505">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5506">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5507">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5508">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5509">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5510">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5511">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5512">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5512">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5514">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5515">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5516">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5517">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5518">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5519">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5520">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5520">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5522">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5523">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5524">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5525">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5526">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="d8e8a-5527">DXGI_FORMAT_BC5 \_ Снорм<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="d8e8a-5528">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5528">Target</span></span> | <span data-ttu-id="d8e8a-5529">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5530">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5531">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5531">8</span></span> |
| <span data-ttu-id="d8e8a-5532">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5532">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5534">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5534">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5535">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5536">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5537">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5539">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5541">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5543">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5545">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5545">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5547">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5547">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5549">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5550">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5551">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5552">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5553">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5555">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5556">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5557">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5558">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5559">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5560">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5561">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5562">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5563">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5564">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5565">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5566">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5567">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5568">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5569">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5570">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5571">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5571">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5573">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5574">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5575">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5576">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5577">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5578">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5579">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5579">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5581">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5582">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5583">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5584">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5585">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="d8e8a-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>фнс</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="d8e8a-5587">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5587">Target</span></span> | <span data-ttu-id="d8e8a-5588">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5589">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5590">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5590">16</span></span> |
| <span data-ttu-id="d8e8a-5591">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5591">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5593">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5593">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5595">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5595">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5597">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5598">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5599">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5601">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5603">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5605">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5607">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5607">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5609">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5609">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5611">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5612">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5613">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5614">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5615">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5617">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5617">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5619">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5619">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5621">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5621">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5623">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5624">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5625">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5626">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5627">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5628">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5629">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5630">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5631">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5632">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5633">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5634">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5635">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5636">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5636">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5638">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5638">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5640">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5640">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5642">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5642">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5644">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5644">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5646">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5646">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5648">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5649">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-5650">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5651">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5652">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5653">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5654">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="d8e8a-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>фнс</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="d8e8a-5656">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5656">Target</span></span> | <span data-ttu-id="d8e8a-5657">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5658">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5659">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5659">16</span></span> |
| <span data-ttu-id="d8e8a-5660">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5660">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5662">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5662">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5664">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5664">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5666">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5667">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5668">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5670">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5672">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5674">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5676">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5676">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5678">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5678">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5680">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5681">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5682">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5683">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5684">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5686">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5686">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5688">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5688">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5690">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5690">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5692">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5693">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5694">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5695">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5696">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5697">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5698">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5699">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5700">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5701">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5702">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5703">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5704">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5705">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5705">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5707">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5707">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5709">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5709">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5711">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5711">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5713">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5713">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5715">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5715">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5717">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5718">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-5719">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5720">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5721">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5722">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-5723">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="d8e8a-5724">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8A8 (90)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="d8e8a-5725">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5725">Target</span></span> | <span data-ttu-id="d8e8a-5726">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5727">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5728">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5728">32</span></span> |
| <span data-ttu-id="d8e8a-5729">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5729">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5731">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5731">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5732">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5733">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5734">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5735">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5737">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5739">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5741">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5743">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-5744">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5745">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5746">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5747">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5748">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5749">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5749">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5751">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5752">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5753">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5754">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5755">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5756">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5757">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5758">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5759">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5760">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5761">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5762">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5763">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5764">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5765">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5766">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5767">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5767">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5769">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5770">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5771">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5772">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5773">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5774">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5775">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5775">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5777">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5778">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5779">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5780">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5780">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5782">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="d8e8a-5783">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="d8e8a-5784">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5784">Target</span></span> | <span data-ttu-id="d8e8a-5785">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5786">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5787">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5787">32</span></span> |
| <span data-ttu-id="d8e8a-5788">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5788">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5790">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5790">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5792">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5792">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5794">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5795">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5796">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5798">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5800">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5802">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5804">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5804">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5806">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5806">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5808">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5809">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5810">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5811">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5812">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5812">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5814">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5814">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5816">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5816">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5818">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5818">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5820">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5821">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5822">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5823">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5824">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5825">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5826">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5827">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5828">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5829">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5830">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5831">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5832">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5833">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5833">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5835">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5835">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5837">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5837">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5839">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5839">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5841">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5841">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5843">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5843">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5845">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5845">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5847">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5847">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5849">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5850">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5850">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5852">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5852">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5854">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5854">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5856">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="d8e8a-5857">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="d8e8a-5858">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5858">Target</span></span> | <span data-ttu-id="d8e8a-5859">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5860">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5861">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5861">32</span></span> |
| <span data-ttu-id="d8e8a-5862">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5862">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5864">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5864">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5865">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5866">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5867">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5868">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5870">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5872">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5874">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5876">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5876">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5878">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5878">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5880">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5881">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5882">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5883">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5884">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5884">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5886">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5886">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5888">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5888">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5890">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5890">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5892">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5893">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5894">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5895">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5896">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5897">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5898">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5899">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5900">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5901">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5902">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5903">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5904">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5905">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5905">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5907">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5907">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5909">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5909">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5911">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5911">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5913">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5913">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5915">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5915">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5917">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5917">Display Scan-Out</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5919">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5919">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5921">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5922">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5922">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5924">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5924">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-5926">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5926">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5928">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="d8e8a-5929">\_Нетипизированные<sup>Компьютеры</sup> DXGI_FORMAT_B8G8R8X8 (92)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="d8e8a-5930">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5930">Target</span></span> | <span data-ttu-id="d8e8a-5931">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5932">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5933">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5933">32</span></span> |
| <span data-ttu-id="d8e8a-5934">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5934">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5936">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5936">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5937">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5938">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5939">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5940">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5942">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5944">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5946">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5948">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-5949">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5950">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5951">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-5952">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-5953">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-5954">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5954">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5956">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-5957">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5958">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5959">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-5960">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-5961">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5962">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-5963">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-5964">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-5965">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5966">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-5967">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-5968">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-5969">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-5970">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5971">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-5972">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5972">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5974">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5975">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-5976">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-5977">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-5978">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-5979">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-5980">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5980">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5982">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-5983">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-5984">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-5985">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5985">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5987">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="d8e8a-5988">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="d8e8a-5989">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5989">Target</span></span> | <span data-ttu-id="d8e8a-5990">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-5991">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-5992">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5992">32</span></span> |
| <span data-ttu-id="d8e8a-5993">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5993">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5995">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5995">Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5997">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5997">Input Assembler Vertex Buffer</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-5999">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6000">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6001">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6003">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6005">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6007">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6009">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6009">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6011">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6011">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6013">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6014">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6015">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6016">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6017">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6017">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6019">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6019">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6021">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6021">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6023">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6023">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6025">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6026">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6027">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6028">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6029">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6030">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6031">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6032">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6033">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6034">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6035">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6036">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6037">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6038">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6038">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6040">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6040">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6042">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6042">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6044">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6044">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6046">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6046">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6048">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6048">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6050">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6051">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6051">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6053">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-6054">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6054">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6056">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6056">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6058">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6058">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6060">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="d8e8a-6061">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="d8e8a-6062">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6062">Target</span></span> | <span data-ttu-id="d8e8a-6063">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6064">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6065">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6065">32</span></span> |
| <span data-ttu-id="d8e8a-6066">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6066">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6068">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6068">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6069">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6070">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6071">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6072">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6074">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6076">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6078">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6080">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6080">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6082">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6082">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6084">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6085">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6086">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6087">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6088">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6088">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6090">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6090">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6092">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6092">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6094">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6094">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6096">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6097">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6098">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6099">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6100">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6101">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6102">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6103">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6104">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6105">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6106">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6107">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6108">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6109">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6109">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6111">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6111">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6113">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6113">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6115">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6115">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6117">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6117">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6119">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6119">Multisample Load</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6121">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6122">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6122">Cast Within Bit Layout</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6124">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-6125">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-6126">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-6127">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6127">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6129">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="d8e8a-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="d8e8a-6131">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6131">Target</span></span> | <span data-ttu-id="d8e8a-6132">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6133">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6134">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6134">32</span></span> |
| <span data-ttu-id="d8e8a-6135">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6135">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6137">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6137">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6138">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6139">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6140">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6142">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6146">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6146">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6148">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6148">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6150">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6151">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6152">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6153">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6154">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6154">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6156">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6156">Mipmap Auto-Generation</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6158">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6158">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6160">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6160">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6162">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6163">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6164">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6165">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6166">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6167">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6168">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6169">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6170">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6171">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6172">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6173">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6174">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6175">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6175">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6177">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6178">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6179">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6180">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6181">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6182">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6183">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6184">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6184">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6186">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6186">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6188">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6188">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6190">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6190">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6192">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="d8e8a-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="d8e8a-6194">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6194">Target</span></span> | <span data-ttu-id="d8e8a-6195">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6196">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6197">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6197">32</span></span> |
| <span data-ttu-id="d8e8a-6198">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6198">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6200">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6200">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6201">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6202">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6203">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6205">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6209">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6209">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6211">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6211">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6213">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6214">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6215">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6216">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6217">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6218">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6219">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6220">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6221">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6222">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6223">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6224">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6225">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6226">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6227">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6228">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6229">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6230">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6231">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6232">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6233">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6234">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6234">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6236">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6237">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6238">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6239">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6240">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6241">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6242">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6243">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6243">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6245">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6245">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6247">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6247">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6249">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6249">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6251">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="d8e8a-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="d8e8a-6253">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6253">Target</span></span> | <span data-ttu-id="d8e8a-6254">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6255">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6256">64</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6256">64</span></span> |
| <span data-ttu-id="d8e8a-6257">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6257">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6259">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6259">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6260">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6261">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6262">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6264">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6268">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6268">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6270">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6270">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6272">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6273">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6274">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6275">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6276">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6276">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6278">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6279">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6280">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6281">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6282">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6283">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6284">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6285">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6286">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6287">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6288">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6289">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6290">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6291">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6292">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6293">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6294">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6294">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6296">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6297">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6298">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6299">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6300">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6301">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6302">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6303">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6303">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6305">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6305">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6307">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6307">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6309">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6309">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6311">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="d8e8a-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="d8e8a-6313">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6313">Target</span></span> | <span data-ttu-id="d8e8a-6314">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6315">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6316">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6316">8</span></span> |
| <span data-ttu-id="d8e8a-6317">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6317">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6319">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6319">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6320">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6321">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6322">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6324">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6328">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6328">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6330">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6330">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6332">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6333">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6334">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6335">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6336">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6337">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6338">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6338">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6340">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6340">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6342">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6343">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6344">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6345">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6346">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6347">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6348">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6349">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6350">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6351">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6352">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6353">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6354">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6355">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6355">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6357">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6358">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6359">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6360">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6361">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6362">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6363">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6364">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6364">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6366">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6366">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6368">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6368">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6370">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6370">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6372">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="d8e8a-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="d8e8a-6374">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6374">Target</span></span> | <span data-ttu-id="d8e8a-6375">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6376">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6377">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6377">16</span></span> |
| <span data-ttu-id="d8e8a-6378">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6378">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6380">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6380">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6381">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6382">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6383">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6385">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6389">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6389">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6391">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6391">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6393">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6394">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6395">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6396">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6397">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6398">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6399">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6399">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6401">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6401">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6403">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6404">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6405">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6406">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6407">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6408">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6409">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6410">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6411">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6412">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6413">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6414">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6415">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6416">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6416">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6418">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6419">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6420">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6421">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6422">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6423">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6424">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6425">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6425">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6427">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6427">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6429">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6429">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6431">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6431">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6433">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="d8e8a-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="d8e8a-6435">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6435">Target</span></span> | <span data-ttu-id="d8e8a-6436">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6437">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6438">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6438">16</span></span> |
| <span data-ttu-id="d8e8a-6439">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6439">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6441">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6441">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6442">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6443">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6444">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6446">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6450">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6450">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6452">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6452">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6454">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6455">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6456">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6457">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6458">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6459">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6460">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6460">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6462">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6462">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6464">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6465">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6466">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6467">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6468">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6469">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6470">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6471">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6472">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6473">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6474">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6475">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6476">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6477">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6477">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6479">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6480">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6481">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6482">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6483">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6484">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6485">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6486">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6486">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6488">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6488">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6490">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6490">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6492">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6492">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6494">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="d8e8a-6495">DXGI_FORMAT_420 \_ непрозрачный<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="d8e8a-6496">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6496">Target</span></span> | <span data-ttu-id="d8e8a-6497">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6498">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6499">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6499">8</span></span> |
| <span data-ttu-id="d8e8a-6500">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6500">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6502">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6502">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6503">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6504">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6505">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6507">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6511">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-6512">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6513">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6514">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6515">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6516">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6517">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6518">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6519">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6520">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6521">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6522">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6523">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6524">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6525">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6526">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6527">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6528">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6529">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6530">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6531">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6532">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6533">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6534">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="d8e8a-6535">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6536">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6537">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6538">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6539">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6540">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6541">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6542">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6542">Video Decoder Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6544">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6544">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6546">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6546">Video Processor Output</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6548">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6548">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6550">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="d8e8a-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="d8e8a-6552">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6552">Target</span></span> | <span data-ttu-id="d8e8a-6553">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6554">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6555">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6555">16</span></span> |
| <span data-ttu-id="d8e8a-6556">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6556">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6558">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6558">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6559">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6560">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6561">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6563">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6567">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6567">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6569">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6569">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6571">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6572">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6573">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6574">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6575">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6576">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6577">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6578">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6579">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6580">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6581">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6582">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6583">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6584">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6585">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6586">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6587">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6588">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6589">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6590">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6591">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6592">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6592">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6594">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6595">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6596">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6597">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6598">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6599">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6600">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6601">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6601">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6603">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6603">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6605">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6605">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6607">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6607">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6609">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="d8e8a-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="d8e8a-6611">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6611">Target</span></span> | <span data-ttu-id="d8e8a-6612">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6613">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6614">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6614">32</span></span> |
| <span data-ttu-id="d8e8a-6615">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6615">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6617">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6617">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6618">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6619">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6620">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6622">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6626">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6626">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6628">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6628">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6630">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6631">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6632">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6633">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6634">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6635">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6636">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6637">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6638">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6639">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6640">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6641">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6642">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6643">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6644">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6645">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6646">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6647">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6648">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6649">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6650">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6651">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6651">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6653">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6654">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6655">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6656">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6657">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6658">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6659">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6660">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6660">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6662">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6662">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6664">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6664">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6666">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6666">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6668">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="d8e8a-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="d8e8a-6670">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6670">Target</span></span> | <span data-ttu-id="d8e8a-6671">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6672">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6673">32</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6673">32</span></span> |
| <span data-ttu-id="d8e8a-6674">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6674">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6676">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6676">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6677">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6678">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6679">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6681">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6685">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6685">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6687">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6687">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6689">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6690">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6691">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6692">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6694">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6695">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6696">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6697">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6698">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6699">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6700">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6701">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6702">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6703">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6704">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6705">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6706">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6707">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6708">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6709">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6710">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6710">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6712">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6713">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6714">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6715">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6716">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6717">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6718">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6719">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6719">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6721">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6721">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6723">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6723">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6725">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6725">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6727">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="d8e8a-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="d8e8a-6729">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6729">Target</span></span> | <span data-ttu-id="d8e8a-6730">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6731">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6732">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6732">8</span></span> |
| <span data-ttu-id="d8e8a-6733">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6733">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6735">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6735">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6736">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6737">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6738">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6740">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6744">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6744">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6746">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6746">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6748">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6749">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6750">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6751">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6753">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6754">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6754">RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6756">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6756">Blendable RenderTarget</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6758">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6759">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6760">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6761">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6762">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6763">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6764">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6765">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6766">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6767">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6768">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6769">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6770">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6771">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6771">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6773">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6774">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6775">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6776">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6777">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6778">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6779">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6780">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6780">Video Decoder Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6782">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6782">Video Processor Input</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6784">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6784">Video Processor Output</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6786">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6786">Shared Resource</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6788">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="d8e8a-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="d8e8a-6790">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6790">Target</span></span> | <span data-ttu-id="d8e8a-6791">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6792">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6793">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6793">8</span></span> |
| <span data-ttu-id="d8e8a-6794">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6794">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6796">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6796">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6797">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6798">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6799">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6801">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6805">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-6806">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6807">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6808">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6809">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6810">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6811">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6812">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6813">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6814">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6815">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6816">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6817">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6818">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6819">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6820">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6821">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6822">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6823">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6824">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6825">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6826">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6827">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6828">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6828">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6830">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6831">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6832">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6833">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6834">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6835">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6836">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6837">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-6838">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6838">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6840">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-6841">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-6842">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="d8e8a-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="d8e8a-6844">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6844">Target</span></span> | <span data-ttu-id="d8e8a-6845">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6846">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6847">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6847">8</span></span> |
| <span data-ttu-id="d8e8a-6848">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6848">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6850">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6850">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6851">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6852">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6853">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6855">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6859">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-6860">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6861">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6862">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6863">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6864">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6865">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6866">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6867">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6868">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6869">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6870">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6871">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6872">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6873">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6874">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6875">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6876">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6877">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6878">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6879">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6880">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6881">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6882">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6882">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6884">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6885">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6886">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6887">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6888">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6889">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6890">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6891">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-6892">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6892">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6894">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-6895">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-6896">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="d8e8a-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="d8e8a-6898">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6898">Target</span></span> | <span data-ttu-id="d8e8a-6899">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6900">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6901">8</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6901">8</span></span> |
| <span data-ttu-id="d8e8a-6902">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6902">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6904">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6904">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6905">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6906">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6907">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6909">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6913">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-6914">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6915">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6916">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6917">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6918">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6919">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6920">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6921">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6922">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6923">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6924">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6925">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6926">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6927">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6928">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6929">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6930">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6931">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6932">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6933">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6934">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6935">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6936">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6936">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6938">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6939">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6940">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6941">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6942">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6943">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6944">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6945">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-6946">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6946">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6948">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-6949">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-6950">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="d8e8a-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="d8e8a-6952">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6952">Target</span></span> | <span data-ttu-id="d8e8a-6953">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-6954">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-6955">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6955">16</span></span> |
| <span data-ttu-id="d8e8a-6956">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6956">Format Support</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-6958">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6958">Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6959">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6960">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6961">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="d8e8a-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6963">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="d8e8a-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="d8e8a-6967">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="d8e8a-6968">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6969">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6970">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-6971">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-6972">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-6973">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="d8e8a-6974">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="d8e8a-6975">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6976">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6977">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-6978">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-6979">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6980">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-6981">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-6982">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-6983">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6984">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-6985">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-6986">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-6987">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-6988">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6989">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-6990">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6990">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-6992">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6993">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="d8e8a-6994">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="d8e8a-6995">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="d8e8a-6996">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="d8e8a-6997">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-6998">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-6999">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-7000">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7000">Video Processor Input</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7002">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-7003">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-7004">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="d8e8a-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>фнс</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="d8e8a-7006">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7006">Target</span></span> | <span data-ttu-id="d8e8a-7007">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="d8e8a-7008">Бит на элемент (BPE)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="d8e8a-7009">16</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7009">16</span></span> |
| <span data-ttu-id="d8e8a-7010">Поддержка формата</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7010">Format Support</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7012">Буфер</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7012">Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7014">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7014">Input Assembler Vertex Buffer</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7016">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-7017">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="d8e8a-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7018">Texture1D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7020">Texture2D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7022">Texture3D</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7024">TextureCube</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7026">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7026">Shader ld</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7028">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7028">Shader sample (any filter)</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7030">Образец шейдера \_ c (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-7031">Образец шейдера (1-разрядный фильтр Mono)</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="d8e8a-7032">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="d8e8a-7033">Шейдер gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="d8e8a-7034">Mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7034">Mipmap</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7036">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7036">Mipmap Auto-Generation</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7038">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7038">RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7040">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7040">Blendable RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7042">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="d8e8a-7043">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="d8e8a-7044">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-7045">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="d8e8a-7046">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="d8e8a-7047">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="d8e8a-7048">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="d8e8a-7049">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="d8e8a-7050">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="d8e8a-7051">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="d8e8a-7052">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="d8e8a-7053">UAV Atomic со знаком min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-7054">UAV Atomic неподписанные min или Max</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="d8e8a-7055">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7055">CPU Lockable</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7057">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7057">4x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7059">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7059">8x Multisample RenderTarget</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7061">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7061">Other Multisample Count RT</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7063">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7063">Multisample Resolve</span></span> | ![обязательно](images/letter-r.jpg) |
| <span data-ttu-id="d8e8a-7065">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7065">Multisample Load</span></span> | ![необязательно](images/letter-o.jpg) |
| <span data-ttu-id="d8e8a-7067">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="d8e8a-7068">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="d8e8a-7069">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="d8e8a-7070">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="d8e8a-7071">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="d8e8a-7072">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="d8e8a-7073">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="d8e8a-7074">Форматирование заметок</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7074">Format notes</span></span>

<span data-ttu-id="d8e8a-7075">Назначение формата может изменяться с одного уровня компонентов оборудования на следующий.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="d8e8a-7076"><sup>L</sup> : нетипизированный формат</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="d8e8a-7077"><sup>ПК</sup> : частично типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="d8e8a-7078"><sup>FCS</sup> : полностью типизированный, приведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="d8e8a-7079"><sup>ФНС</sup> : полностью типизированный, неприведенный и простой макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="d8e8a-7080"><sup>ПКК</sup> : частично типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="d8e8a-7081"><sup>FCC</sup> : полностью типизированный, приведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="d8e8a-7082"><sup>ФНК</sup> : полностью типизированный, неприведенный и сложный макет</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="d8e8a-7083"><sup>V</sup> : формат видео</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="d8e8a-7084">Задние буферы и сканирование с форматом [**DXGI \_ \_ R16G16B16A16 \_ float**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) содержат данные гаммы с линейным значением.</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8e8a-7085">См. также</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7085">Related topics</span></span>

[<span data-ttu-id="d8e8a-7086">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="d8e8a-7087">**ID3D10Device:: Чеккформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="d8e8a-7088">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="d8e8a-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
