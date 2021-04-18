---
description: Сжатие блока — это метод сжатия текстур для уменьшения их размера.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Блочное сжатие (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565290"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="fc776-103">Блочное сжатие (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fc776-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="fc776-104">Сжатие блока — это метод сжатия текстур для уменьшения их размера.</span><span class="sxs-lookup"><span data-stu-id="fc776-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="fc776-105">По сравнению с текстурой с 32 битами на цвет текстура со сжатыми блоками может быть до 75 % меньше.</span><span class="sxs-lookup"><span data-stu-id="fc776-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="fc776-106">Как правило, приложения начинают работать быстрее при использовании сжатия блоков, поскольку нагрузка на память снижается.</span><span class="sxs-lookup"><span data-stu-id="fc776-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="fc776-107">Сжатие блоков выполняется с потерями, однако работает хорошо и рекомендуется для всех текстур, преобразуемых и фильтруемых конвейером.</span><span class="sxs-lookup"><span data-stu-id="fc776-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="fc776-108">Текстуры, которые напрямую сопоставляются экрану (элементы пользовательского интерфейса, такие как значки и текст), не очень подходят для сжатия, поскольку артефакты более заметны.</span><span class="sxs-lookup"><span data-stu-id="fc776-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="fc776-109">Текстура со сжатыми блоками должна создаваться как кратная размеру 4 во всех измерениях, ее невозможно использовать в качестве выходных данных конвейера.</span><span class="sxs-lookup"><span data-stu-id="fc776-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="fc776-110">Как работает сжатие блокировок?</span><span class="sxs-lookup"><span data-stu-id="fc776-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="fc776-111">Хранение несжатых данных</span><span class="sxs-lookup"><span data-stu-id="fc776-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="fc776-112">Хранение сжатых данных</span><span class="sxs-lookup"><span data-stu-id="fc776-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="fc776-113">Использование блочного сжатия</span><span class="sxs-lookup"><span data-stu-id="fc776-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="fc776-114">Виртуальный размер и физический размер</span><span class="sxs-lookup"><span data-stu-id="fc776-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="fc776-115">Алгоритмы сжатия</span><span class="sxs-lookup"><span data-stu-id="fc776-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="fc776-116">BC1</span><span class="sxs-lookup"><span data-stu-id="fc776-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="fc776-117">BC2</span><span class="sxs-lookup"><span data-stu-id="fc776-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="fc776-118">BC3</span><span class="sxs-lookup"><span data-stu-id="fc776-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="fc776-119">BC4</span><span class="sxs-lookup"><span data-stu-id="fc776-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="fc776-120">BC5</span><span class="sxs-lookup"><span data-stu-id="fc776-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="fc776-121">Преобразование формата с помощью Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="fc776-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="fc776-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fc776-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="fc776-123">Как работает сжатие блокировок?</span><span class="sxs-lookup"><span data-stu-id="fc776-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="fc776-124">Сжатие блоков — это метод уменьшения объема памяти, необходимой для хранения данных цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="fc776-125">Сохраняя некоторые цвета в первоначальном размере, а другие — с использованием схемы кодирования, можно существенно уменьшить объем памяти, необходимый для хранения изображения.</span><span class="sxs-lookup"><span data-stu-id="fc776-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="fc776-126">Поскольку оборудование автоматически декодирует сжатые данные, использование сжатых текстур не приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="fc776-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="fc776-127">Чтобы узнать, как работает сжатие, рассмотрите следующие два примера.</span><span class="sxs-lookup"><span data-stu-id="fc776-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="fc776-128">В первом примере описывается объем памяти, используемой при хранении несжатых данных; а второй — объем памяти при хранении сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="fc776-129">Хранение несжатых данных</span><span class="sxs-lookup"><span data-stu-id="fc776-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="fc776-130">На следующем рисунке показана текстура 4×4 без сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="fc776-131">Допустим, каждый цвет имеет один компонент цвета (например, красный) и хранится в одном байте памяти.</span><span class="sxs-lookup"><span data-stu-id="fc776-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![Иллюстрация несжатой текстуры 4x4](images/d3d10-block-compress-1.png)

<span data-ttu-id="fc776-133">Несжатые данные располагаются в памяти последовательно и требуют 16 байтов для хранения, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="fc776-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![Иллюстрация несжатых данных в последовательной памяти](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="fc776-135">Хранение сжатых данных</span><span class="sxs-lookup"><span data-stu-id="fc776-135">Storing Compressed Data</span></span>

<span data-ttu-id="fc776-136">Вы увидели, сколько памяти требуется для хранения несжатого изображения. А теперь посмотрим, сколько памяти экономит сжатое изображение.</span><span class="sxs-lookup"><span data-stu-id="fc776-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="fc776-137">Формат сжатия [BC1](#bc1) сохраняет 2 цвета (по 1 байту каждый) и 16 3-битовых индексов (48 битов или 6 байтов), которые используются для интерполяции первоначальных цветов в текстуре, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="fc776-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![Иллюстрация формата сжатия BC1](images/d3d10-block-compress-3.png)

<span data-ttu-id="fc776-139">Совокупное пространство, необходимое для хранения сжатых данных, равно 8 байтов, то есть экономия памяти составляет 50 % по сравнению с примером без сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="fc776-140">Экономия увеличивается, если используется несколько компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="fc776-141">Значительная экономия памяти, обеспечиваемая сжатием блоков, позволяет существенно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="fc776-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="fc776-142">Это повышение производительности происходит за счет снижения качества изображения (из-за интерполяции цвета); однако более низкое качество не всегда заметно.</span><span class="sxs-lookup"><span data-stu-id="fc776-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="fc776-143">В следующем разделе показано, как Direct3D 10 упрощает использование блочного сжатия в приложении.</span><span class="sxs-lookup"><span data-stu-id="fc776-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="fc776-144">Использование блочного сжатия</span><span class="sxs-lookup"><span data-stu-id="fc776-144">Using Block Compression</span></span>

<span data-ttu-id="fc776-145">Создайте текстуру с сжатием блока точно так же, как несжатая текстура (см. раздел [Создание текстуры из файла](d3d10-graphics-programming-guide-resources-creating-textures.md)), за исключением того, что вы указали формат, сжатый в виде блока.</span><span class="sxs-lookup"><span data-stu-id="fc776-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="fc776-146">Затем создайте представление для привязки текстуры к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="fc776-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="fc776-147">Так как текстура с сжатием блока может использоваться только в качестве входных данных для этапа шейдера, необходимо создать представление шейдера, вызвав [**креатешадерресаурцевиев**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="fc776-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="fc776-148">Используйте текстуру со сжатыми блоками так же, как вы бы использовали текстуру без сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="fc776-149">Если ваше приложение будет использовать указатель памяти на данные со сжатием блоков, потребуется учетная запись для заполнения памяти в MIP-карте, из-за чего объявленный размер может отличаться от фактического.</span><span class="sxs-lookup"><span data-stu-id="fc776-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="fc776-150">Виртуальный размер и физический размер</span><span class="sxs-lookup"><span data-stu-id="fc776-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="fc776-151">Если у вас есть код приложения, который использует указатель памяти для прохода памяти текстуры со сжатием блоков, существует один важный аспект, который может потребовать изменения кода приложения.</span><span class="sxs-lookup"><span data-stu-id="fc776-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="fc776-152">Текстура со сжатием блоков должна быть кратна 4 во всех измерениях, поскольку алгоритмы сжатия блоков работают с блоками текселей 4x4.</span><span class="sxs-lookup"><span data-stu-id="fc776-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="fc776-153">Это может представлять проблему для MIP-карты, первоначальные габариты которой кратны 4, а подразделенные уровни — нет.</span><span class="sxs-lookup"><span data-stu-id="fc776-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="fc776-154">На следующей схеме показаны различия областей между виртуальным (объявленным) и физическим (фактическим) размером каждого уровня MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="fc776-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![Схема несжатых и сжатых уровней mipmap](images/d3d10-block-compress-pad.png)

<span data-ttu-id="fc776-156">В левой части схемы показаны размеры уровня MIP-карты, создаваемые для несжатой текстуры 60×40.</span><span class="sxs-lookup"><span data-stu-id="fc776-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="fc776-157">Размер верхнего уровня взят из вызова API, создающего текстуру; размер каждого последующего уровня равен половине размера предыдущего уровня.</span><span class="sxs-lookup"><span data-stu-id="fc776-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="fc776-158">Для несжатой текстуры нет различия между виртуальным (объявленным) и физическим (фактическим) размером.</span><span class="sxs-lookup"><span data-stu-id="fc776-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="fc776-159">В правой части схемы показаны размеры уровня MIP-карты, которые создаются для той же текстуры 60×40 со сжатием.</span><span class="sxs-lookup"><span data-stu-id="fc776-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="fc776-160">Обратите внимание, что на втором и третьем уровнях используется заполнение памяти, чтобы сделать размеры кратными 4 на каждом уровне.</span><span class="sxs-lookup"><span data-stu-id="fc776-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="fc776-161">Это необходимо, чтобы эти алгоритмы могли работать с блоками текселей 4×4.</span><span class="sxs-lookup"><span data-stu-id="fc776-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="fc776-162">Это особенно очевидно, если вы рассматриваете уровни MIP-карт менее 4×4; размеры этих очень маленьких MIP-карт при выделении памяти текстуры будут округляться до ближайшего кратного 4 числа.</span><span class="sxs-lookup"><span data-stu-id="fc776-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="fc776-163">Оборудование для выборки использует виртуальный размер; при выборке текстуры заполнение памяти игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fc776-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="fc776-164">Для уровней MIP-карт менее 4×4 только первые четыре текселя будут использоваться для карты 2×2 и только первый тексель будет использоваться для блока 1×1.</span><span class="sxs-lookup"><span data-stu-id="fc776-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="fc776-165">Однако нет структуры API, которая предоставляет физический размер (включая заполнение памяти).</span><span class="sxs-lookup"><span data-stu-id="fc776-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="fc776-166">Необходимо с большой осторожностью пользоваться выровненными блоками памяти при копировании регионов, которые содержат данные со сжатием блоков.</span><span class="sxs-lookup"><span data-stu-id="fc776-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="fc776-167">Чтобы сделать это в приложении с указателем памяти, убедитесь, что указатель использует шаг поверхности для учета размера физической памяти.</span><span class="sxs-lookup"><span data-stu-id="fc776-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="fc776-168">Алгоритмы сжатия</span><span class="sxs-lookup"><span data-stu-id="fc776-168">Compression Algorithms</span></span>

<span data-ttu-id="fc776-169">Техника сжатия блоков в Direct3D подразумевает разделение данных несжатой текстуры в блоки 4×4, сжатие каждого блока и последующее сохранение файлов.</span><span class="sxs-lookup"><span data-stu-id="fc776-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="fc776-170">По этой причине сжимаемые текстуры должны иметь габариты, кратные 4.</span><span class="sxs-lookup"><span data-stu-id="fc776-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![Схема блочного сжатия](images/d3d10-compression-1.png)

<span data-ttu-id="fc776-172">На предыдущей схеме показана текстура, разделенная на блоки текселей.</span><span class="sxs-lookup"><span data-stu-id="fc776-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="fc776-173">Первый блок показывает структуру 16 текселей, помеченных с a до p, однако во всех блоках данные организованы одинаково.</span><span class="sxs-lookup"><span data-stu-id="fc776-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="fc776-174">Direct3D реализует несколько схем сжатия, каждая из которых представляет собой разные компромиссы между количеством хранимых компонентов, количеством битов на компонент и объемом потребляемой памяти.</span><span class="sxs-lookup"><span data-stu-id="fc776-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="fc776-175">Воспользуйтесь этой таблицей, чтобы выбрать формат, который больше всего подходит для вашего типа и разрешения данных в приложении.</span><span class="sxs-lookup"><span data-stu-id="fc776-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="fc776-176">Исходные данные</span><span class="sxs-lookup"><span data-stu-id="fc776-176">Source Data</span></span>                     | <span data-ttu-id="fc776-177">Разрешение сжатия данных (в битах)</span><span class="sxs-lookup"><span data-stu-id="fc776-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="fc776-178">Выберите этот формат сжатия</span><span class="sxs-lookup"><span data-stu-id="fc776-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="fc776-179">Трех-компонентный цвет и альфа</span><span class="sxs-lookup"><span data-stu-id="fc776-179">Three-component color and alpha</span></span> | <span data-ttu-id="fc776-180">Цвет (5:6:5), альфа (1) или без альфа</span><span class="sxs-lookup"><span data-stu-id="fc776-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="fc776-181">BC1</span><span class="sxs-lookup"><span data-stu-id="fc776-181">BC1</span></span>                            |
| <span data-ttu-id="fc776-182">Трех-компонентный цвет и альфа</span><span class="sxs-lookup"><span data-stu-id="fc776-182">Three-component color and alpha</span></span> | <span data-ttu-id="fc776-183">Цвет (5:6:5), альфа (4)</span><span class="sxs-lookup"><span data-stu-id="fc776-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="fc776-184">BC2</span><span class="sxs-lookup"><span data-stu-id="fc776-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="fc776-185">Трех-компонентный цвет и альфа</span><span class="sxs-lookup"><span data-stu-id="fc776-185">Three-component color and alpha</span></span> | <span data-ttu-id="fc776-186">Цвет (5:6:5), альфа (8)</span><span class="sxs-lookup"><span data-stu-id="fc776-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="fc776-187">BC3</span><span class="sxs-lookup"><span data-stu-id="fc776-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="fc776-188">Однокомпонентный цвет</span><span class="sxs-lookup"><span data-stu-id="fc776-188">One-component color</span></span>             | <span data-ttu-id="fc776-189">Один компонент (8)</span><span class="sxs-lookup"><span data-stu-id="fc776-189">One component (8)</span></span>                     | [<span data-ttu-id="fc776-190">BC4</span><span class="sxs-lookup"><span data-stu-id="fc776-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="fc776-191">Двухкомпонентный цвет</span><span class="sxs-lookup"><span data-stu-id="fc776-191">Two-component color</span></span>             | <span data-ttu-id="fc776-192">Два компонента (8:8)</span><span class="sxs-lookup"><span data-stu-id="fc776-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="fc776-193">BC5</span><span class="sxs-lookup"><span data-stu-id="fc776-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="fc776-194">BC1</span><span class="sxs-lookup"><span data-stu-id="fc776-194">BC1</span></span>

<span data-ttu-id="fc776-195">Используйте первый формат сжатия блоков (BC1) (в формате DXGI \_ \_ BC1 \_ Type, \_ \_ BC1 \_ UNORM или DXGI \_ BC1 \_ UNORM \_ sRGB) для хранения данных цвета с тремя компонентами, используя цвет 5:6:5 (5 бит красного, 6 бит зеленого, 5 бит синего цвета).</span><span class="sxs-lookup"><span data-stu-id="fc776-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="fc776-196">Это актуально, даже если данные также содержат 1-битовый альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="fc776-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="fc776-197">Допустим, текстура 4×4 использует самый крупный из возможных форматов данных. В этом случае формат BC1 уменьшает объем необходимой памяти с 48 байтов (16 цветов × 3 компонента/цвет × 1 байт/компонент) до 8 байтов.</span><span class="sxs-lookup"><span data-stu-id="fc776-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="fc776-198">Этот алгоритм работает в блоках текселей 4×4.</span><span class="sxs-lookup"><span data-stu-id="fc776-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="fc776-199">Вместо того чтобы хранить 16 цветов, алгоритм сохраняет 2 эталонных цвета (цвет \_ 0 и цвет \_ 1) и 16 2-разрядные индексы цвета (Block a – p), как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="fc776-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![Схема макета для сжатия BC1](images/d3d10-compression-bc1.png)

<span data-ttu-id="fc776-201">Индексы цвета (a–p) используются для поиска первоначальных цветов в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="fc776-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="fc776-202">Таблица цветов содержит 4 цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-202">The color table contains 4 colors.</span></span> <span data-ttu-id="fc776-203">Первые два цвета — цвет \_ 0 и цвет \_ 1 — являются минимальным и максимальным цветом.</span><span class="sxs-lookup"><span data-stu-id="fc776-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="fc776-204">Другие два цвета, цвет \_ 2 и цвет \_ 3, являются промежуточными цветами, вычисляемыми с помощью линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="fc776-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="fc776-205">Четырем цветам назначаются 2-битовые значения индекса, которые сохраняются в блоках a–p.</span><span class="sxs-lookup"><span data-stu-id="fc776-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="fc776-206">Наконец, все цвета в блоках a–p сравниваются с четырьмя цветами в таблице цветов, и индекс ближайшего цвета сохраняется в 2-битовых блоках.</span><span class="sxs-lookup"><span data-stu-id="fc776-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="fc776-207">Этот алгоритм пригоден для данных, которые также содержит 1-битовый альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="fc776-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="fc776-208">Единственное отличие заключается в том, что цвет \_ 3 имеет значение 0 (что представляет собой прозрачный цвет), а цвет \_ 2 — линейное смешение цвета \_ 0 и цвета \_ 1.</span><span class="sxs-lookup"><span data-stu-id="fc776-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc776-209">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="fc776-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="fc776-210">Этот формат существует как в Direct3D 9, так и в 10.</span><span class="sxs-lookup"><span data-stu-id="fc776-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="fc776-211">В Direct3D 9 формат BC1 называется D3DFMT_DXT1.</span><span class="sxs-lookup"><span data-stu-id="fc776-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="fc776-212">В Direct3D 10 формат BC1 представлен DXGI_FORMAT_BC1_UNORM или DXGI_FORMAT_BC1_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="fc776-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="fc776-213">BC2</span><span class="sxs-lookup"><span data-stu-id="fc776-213">BC2</span></span>

<span data-ttu-id="fc776-214">Используйте формат BC2 (в формате DXGI \_ \_ BC2 без \_ типов, в \_ формате DXGI \_ BC2 \_ UNORM или DXGI \_ BC2 \_ UNORM \_ sRGB) для хранения данных, содержащих цвет и альфа-данные с низкой согласованностью (используйте [BC3](#bc3) для обеспечения высокой согласованности альфа-данных).</span><span class="sxs-lookup"><span data-stu-id="fc776-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="fc776-215">Формат BC2 хранит данные RGB как цвет 5:6:5 (5 битов на красный, 6 битов на зеленый, 5 битов на синий), а альфа-канал — как отдельное 4-битовое значение.</span><span class="sxs-lookup"><span data-stu-id="fc776-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="fc776-216">Допустим, текстура 4×4 использует самый крупный из возможных форматов данных. В этом случае эта техника сжатия уменьшает объем необходимой памяти с 64 байтов (16 цветов × 4 компонента/цвет × 1 байт/компонент) до 16 байтов памяти.</span><span class="sxs-lookup"><span data-stu-id="fc776-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="fc776-217">Формат BC2 сохраняет цвета с тем же количеством битов и той же структурой данных, что и формат [BC1](#bc1); однако формату BC2 требуются дополнительно 64 бита памяти для хранения альфа-данных, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="fc776-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![Схема макета для сжатия BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc776-219">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="fc776-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="fc776-220">Этот формат существует как в Direct3D 9, так и в 10.</span><span class="sxs-lookup"><span data-stu-id="fc776-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="fc776-221">В Direct3D 9 формат BC2 называется D3DFMT_DXT2 и D3DFMT_DXT3.</span><span class="sxs-lookup"><span data-stu-id="fc776-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="fc776-222">В Direct3D 10 формат BC2 представлен DXGI_FORMAT_BC2_UNORM или DXGI_FORMAT_BC2_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="fc776-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="fc776-223">BC3</span><span class="sxs-lookup"><span data-stu-id="fc776-223">BC3</span></span>

<span data-ttu-id="fc776-224">Используйте формат BC3 (в формате DXGI \_ \_ BC3 \_ без типов, в \_ формате DXGI \_ BC3 \_ UNORM или DXGI \_ BC3 \_ UNORM \_ sRGB) для хранения данных цвета с высокой степенью согласованности (используйте [BC2](#bc2) с менее согласованными альфа-данными).</span><span class="sxs-lookup"><span data-stu-id="fc776-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="fc776-225">Формат BC3 сохраняет данные цвета с использованием цвета 5:6:5 (5 битов красного, 6 битов зеленого, 5 битов синего) и альфа-данные с использованием одного байта.</span><span class="sxs-lookup"><span data-stu-id="fc776-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="fc776-226">Допустим, текстура 4×4 использует самый крупный из возможных форматов данных. В этом случае эта техника сжатия уменьшает объем необходимой памяти с 64 байтов (16 цветов × 4 компонента/цвет × 1 байт/компонент) до 16 байтов памяти.</span><span class="sxs-lookup"><span data-stu-id="fc776-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="fc776-227">Формат BC3 сохраняет цвета с тем же количеством битов и той же структурой данных, что и формат [BC1](#bc1); однако формату BC3 требуются дополнительно 64 бита памяти для хранения альфа-данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="fc776-228">Формат BC3 обрабатывает альфа-канал, сохраняя два эталонных значения и выполняя интерполяцию между ними (аналогично сохранению цвета RGB в формате BC1).</span><span class="sxs-lookup"><span data-stu-id="fc776-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="fc776-229">Этот алгоритм работает в блоках текселей 4×4.</span><span class="sxs-lookup"><span data-stu-id="fc776-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="fc776-230">Вместо того чтобы хранить 16 альфа-значений, алгоритм сохраняет 2 ссылки (альфа \_ 0 и альфа \_ 1) и 16 3-битные индексы цвета (от Альфа a до p), как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="fc776-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![Схема макета для сжатия BC3](images/d3d10-compression-bc3.png)

<span data-ttu-id="fc776-232">Формат BC3 использует альфа-индексы (a–p) для поиска первоначальных цветов в таблице поиска, которая содержит 8 значений.</span><span class="sxs-lookup"><span data-stu-id="fc776-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="fc776-233">Первые два значения (альфа \_ 0 и альфа \_ 1) — это минимальное и максимальное значения; остальные шесть промежуточных значений рассчитываются с помощью линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="fc776-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="fc776-234">Алгоритм определяет количество интерполированных альфа-значений, анализируя два эталонных альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="fc776-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="fc776-235">Если альфа \_ 0 больше альфа \_ 1, то BC3 интерполирует 6 альфа-значений; в противном случае — интерполяцию 4.</span><span class="sxs-lookup"><span data-stu-id="fc776-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="fc776-236">Если BC3 интерполирует только 4 альфа-значения, он задает два дополнительных альфа-значения (0 для полностью прозрачного и 255 для полностью непрозрачного).</span><span class="sxs-lookup"><span data-stu-id="fc776-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="fc776-237">BC3 сжимает альфа-значения в области текселей 4×4, сохраняя битовый код, соответствующий интерполированным альфа-значениям, которые наиболее полно соответствуют исходному альфа-значению для заданного текселя.</span><span class="sxs-lookup"><span data-stu-id="fc776-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc776-238">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="fc776-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="fc776-239">В Direct3D 9 формат BC3 называется D3DFMT_DXT4 и D3DFMT_DXT5.</span><span class="sxs-lookup"><span data-stu-id="fc776-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="fc776-240">В Direct3D 10 формат BC3 представлен DXGI_FORMAT_BC3_UNORM или DXGI_FORMAT_BC3_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="fc776-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="fc776-241">BC4</span><span class="sxs-lookup"><span data-stu-id="fc776-241">BC4</span></span>

<span data-ttu-id="fc776-242">Используйте формат BC4 для хранения данных об однокомпонентном цвете с использованием 8 битов каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="fc776-243">В результате повышения точности (по сравнению с [BC1](#bc1)) BC4 идеально подходит для хранения данных с плавающей запятой в диапазоне от \[ 0 до 1 \] с помощью формата DXGI \_ \_ BC4 \_ UNORM и \[ от-1 до + 1 \] с использованием \_ формата DXGI \_ BC4 \_ снорм.</span><span class="sxs-lookup"><span data-stu-id="fc776-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="fc776-244">Допустим, текстура 4×4 использует самый крупный из возможных форматов данных. В этом случае эта техника сжатия уменьшает объем необходимой памяти с 16 байтов (16 цветов × 1 компонент/цвет × 1 байт/компонент) до 8 байтов.</span><span class="sxs-lookup"><span data-stu-id="fc776-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="fc776-245">Этот алгоритм работает в блоках текселей 4×4.</span><span class="sxs-lookup"><span data-stu-id="fc776-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="fc776-246">Вместо того чтобы хранить 16 цветов, алгоритм сохраняет 2 эталонных цвета (красный \_ 0 и красный \_ 1) и 16 3-битные индексы цвета (от красного до Красного p), как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="fc776-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![Схема макета для сжатия BC4](images/d3d10-compression-bc4.png)

<span data-ttu-id="fc776-248">Алгоритм использует 3-битовые индексы для поиска цветов в таблице цветов, которая содержит 8 элементов.</span><span class="sxs-lookup"><span data-stu-id="fc776-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="fc776-249">Первые два цвета (красный \_ 0 и красный \_ 1) — это минимальное и максимальное цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="fc776-250">Этот алгоритм вычисляет оставшиеся цвета с использованием линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="fc776-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="fc776-251">Алгоритм определяет количество интерполированных значений цвета, анализируя два эталонных значения.</span><span class="sxs-lookup"><span data-stu-id="fc776-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="fc776-252">Если красный \_ 0 больше, чем красный \_ 1, BC4 интерполирует 6 значений цвета; в противном случае — интерполяцию 4.</span><span class="sxs-lookup"><span data-stu-id="fc776-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="fc776-253">Если BC4 интерполирует только 4 значения цвета, задается два дополнительных значения цвета (0.0f для полностью прозрачного и 1.0f для полностью непрозрачного).</span><span class="sxs-lookup"><span data-stu-id="fc776-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="fc776-254">BC4 сжимает альфа-значения в области текселей 4×4, сохраняя битовый код, соответствующий интерполированным альфа-значениям, которые наиболее полно соответствуют исходному альфа-значению для заданного текселя.</span><span class="sxs-lookup"><span data-stu-id="fc776-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="fc776-255">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="fc776-256">BC4 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="fc776-257">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-257">BC4\_UNORM</span></span>

<span data-ttu-id="fc776-258">Следующий пример кода показывает, как выполняется интерполяция однокомпонентных данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="fc776-259">Эталонным цветам назначаются 3-битовые индексы (000–111, поскольку значений 8), которые сохраняются в блоках с red a до red p во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="fc776-260">BC4 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-260">BC4\_SNORM</span></span>

<span data-ttu-id="fc776-261">Формат DXGI \_ \_ BC4 \_ снорм точно такой же, за исключением того, что данные КОДИРУЮТСЯ в диапазоне снорм, а 4 значения цвета интерполируются.</span><span class="sxs-lookup"><span data-stu-id="fc776-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="fc776-262">Следующий пример кода показывает, как выполняется интерполяция однокомпонентных данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="fc776-263">Эталонным цветам назначаются 3-битовые индексы (000–111, поскольку значений 8), которые сохраняются в блоках с red a до red p во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="fc776-264">BC5</span><span class="sxs-lookup"><span data-stu-id="fc776-264">BC5</span></span>

<span data-ttu-id="fc776-265">Используйте формат BC5 для хранения данных о двухкомпонентном цвете с использованием 8 битов каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="fc776-266">В результате повышения точности (по сравнению с [BC1](#bc1)) Bc5 идеально подходит для хранения данных с плавающей запятой в диапазоне от \[ 0 до 1 \] с помощью формата DXGI \_ \_ Bc5 \_ UNORM и \[ от-1 до + 1 \] с использованием \_ формата DXGI \_ Bc5 \_ снорм.</span><span class="sxs-lookup"><span data-stu-id="fc776-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="fc776-267">Допустим, текстура 4×4 использует самый крупный из возможных форматов данных. В этом случае эта техника сжатия уменьшает объем необходимой памяти с 32 байтов (16 цветов × 2 компонента/цвет × 1 байт/компонент) до 16 байтов.</span><span class="sxs-lookup"><span data-stu-id="fc776-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="fc776-268">Этот алгоритм работает в блоках текселей 4×4.</span><span class="sxs-lookup"><span data-stu-id="fc776-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="fc776-269">Вместо того чтобы хранить 16 цветов для обоих компонентов, алгоритм сохраняет 2 эталонных цвета для каждого компонента (красный \_ 0, красный \_ 1, зеленый \_ 0 и зеленый \_ 1) и 16 3-битные индексы цвета для каждого компонента (от красного до Красного p и зеленого a до зеленого p), как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="fc776-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![Схема макета для сжатия Bc5](images/d3d10-compression-bc5.png)

<span data-ttu-id="fc776-271">Алгоритм использует 3-битовые индексы для поиска цветов в таблице цветов, которая содержит 8 элементов.</span><span class="sxs-lookup"><span data-stu-id="fc776-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="fc776-272">Первые два цвета — красный \_ 0 и красный \_ 1 (или зеленый \_ 0 и зеленый \_ 1) — — это минимальное и максимальное цвета.</span><span class="sxs-lookup"><span data-stu-id="fc776-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="fc776-273">Этот алгоритм вычисляет оставшиеся цвета с использованием линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="fc776-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="fc776-274">Алгоритм определяет количество интерполированных значений цвета, анализируя два эталонных значения.</span><span class="sxs-lookup"><span data-stu-id="fc776-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="fc776-275">Если красный \_ 0 больше, чем красный \_ 1, Bc5 интерполирует 6 значений цвета; в противном случае — интерполяцию 4.</span><span class="sxs-lookup"><span data-stu-id="fc776-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="fc776-276">Если BC5 интерполирует только 4 значения цвета, он задает остальные два значения цвета равными 0.0f и 1.0f.</span><span class="sxs-lookup"><span data-stu-id="fc776-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="fc776-277">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="fc776-278">BC5 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="fc776-279">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-279">BC5\_UNORM</span></span>

<span data-ttu-id="fc776-280">Следующий пример кода показывает, как выполняется интерполяция однокомпонентных данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="fc776-281">Вычисления для зеленых компонентов похожи.</span><span class="sxs-lookup"><span data-stu-id="fc776-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="fc776-282">Эталонным цветам назначаются 3-битовые индексы (000–111, поскольку значений 8), которые сохраняются в блоках с red a до red p во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="fc776-283">BC5 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-283">BC5\_SNORM</span></span>

<span data-ttu-id="fc776-284">Формат DXGI \_ \_ Bc5 \_ снорм точно такой же, за исключением того, что данные КОДИРУЮТСЯ в диапазоне снорм и когда 4 значения данных интерполируются, два дополнительных значения:-1,0 f и 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="fc776-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="fc776-285">Следующий пример кода показывает, как выполняется интерполяция однокомпонентных данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="fc776-286">Вычисления для зеленых компонентов похожи.</span><span class="sxs-lookup"><span data-stu-id="fc776-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="fc776-287">Эталонным цветам назначаются 3-битовые индексы (000–111, поскольку значений 8), которые сохраняются в блоках с red a до red p во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc776-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="fc776-288">Преобразование формата с помощью Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="fc776-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="fc776-289">Direct3D 10,1 обеспечивает копирование между предварительно структурированными текстурами и текстурами с блочным сжатием одинаковой битовой ширины.</span><span class="sxs-lookup"><span data-stu-id="fc776-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="fc776-290">Это можно сделать с помощью функций [**копиресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) и [**кописубресаурцерегион**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="fc776-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="fc776-291">Начиная с Direct3D 10,1, можно использовать [**копиресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) и [**кописубресаурцерегион**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) для копирования между несколькими типами форматов.</span><span class="sxs-lookup"><span data-stu-id="fc776-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="fc776-292">Этот тип операции копирования выполняет тип преобразования формата, который интерпретирует исходные данные как другой тип формата.</span><span class="sxs-lookup"><span data-stu-id="fc776-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="fc776-293">Рассмотрите этот пример, в котором показана разница между повторной интерпретацией данных с поведением более стандартного типа преобразования.</span><span class="sxs-lookup"><span data-stu-id="fc776-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="fc776-294">Чтобы пересчитать "f" в качестве типа "u", используйте [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span><span class="sxs-lookup"><span data-stu-id="fc776-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="fc776-295">В предыдущем примере повторной интерпретации базовое значение данных не меняется; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) повторно интерпретирует число с плавающей запятой как целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="fc776-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="fc776-296">Для выполнения более стандартного преобразования используйте следующее назначение:</span><span class="sxs-lookup"><span data-stu-id="fc776-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="fc776-297">В предыдущем преобразовании базовое значение изменений данных.</span><span class="sxs-lookup"><span data-stu-id="fc776-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="fc776-298">В следующей таблице перечислены допустимые форматы исходного объекта и объекта назначения, которые можно использовать в данном типе повторной интерпретации преобразования формата.</span><span class="sxs-lookup"><span data-stu-id="fc776-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="fc776-299">Необходимо кодировать значения надлежащим образом, чтобы повторная интерпретация работала правильно.</span><span class="sxs-lookup"><span data-stu-id="fc776-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="fc776-300">Ширина бита</span><span class="sxs-lookup"><span data-stu-id="fc776-300">Bit Width</span></span> | <span data-ttu-id="fc776-301">Несжатый ресурс</span><span class="sxs-lookup"><span data-stu-id="fc776-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="fc776-302">Ресурс со сжатием блоков</span><span class="sxs-lookup"><span data-stu-id="fc776-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc776-303">32</span><span class="sxs-lookup"><span data-stu-id="fc776-303">32</span></span>        | <span data-ttu-id="fc776-304">\_Формат DXGI \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="fc776-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="fc776-305">\_Формат DXGI \_ R32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="fc776-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="fc776-306">\_Формат DXGI \_ R9G9B9E5 \_ шаредексп</span><span class="sxs-lookup"><span data-stu-id="fc776-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="fc776-307">64</span><span class="sxs-lookup"><span data-stu-id="fc776-307">64</span></span>        | <span data-ttu-id="fc776-308">\_Формат DXGI \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="fc776-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="fc776-309">\_Формат DXGI \_ R16G16B16A16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="fc776-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="fc776-310">\_Формат DXGI \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="fc776-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="fc776-311">\_Формат DXGI \_ R32G32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="fc776-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="fc776-312">\_Формат DXGI \_ BC1 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="fc776-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="fc776-313">\_Формат DXGI \_ BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="fc776-314">\_Формат DXGI \_ BC4 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="fc776-315">128</span><span class="sxs-lookup"><span data-stu-id="fc776-315">128</span></span>       | <span data-ttu-id="fc776-316">\_Формат DXGI \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="fc776-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="fc776-317">\_Формат DXGI \_ R32G32B32A32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="fc776-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="fc776-318">\_Формат DXGI \_ BC2 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="fc776-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="fc776-319">\_Формат DXGI \_ BC3 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="fc776-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="fc776-320">\_Формат DXGI \_ Bc5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="fc776-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="fc776-321">\_Формат DXGI \_ Bc5 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="fc776-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fc776-322">См. также</span><span class="sxs-lookup"><span data-stu-id="fc776-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc776-323">Ресурсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fc776-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
