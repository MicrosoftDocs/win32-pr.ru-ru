---
title: Новые возможности пакета SDK для Windows 7 августа 2009 и Direct3D 11
description: Эта версия Windows 7 или Direct3D 11 поставляется в составе пакета SDK DirectX и содержит новые функции, средства и документацию.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794820"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="362e7-103">Новые возможности пакета SDK для Windows 7 августа 2009 и Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="362e7-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="362e7-104">Эта версия Windows 7 или Direct3D 11 поставляется в составе пакета SDK DirectX и содержит новые функции, средства и документацию.</span><span class="sxs-lookup"><span data-stu-id="362e7-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="362e7-105">Элемент</span><span class="sxs-lookup"><span data-stu-id="362e7-105">Item</span></span></th>
<th><span data-ttu-id="362e7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="362e7-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="362e7-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="362e7-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="362e7-108">Direct2D — это высокопроизводительный высокоскоростной графический API, обеспечивающий высокую производительность и высококачественную отрисовку для двухмерной геометрии, точечных рисунков и текста.</span><span class="sxs-lookup"><span data-stu-id="362e7-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="362e7-109">API Direct2D поддерживает взаимодействие с Direct3D и GDI.</span><span class="sxs-lookup"><span data-stu-id="362e7-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="362e7-110">Этот пакет SDK позволяет разработчикам оценивать API и создавать простые приложения с использованием некоторых расширенных функций, доступных на правильно настроенных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="362e7-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="362e7-111"><a href="/windows/win32/direct2d/direct2d-portal">Документация</a> и <a href="/previous-versions//dd372354(v=vs.85)">примеры</a> для Direct2D в настоящее время доступны на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="362e7-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="362e7-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="362e7-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="362e7-113">DirectWrite обеспечивает поддержку высококачественной отрисовки текста, независимых от разрешения шрифтов, полную поддержку текста и макета в Юникоде, а также многое другое.</span><span class="sxs-lookup"><span data-stu-id="362e7-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="362e7-114">Независимая от устройства система макета текста, улучшающая удобочитаемость текста в документах и в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="362e7-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="362e7-115">Высококачественная, Подпиксельная визуализация текста ClearType, которая может использовать GDI Direct3D, Direct2D или технологию отрисовки для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="362e7-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="362e7-116">Поддержка многоязычного текста.</span><span class="sxs-lookup"><span data-stu-id="362e7-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="362e7-117">Поддержка расширенных типографских функций шрифтов OpenType.</span><span class="sxs-lookup"><span data-stu-id="362e7-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="362e7-118">Поддержка макета и отрисовки текста во всех языках, поддерживаемых Windows.</span><span class="sxs-lookup"><span data-stu-id="362e7-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="362e7-119">Этот пакет SDK позволяет разработчикам оценивать API и создавать базовые приложения только в демонстрационных целях.</span><span class="sxs-lookup"><span data-stu-id="362e7-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="362e7-120"><a href="/windows/win32/directwrite/direct-write-portal">Документация</a> и <a href="/windows/win32/directwrite/samples">примеры</a> для DirectWrite в настоящее время доступны на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="362e7-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="362e7-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="362e7-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="362e7-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">Dxgi 1,1</a> строится на DXGI 1,0 и будет доступно как в Windows Vista, так и в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="362e7-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="362e7-123">DXGI 1,1 добавляет несколько новых функций:</span><span class="sxs-lookup"><span data-stu-id="362e7-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="362e7-124">Поддержка синхронизированных общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="362e7-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="362e7-125">Это обеспечивает эффективное совместное использование поверхности чтения и записи для нескольких D3D (может быть между D3D10 и D3D11).</span><span class="sxs-lookup"><span data-stu-id="362e7-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="362e7-126">Поддержка формата BGRA.</span><span class="sxs-lookup"><span data-stu-id="362e7-126">BGRA format support.</span></span> <span data-ttu-id="362e7-127">Это позволяет GDI отображаться на той же поверхности DXGI, которая предназначена для устройства Direct2D, Direct3D 10,1 или Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="362e7-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="362e7-128">Максимальная задержка кадра.</span><span class="sxs-lookup"><span data-stu-id="362e7-128">Maximum Frame Latency.</span></span> <span data-ttu-id="362e7-129">С помощью <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: сетмаксимумфрамелатенци</strong></a> и <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: жетмаксимумфрамелатенци</strong></a>заголовки могут управлять числом кадров, которые могут храниться в очереди, перед отправкой для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="362e7-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="362e7-130">Задержка часто используется для управления тем, как ЦП выбирает между ответами на вводимые пользователем данные и фреймами, находящиеся в очереди отрисовки.</span><span class="sxs-lookup"><span data-stu-id="362e7-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="362e7-131">Перечисление адаптеров.</span><span class="sxs-lookup"><span data-stu-id="362e7-131">Adapter Enumeration.</span></span> <span data-ttu-id="362e7-132">С помощью <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>заголовки могут перечислять локальные адаптеры без подключенных мониторов или выходных данных, а также адаптеры с присоединенными выходами.</span><span class="sxs-lookup"><span data-stu-id="362e7-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="362e7-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Обновленные примеры</span><span class="sxs-lookup"><span data-stu-id="362e7-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="362e7-134">В этом выпуске есть несколько новых и обновленных примеров.</span><span class="sxs-lookup"><span data-stu-id="362e7-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="362e7-135">Новый <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> — это иллюстрация более сложных методов обработки шейдеров вычислений, которые можно ЗАПУСКАТЬ на D3D10 или D3D11 GPU.</span><span class="sxs-lookup"><span data-stu-id="362e7-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="362e7-136"><a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">Пример HDRToneMappingCS11</a> был расширен для реализации эффектов размытия и раскрытияа (в дополнение к сопоставлению тонов) с помощью COMPUTE Shader, а также для сравнения реализаций шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="362e7-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="362e7-137"><a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">Пример MultithreadedRendering11</a> был значительно обновлен, благодаря более сложным материалам для графических ресурсов и более интенсивной обработке потоков.</span><span class="sxs-lookup"><span data-stu-id="362e7-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="362e7-138"><a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">Образец SubD11</a> был обновлен с использованием новой модели лица, и теперь в примере используется функция вычисления соседей в средстве экспорта содержимого примеров.</span><span class="sxs-lookup"><span data-stu-id="362e7-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="362e7-139">См. также</span><span class="sxs-lookup"><span data-stu-id="362e7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="362e7-140">Функции, появившиеся в предыдущих выпусках</span><span class="sxs-lookup"><span data-stu-id="362e7-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

