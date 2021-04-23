---
description: В Microsoft Direct3D 9 были изменены следующие функции. Если вы используете эти функции, см. Приведенные ниже изменения, которые помогут перенести приложение на Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Преобразование в Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710767"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="023ef-104">Преобразование в Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="023ef-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="023ef-105">В Microsoft Direct3D 9 были изменены следующие функции.</span><span class="sxs-lookup"><span data-stu-id="023ef-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="023ef-106">Если вы используете эти функции, см. Приведенные ниже изменения, которые помогут перенести приложение на Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="023ef-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="023ef-107">Басевертексиндекс изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="023ef-108">Креатеимажесурфаце изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="023ef-109">D3DENUM \_ без \_ \_ изменений уровня WHQL</span><span class="sxs-lookup"><span data-stu-id="023ef-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="023ef-110">Создание изменений ресурсов</span><span class="sxs-lookup"><span data-stu-id="023ef-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="023ef-111">Енумадаптермодес изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="023ef-112">Изменения Get и Сетстреамсаурце \_</span><span class="sxs-lookup"><span data-stu-id="023ef-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="023ef-113">Изменение качества с множественной выборкой</span><span class="sxs-lookup"><span data-stu-id="023ef-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="023ef-114">Ресаурцеманажердискардбитес изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="023ef-115">Сетсофтваревертекспроцессинг изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="023ef-116">Изменения в образце текстур</span><span class="sxs-lookup"><span data-stu-id="023ef-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="023ef-117">Изменения в объявлении вершин</span><span class="sxs-lookup"><span data-stu-id="023ef-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="023ef-118">Интервалы \_ и \_ SwapEffects \_ изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="023ef-119">Басевертексиндекс изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="023ef-120">В DirectX 8. x IDirect3DDevice8:: Сетиндицес требуется указатель на буфер индекса и Басевертексиндекс для начальной позиции в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="023ef-121">Приложение, пакетное выполнение различных объектов в буфере вершин, пришлось переключить буфер индексов (или выполнить вызов IDirect3DDevice8:: Сетиндицес) перед вызовом IDirect3DDevice8::D Равиндекседпримитиве.</span><span class="sxs-lookup"><span data-stu-id="023ef-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="023ef-122">В Direct3D 9 начальная позицией в буфере вершин, *басевертексиндекс*, была перемещена в IDirect3DDevice9::D равиндекседпримитиве, а ее тип данных изменился с DWORD на int.</span><span class="sxs-lookup"><span data-stu-id="023ef-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="023ef-123">Креатеимажесурфаце изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="023ef-124">IDirect3DDevice8:: Креатеимажесурфаце был переименован в [**креатеоффскринплаинсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span><span class="sxs-lookup"><span data-stu-id="023ef-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="023ef-125">Добавлен дополнительный параметр, принимающий тип D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="023ef-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="023ef-126">D3DPOOL \_ будет возвращать поверхность с одинаковыми характеристиками на поверхность, созданную IDirect3DDevice8:: креатеимажесурфаце.</span><span class="sxs-lookup"><span data-stu-id="023ef-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="023ef-127">D3DPOOL \_ по умолчанию — соответствующий пул для использования с [**Стретчрект**](/windows/desktop/api) и [**колорфилл**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="023ef-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="023ef-128">D3DENUM \_ без \_ \_ изменений уровня WHQL</span><span class="sxs-lookup"><span data-stu-id="023ef-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="023ef-129">Теперь приложениям необходимо явно запрашивать лаборатории WHQL, так как ответ принимается относительно долго (несколько секунд).</span><span class="sxs-lookup"><span data-stu-id="023ef-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="023ef-130">D3DENUM \_ \_ . уровень лаборатории не был \_ удален, и \_ был \_ добавлен D3DENUM уровень WHQL.</span><span class="sxs-lookup"><span data-stu-id="023ef-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="023ef-131">Создание изменений ресурсов</span><span class="sxs-lookup"><span data-stu-id="023ef-131">Create Resource Changes</span></span>

<span data-ttu-id="023ef-132">К нескольким методам был добавлен маркер, и для него должно быть задано **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="023ef-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="023ef-133">К этим методам относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="023ef-133">The methods affected include:</span></span>

-   [<span data-ttu-id="023ef-134">**креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="023ef-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="023ef-135">**креатеволуметекстуре**</span><span class="sxs-lookup"><span data-stu-id="023ef-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="023ef-136">**креатекубетекстуре**</span><span class="sxs-lookup"><span data-stu-id="023ef-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="023ef-137">**креатевертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="023ef-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="023ef-138">**креатеиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="023ef-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="023ef-139">**креатерендертаржет**</span><span class="sxs-lookup"><span data-stu-id="023ef-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="023ef-140">**креатедепсстенЦилсурфаце**</span><span class="sxs-lookup"><span data-stu-id="023ef-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="023ef-141">**креатеоффскринплаинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="023ef-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="023ef-142">Енумадаптермодес изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="023ef-143">Теперь [**енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) принимает D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="023ef-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="023ef-144">Формат поддерживает расширяемый набор режимов экрана.</span><span class="sxs-lookup"><span data-stu-id="023ef-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="023ef-145">Чтобы защитить приложения от перечислений форматов, которые не были выпущены при отгрузке приложения, приложение должно сообщить Direct3D формат для режимов экрана, которые необходимо перечислить.</span><span class="sxs-lookup"><span data-stu-id="023ef-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="023ef-146">Результирующий массив режимов вывода будет отличаться только шириной, высотой и частотой обновления.</span><span class="sxs-lookup"><span data-stu-id="023ef-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="023ef-147">Приложение указывает формат пикселей, а перечисление ограничено теми режимами экрана, которые точно соответствуют формату.</span><span class="sxs-lookup"><span data-stu-id="023ef-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="023ef-148">Ниже приведен список разрешенных форматов.</span><span class="sxs-lookup"><span data-stu-id="023ef-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="023ef-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="023ef-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="023ef-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="023ef-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="023ef-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="023ef-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="023ef-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="023ef-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="023ef-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="023ef-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="023ef-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="023ef-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="023ef-155">Перечисление эквивалентно для альфа-и неальфа-версий того же формата.</span><span class="sxs-lookup"><span data-stu-id="023ef-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="023ef-156">Возвращаемый формат всегда будет иметь тот же формат, что и приложение.</span><span class="sxs-lookup"><span data-stu-id="023ef-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="023ef-157">Этот метод обрабатывает 565 и 555 как эквивалентный и возвращает правильную версию в формате.</span><span class="sxs-lookup"><span data-stu-id="023ef-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="023ef-158">Разница вступает в игру только в том случае, если приложение блокирует задний буфер, и существует явный флаг, который приложение должно установить для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="023ef-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="023ef-159">Изменения Get и Сетстреамсаурце</span><span class="sxs-lookup"><span data-stu-id="023ef-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="023ef-160">К методам [**жетстреамсаурце**](/windows/desktop/api) и [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) был добавлен один параметр.</span><span class="sxs-lookup"><span data-stu-id="023ef-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="023ef-161">Смещение — это число байтов между началом потока и началом данных вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="023ef-162">Измеряется в байтах.</span><span class="sxs-lookup"><span data-stu-id="023ef-162">It is measured in bytes.</span></span> <span data-ttu-id="023ef-163">Это позволяет конвейеру поддерживать смещения потоков.</span><span class="sxs-lookup"><span data-stu-id="023ef-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="023ef-164">Чтобы узнать, поддерживает ли устройство смещения потоков, см. раздел D3DDEVCAPS2 \_ стреамоффсет.</span><span class="sxs-lookup"><span data-stu-id="023ef-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="023ef-165">Изменение качества с множественной выборкой</span><span class="sxs-lookup"><span data-stu-id="023ef-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="023ef-166">Ранее было \_ Перечисление типов D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="023ef-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="023ef-167">Direct3D 9 удерживает это перечисление и добавляет идею уровня качества для каждого элемента перечисления.</span><span class="sxs-lookup"><span data-stu-id="023ef-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="023ef-168">Уровень качества указывает на компромисс между качеством и производительностью, указывая число образцов с маской (в смысле D3DRS \_ мултисамплемаск).</span><span class="sxs-lookup"><span data-stu-id="023ef-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="023ef-169">Приложение должно выбрать, сколько примеров для маскирования требуется, а затем обратиться к Пкуалитилевелс.</span><span class="sxs-lookup"><span data-stu-id="023ef-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="023ef-170">Если не равно нулю, это значение указывает количество уровней качества, которое приложение может передать различным функциям создания через Мултисамплекуалити.</span><span class="sxs-lookup"><span data-stu-id="023ef-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="023ef-171">Поскольку драйверы предоставляют все свои Многовыборочные схемы как уровни качества в D3DMULTISAMPLE \_ без маскировки, можно перечислить все доступные Многовыборочные схемы с помощью этого типа, если приложению не нужно маскировать образцы.</span><span class="sxs-lookup"><span data-stu-id="023ef-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="023ef-172">Бит D3DPRASTERCAPS \_ стретчблтмултисампле Caps снят с учета.</span><span class="sxs-lookup"><span data-stu-id="023ef-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="023ef-173">Этот бит используется для обозначения того, что метод многовыборки не поддерживал маски записи и не может быть включен и отключен между [**бегинсцене**](/windows/desktop/api) и [**ендсцене**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span><span class="sxs-lookup"><span data-stu-id="023ef-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="023ef-174">Такие немаскированные методы теперь доступны через D3DMULTISAMPLE без \_ маскировки.</span><span class="sxs-lookup"><span data-stu-id="023ef-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="023ef-175">Для каждого числа образцов с маской существует другое значение.</span><span class="sxs-lookup"><span data-stu-id="023ef-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="023ef-176">Например, примеры D3DMULTISAMPLE \_ 4 \_ могут иметь три уровня качества, тогда как у D3DMULTISAMPLE \_ 2 \_ образцов может быть только один.</span><span class="sxs-lookup"><span data-stu-id="023ef-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="023ef-177">Существует не более восьми уровней качества для каждого числа образцов с маской (драйвер не может выразить больше).</span><span class="sxs-lookup"><span data-stu-id="023ef-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="023ef-178">Диапазон качества — от нуля до ( \* пкуалитилевелс-1).</span><span class="sxs-lookup"><span data-stu-id="023ef-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="023ef-179">Ресаурцеманажердискардбитес изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="023ef-180">Ресаурцеманажердискардбитес был заменен IDirect3DDevice9:: Евиктманажедресаурцес.</span><span class="sxs-lookup"><span data-stu-id="023ef-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="023ef-181">Он может исключить все ресурсы, как Direct3D, так и драйверы.</span><span class="sxs-lookup"><span data-stu-id="023ef-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="023ef-182">Диспетчер ресурсов теперь обращается к, когда происходит сбой создания ресурса (управляемого или неуправляемого) из-за нехватки памяти видео.</span><span class="sxs-lookup"><span data-stu-id="023ef-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="023ef-183">Руководителю будет автоматически предложено освободить достаточно ресурсов, чтобы процесс создания был выполнен.</span><span class="sxs-lookup"><span data-stu-id="023ef-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="023ef-184">В DirectX 8,0 этот процесс не был автоматизирован.</span><span class="sxs-lookup"><span data-stu-id="023ef-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="023ef-185">Сетсофтваревертекспроцессинг изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="023ef-186">Приложение может создать устройство в смешанном режиме для использования обработки вершин программного обеспечения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="023ef-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="023ef-187">Чтобы переключиться между двумя режимами обработки вершин в DirectX 8. x, вызовите IDirect3DDevice8:: Сетрендерстате.</span><span class="sxs-lookup"><span data-stu-id="023ef-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="023ef-188">Это было заменено на [**сетсофтваревертекспроцессинг**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) для упрощения проблем, вызванных блоками состояния.</span><span class="sxs-lookup"><span data-stu-id="023ef-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="023ef-189">Этот новый метод не записывается блоками состояния.</span><span class="sxs-lookup"><span data-stu-id="023ef-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="023ef-190">Изменения в образце текстур</span><span class="sxs-lookup"><span data-stu-id="023ef-190">Texture Sampler Changes</span></span>

<span data-ttu-id="023ef-191">Direct3D 9 поддерживает до 16 поверхностей текстуры за один проход, используя модель шейдера Pixel Shader 2 \_ 0, однако число координат текстуры остается ограниченным восемью.</span><span class="sxs-lookup"><span data-stu-id="023ef-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="023ef-192">Состояние этапа текстуры связано с поверхностями, наборами координат, обработкой вершин и обработкой пикселей.</span><span class="sxs-lookup"><span data-stu-id="023ef-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="023ef-193">Для управления этими различиями во время компиляции [**сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) разбивается на два метода:</span><span class="sxs-lookup"><span data-stu-id="023ef-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="023ef-194">IDirect3DDevice9:: Сеттекстурестажестате будет по-прежнему использоваться для состояния координат текстуры, например для режимов переноса и создания координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="023ef-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="023ef-195">[**Сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) был добавлен и теперь будет использоваться для фильтрации, мозаичного заполнения, фиксации, миплод и т. д.</span><span class="sxs-lookup"><span data-stu-id="023ef-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="023ef-196">Это можно настроить до шестнадцати пробных выработок.</span><span class="sxs-lookup"><span data-stu-id="023ef-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="023ef-197">Сеттекстурестажестате изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="023ef-198">IDirect3DDevice9:: Сеттекстурестажестате теперь задает следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="023ef-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="023ef-199">Состояние обработки фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="023ef-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="023ef-200">Это состояние управляет обработкой координат текстуры D3DTSS \_ текстуретрансформфлагс и D3DTSS \_ текскурдиндекс.</span><span class="sxs-lookup"><span data-stu-id="023ef-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="023ef-201">Можно задать до восьми экземпляров (поскольку восемь координат текстуры всегда поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="023ef-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="023ef-202">D3DTSS \_ текскурдиндекс — это состояние обработки фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="023ef-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="023ef-203">Если используется программируемый шейдер вершин, это состояние игнорируется.</span><span class="sxs-lookup"><span data-stu-id="023ef-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="023ef-204">Фиксированное состояние шейдера пикселей функции (устаревший Текстурестажестате).</span><span class="sxs-lookup"><span data-stu-id="023ef-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="023ef-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="023ef-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="023ef-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="023ef-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="023ef-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="023ef-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="023ef-208">D3DTSS \_ алфаоп</span><span class="sxs-lookup"><span data-stu-id="023ef-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="023ef-209">D3DTSS \_ бумпенвлоффсет</span><span class="sxs-lookup"><span data-stu-id="023ef-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="023ef-210">D3DTSS \_ бумпенвлскале</span><span class="sxs-lookup"><span data-stu-id="023ef-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="023ef-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="023ef-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="023ef-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="023ef-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="023ef-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="023ef-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="023ef-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="023ef-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="023ef-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="023ef-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="023ef-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="023ef-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="023ef-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="023ef-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="023ef-218">D3DTSS \_ колороп</span><span class="sxs-lookup"><span data-stu-id="023ef-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="023ef-219">D3DTSS \_ ресултарг</span><span class="sxs-lookup"><span data-stu-id="023ef-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="023ef-220">Число состояний шейдера с фиксированной функцией, которые могут быть заданы, меньше или равно числу, представленному параметром Макстекстуреблендстажес.</span><span class="sxs-lookup"><span data-stu-id="023ef-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="023ef-221">Число доступных для приложения образцов текстуры определяется версией шейдера пикселей, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="023ef-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="023ef-222">Имя</span><span class="sxs-lookup"><span data-stu-id="023ef-222">Name</span></span>                    | <span data-ttu-id="023ef-223">Число</span><span class="sxs-lookup"><span data-stu-id="023ef-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="023ef-224">PS \_ 1 \_ 1 – PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="023ef-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="023ef-225">4 образцов текстуры</span><span class="sxs-lookup"><span data-stu-id="023ef-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="023ef-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="023ef-226">ps\_1\_4</span></span>                | <span data-ttu-id="023ef-227">6 образцов текстуры</span><span class="sxs-lookup"><span data-stu-id="023ef-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="023ef-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="023ef-228">ps\_2\_0</span></span>                | <span data-ttu-id="023ef-229">16 образцов текстуры</span><span class="sxs-lookup"><span data-stu-id="023ef-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="023ef-230">фиксированный конвейер функций</span><span class="sxs-lookup"><span data-stu-id="023ef-230">fixed function pipeline</span></span> | <span data-ttu-id="023ef-231">Макстекстуреблендстажес/Макссимултанеаустекстуресные пробы</span><span class="sxs-lookup"><span data-stu-id="023ef-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="023ef-232">Устройства, поддерживающие сопоставление смещений в Direct3D 9, будут поддерживать дополнительный образец (D3DDMAPSAMPLER), который показывает карты смещения в блоке тесселяции.</span><span class="sxs-lookup"><span data-stu-id="023ef-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="023ef-233">Сетсамплерстате изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-233">SetSamplerState Changes</span></span>

<span data-ttu-id="023ef-234">IDirect3DDevice9:: Сетсамплерстате задает состояние образца (включая ту, которая используется в блоке тесселяции для выборки карт смещения).</span><span class="sxs-lookup"><span data-stu-id="023ef-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="023ef-235">Они были переименованы с \_ префиксом D3DSAMP, чтобы включить обнаружение ошибок во время компиляции при переносе из DirectX 8. x.</span><span class="sxs-lookup"><span data-stu-id="023ef-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="023ef-236">Возможные состояния:</span><span class="sxs-lookup"><span data-stu-id="023ef-236">The states include:</span></span>

-   <span data-ttu-id="023ef-237">D3DSAMP \_ аддрессу</span><span class="sxs-lookup"><span data-stu-id="023ef-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="023ef-238">D3DSAMP \_ аддрессв</span><span class="sxs-lookup"><span data-stu-id="023ef-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="023ef-239">D3DSAMP \_ аддрессв</span><span class="sxs-lookup"><span data-stu-id="023ef-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="023ef-240">D3DSAMP \_ BORDERCOLOR</span><span class="sxs-lookup"><span data-stu-id="023ef-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="023ef-241">D3DSAMP \_ магфилтер</span><span class="sxs-lookup"><span data-stu-id="023ef-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="023ef-242">D3DSAMP \_ максанисотропи</span><span class="sxs-lookup"><span data-stu-id="023ef-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="023ef-243">D3DSAMP \_ максмиплевел</span><span class="sxs-lookup"><span data-stu-id="023ef-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="023ef-244">D3DSAMP \_ минфилтер</span><span class="sxs-lookup"><span data-stu-id="023ef-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="023ef-245">D3DSAMP \_ мипфилтер</span><span class="sxs-lookup"><span data-stu-id="023ef-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="023ef-246">D3DSAMP \_ мипмаплодбиас</span><span class="sxs-lookup"><span data-stu-id="023ef-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="023ef-247">Изменения в объявлении вершин</span><span class="sxs-lookup"><span data-stu-id="023ef-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="023ef-248">Объявления вершин теперь отделены от создания шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="023ef-249">Объявления вершин теперь используют интерфейс модели COM.</span><span class="sxs-lookup"><span data-stu-id="023ef-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="023ef-250">Для DirectX 8. x объявления вершин привязаны к шейдерам вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="023ef-251">Для конвейера фиксированной функции вызовите [**сетвертексшадер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) с помощью кода гибкого формата вершины (фвф) в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="023ef-252">Для шейдеров вершин вызовите IDirect3DDevice9:: Сетвертексшадер с маркером ранее созданного шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="023ef-253">Шейдер включает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="023ef-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="023ef-254">Для Direct3D 9 объявления вершин отделены от шейдеров вершин и могут использоваться с фиксированным конвейером функций или с шейдерами.</span><span class="sxs-lookup"><span data-stu-id="023ef-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="023ef-255">Для конвейера фиксированной функции нет необходимости вызывать IDirect3DDevice9:: Сетвертексшадер.</span><span class="sxs-lookup"><span data-stu-id="023ef-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="023ef-256">Однако если вы хотите переключиться на конвейер фиксированной функции и ранее использовала шейдер вершин, вызовите IDirect3DDevice9:: Сетвертексшадер (**null**).</span><span class="sxs-lookup"><span data-stu-id="023ef-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="023ef-257">Когда это будет сделано, вам все равно потребуется вызвать [**сетфвф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) для объявления кода фвф.</span><span class="sxs-lookup"><span data-stu-id="023ef-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="023ef-258">При использовании шейдеров вершин вызовите IDirect3DDevice9:: Сетвертексшадер с объектом шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="023ef-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="023ef-259">Кроме того, вызовите метод IDirect3DDevice9:: Сетфвф, чтобы настроить объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="023ef-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="023ef-260">При этом используются сведения, неявные в ФВФ.</span><span class="sxs-lookup"><span data-stu-id="023ef-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="023ef-261">[**Сетвертексдекларатион**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) может быть вызван вместо IDirect3DDevice9:: сетфвф, так как он поддерживает объявления вершин, которые не могут быть выражены с помощью фвф.</span><span class="sxs-lookup"><span data-stu-id="023ef-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="023ef-262">Интервалы и SwapEffects изменения</span><span class="sxs-lookup"><span data-stu-id="023ef-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="023ef-263">Было внесено несколько изменений, чтобы предоставить пользователю больший контроль над частотой обновления монитора, частотой представления, а также фоновым буфером и рисованием заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="023ef-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="023ef-264">Вот они:</span><span class="sxs-lookup"><span data-stu-id="023ef-264">They are as follows:</span></span>

-   <span data-ttu-id="023ef-265">Удален один из эффектов переключения, D3DSWAPEFFECT \_ Copy \_ вертикальной синхронизации и один уровень представления, D3DPRESENTная \_ ставка \_ без ограничений.</span><span class="sxs-lookup"><span data-stu-id="023ef-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="023ef-266">Переименованные \_ Параметры D3DPRESENT. Полноэкранный \_ пресентатионинтервал до пресентатионинтервалс.</span><span class="sxs-lookup"><span data-stu-id="023ef-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="023ef-267">\_Немедленный добавлен интервал D3DPRESENT \_ , что означает, что презентация не синхронизирована с вертикальной синхронизацией. Как и в DirectX 8. x, D3DPRESENT \_ интервал \_ по умолчанию определяется как ноль и эквивалентен D3DPRESENT \_ Interval \_ 1.</span><span class="sxs-lookup"><span data-stu-id="023ef-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="023ef-268">D3DPRESENT \_ Interval \_ по умолчанию — это удобство для инициализации \_ параметров D3DPRESENT равным нулю.</span><span class="sxs-lookup"><span data-stu-id="023ef-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="023ef-269">Подробное описание режимов и поддерживаемых интервалов см. в разделе D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="023ef-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="023ef-270">См. также</span><span class="sxs-lookup"><span data-stu-id="023ef-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="023ef-271">Графика Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="023ef-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 
