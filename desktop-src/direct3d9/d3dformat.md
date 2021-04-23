---
description: Определяет различные типы форматов поверхности.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821165"
---
# <a name="d3dformat"></a><span data-ttu-id="d7f02-103">D3DFORMAT</span><span class="sxs-lookup"><span data-stu-id="d7f02-103">D3DFORMAT</span></span>

<span data-ttu-id="d7f02-104">Определяет различные типы форматов поверхности.</span><span class="sxs-lookup"><span data-stu-id="d7f02-104">Defines the various types of surface formats.</span></span>

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a><span data-ttu-id="d7f02-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7f02-105">Remarks</span></span>

<span data-ttu-id="d7f02-106">Существует несколько типов форматов:</span><span class="sxs-lookup"><span data-stu-id="d7f02-106">There are several types of formats:</span></span>

-   [<span data-ttu-id="d7f02-107">Буферы или форматы вывода</span><span class="sxs-lookup"><span data-stu-id="d7f02-107">BackBuffer or Display Formats</span></span>](#backbuffer-or-display-formats)
-   [<span data-ttu-id="d7f02-108">Форматы буфера</span><span class="sxs-lookup"><span data-stu-id="d7f02-108">Buffer Formats</span></span>](#buffer-formats)
-   [<span data-ttu-id="d7f02-109">Форматы сжатых текстур Дкстн</span><span class="sxs-lookup"><span data-stu-id="d7f02-109">DXTn Compressed Texture Formats</span></span>](#dxtn-compressed-texture-formats)
-   [<span data-ttu-id="d7f02-110">Форматы чисел с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="d7f02-110">Floating-Point Formats</span></span>](#floating-point-formats)
-   [<span data-ttu-id="d7f02-111">Форматы FOURCC</span><span class="sxs-lookup"><span data-stu-id="d7f02-111">FOURCC Formats</span></span>](#fourcc-formats)
-   [<span data-ttu-id="d7f02-112">Форматы IEEE</span><span class="sxs-lookup"><span data-stu-id="d7f02-112">IEEE Formats</span></span>](#ieee-formats)
-   [<span data-ttu-id="d7f02-113">Смешанные форматы</span><span class="sxs-lookup"><span data-stu-id="d7f02-113">Mixed Formats</span></span>](#mixed-formats)
-   [<span data-ttu-id="d7f02-114">Форматы со знаком</span><span class="sxs-lookup"><span data-stu-id="d7f02-114">Signed Formats</span></span>](#signed-formats)
-   [<span data-ttu-id="d7f02-115">Неподписанные форматы</span><span class="sxs-lookup"><span data-stu-id="d7f02-115">Unsigned Formats</span></span>](#unsigned-formats)
-   [<span data-ttu-id="d7f02-116">Другое</span><span class="sxs-lookup"><span data-stu-id="d7f02-116">Other</span></span>](#other)

<span data-ttu-id="d7f02-117">Все форматы перечисляются слева направо, наиболее значащий бит и менее значащий бит.</span><span class="sxs-lookup"><span data-stu-id="d7f02-117">All formats are listed from left to right, most-significant bit to least-significant bit.</span></span> <span data-ttu-id="d7f02-118">Например, **D3DFORMAT \_ ARGB** упорядочивается от наиболее значимого битового канала A (альфа) до наименее значимого бита на канале B (синий).</span><span class="sxs-lookup"><span data-stu-id="d7f02-118">For example, **D3DFORMAT\_ARGB** is ordered from the most-significant bit channel A (alpha), to the least-significant bit channel B (blue).</span></span> <span data-ttu-id="d7f02-119">При просмотре данных в области данные хранятся в памяти с наименьшего значащих бит на наиболее значимый бит, что означает, что порядок каналов в памяти — от наименьшего (синего) бита к наиболее значимому биту (альфа).</span><span class="sxs-lookup"><span data-stu-id="d7f02-119">When traversing surface data, the data is stored in memory from least-significant bit to most-significant bit, which means that the channel order in memory is from least-significant bit (blue) to most-significant bit (alpha).</span></span>

<span data-ttu-id="d7f02-120">Значение по умолчанию для форматов, содержащих неопределенные каналы (G16R16, A8 и т. д.), равно 1.</span><span class="sxs-lookup"><span data-stu-id="d7f02-120">The default value for formats that contain undefined channels (G16R16, A8, and so on) is 1.</span></span> <span data-ttu-id="d7f02-121">Единственным исключением является формат A8, который инициализируется в 000 для трех цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-121">The only exception is the A8 format, which is initialized to 000 for the three color channels.</span></span>

<span data-ttu-id="d7f02-122">Первым является порядок битов от наиболее значимого байта, поэтому D3DFMT \_ A8L8 указывает, что старший байт этого 2-байтового формата имеет формат Alpha.</span><span class="sxs-lookup"><span data-stu-id="d7f02-122">The order of the bits is from the most significant byte first, so D3DFMT\_A8L8 indicates that the high byte of this 2-byte format is alpha.</span></span> <span data-ttu-id="d7f02-123">**D3DFMT \_ D16** указывает 16-разрядное целое значение и область, блокируемую приложением.</span><span class="sxs-lookup"><span data-stu-id="d7f02-123">**D3DFMT\_D16** indicates a 16-bit integer value and an application-lockable surface.</span></span>

<span data-ttu-id="d7f02-124">Форматы пикселей выбраны для включения выражения форматов расширений, определенных поставщиком оборудования, а также для включения правильно установленного метода FOURCC.</span><span class="sxs-lookup"><span data-stu-id="d7f02-124">Pixel formats have been chosen to enable the expression of hardware-vendor-defined extension formats, as well as to include the well-established FOURCC method.</span></span> <span data-ttu-id="d7f02-125">Набор форматов, распознаваемый средой выполнения Direct3D, определяется D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="d7f02-125">The set of formats understood by the Direct3D runtime is defined by D3DFORMAT.</span></span>

<span data-ttu-id="d7f02-126">Обратите внимание, что форматы, предоставляемые независимыми поставщиками оборудования (IHV) и многие коды FOURCC, отсутствуют в списке.</span><span class="sxs-lookup"><span data-stu-id="d7f02-126">Note that formats are supplied by independent hardware vendors (IHVs) and many FOURCC codes are not listed.</span></span> <span data-ttu-id="d7f02-127">Форматы в этом перечислении являются уникальными в том смысле, что они санкционированы средой выполнения, а это означает, что средство программной прорисовки будет обрабатывать все эти типы.</span><span class="sxs-lookup"><span data-stu-id="d7f02-127">The formats in this enumeration are unique in that they are sanctioned by the runtime, meaning that the reference rasterizer will operate on all these types.</span></span> <span data-ttu-id="d7f02-128">Форматы, предоставленные IHV, будут поддерживаться отдельными независимыми поставщиками оборудования по каждой карте.</span><span class="sxs-lookup"><span data-stu-id="d7f02-128">IHV-supplied formats will be supported by the individual IHVs on a card-by-card basis.</span></span>

### <a name="backbuffer-or-display-formats"></a><span data-ttu-id="d7f02-129">Буферы или форматы вывода</span><span class="sxs-lookup"><span data-stu-id="d7f02-129">BackBuffer or Display Formats</span></span>

<span data-ttu-id="d7f02-130">Эти форматы являются единственным допустимым форматом для заднего буфера или дисплея.</span><span class="sxs-lookup"><span data-stu-id="d7f02-130">These formats are the only valid formats for a back buffer or a display.</span></span>



| <span data-ttu-id="d7f02-131">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-131">Format</span></span>      | <span data-ttu-id="d7f02-132">Задний буфер</span><span class="sxs-lookup"><span data-stu-id="d7f02-132">Back buffer</span></span> | <span data-ttu-id="d7f02-133">Отображение</span><span class="sxs-lookup"><span data-stu-id="d7f02-133">Display</span></span>                   |
|-------------|-------------|---------------------------|
| <span data-ttu-id="d7f02-134">A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="d7f02-134">A2R10G10B10</span></span> | <span data-ttu-id="d7f02-135">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-135">x</span></span>           | <span data-ttu-id="d7f02-136">x (только полноэкранный режим)</span><span class="sxs-lookup"><span data-stu-id="d7f02-136">x (full-screen mode only)</span></span> |
| <span data-ttu-id="d7f02-137">A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="d7f02-137">A8R8G8B8</span></span>    | <span data-ttu-id="d7f02-138">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-138">x</span></span>           |                           |
| <span data-ttu-id="d7f02-139">X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="d7f02-139">X8R8G8B8</span></span>    | <span data-ttu-id="d7f02-140">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-140">x</span></span>           | <span data-ttu-id="d7f02-141">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-141">x</span></span>                         |
| <span data-ttu-id="d7f02-142">A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="d7f02-142">A1R5G5B5</span></span>    | <span data-ttu-id="d7f02-143">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-143">x</span></span>           |                           |
| <span data-ttu-id="d7f02-144">X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="d7f02-144">X1R5G5B5</span></span>    | <span data-ttu-id="d7f02-145">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-145">x</span></span>           | <span data-ttu-id="d7f02-146">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-146">x</span></span>                         |
| <span data-ttu-id="d7f02-147">R5G6B5</span><span class="sxs-lookup"><span data-stu-id="d7f02-147">R5G6B5</span></span>      | <span data-ttu-id="d7f02-148">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-148">x</span></span>           | <span data-ttu-id="d7f02-149">x</span><span class="sxs-lookup"><span data-stu-id="d7f02-149">x</span></span>                         |



 

### <a name="buffer-formats"></a><span data-ttu-id="d7f02-150">Форматы буфера</span><span class="sxs-lookup"><span data-stu-id="d7f02-150">Buffer Formats</span></span>

<span data-ttu-id="d7f02-151">Буферы глубины, трафаретов, вершин и индексов имеют уникальные форматы.</span><span class="sxs-lookup"><span data-stu-id="d7f02-151">Depth, stencil, vertex, and index buffers each have unique formats.</span></span>



| <span data-ttu-id="d7f02-152">Флаги буфера</span><span class="sxs-lookup"><span data-stu-id="d7f02-152">Buffer flags</span></span>               | <span data-ttu-id="d7f02-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-153">Value</span></span> | <span data-ttu-id="d7f02-154">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-154">Format</span></span>                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-155">**D3DFMT \_ D16 \_ блокируемый**</span><span class="sxs-lookup"><span data-stu-id="d7f02-155">**D3DFMT\_D16\_LOCKABLE**</span></span>  | <span data-ttu-id="d7f02-156">70</span><span class="sxs-lookup"><span data-stu-id="d7f02-156">70</span></span>    | <span data-ttu-id="d7f02-157">16-битная глубина бита z-буфера.</span><span class="sxs-lookup"><span data-stu-id="d7f02-157">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="d7f02-158">**D3DFMT \_ d32**</span><span class="sxs-lookup"><span data-stu-id="d7f02-158">**D3DFMT\_D32**</span></span>            | <span data-ttu-id="d7f02-159">71</span><span class="sxs-lookup"><span data-stu-id="d7f02-159">71</span></span>    | <span data-ttu-id="d7f02-160">32 — битовая глубина z-буфера.</span><span class="sxs-lookup"><span data-stu-id="d7f02-160">32-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="d7f02-161">**D3DFMT \_ D15S1**</span><span class="sxs-lookup"><span data-stu-id="d7f02-161">**D3DFMT\_D15S1**</span></span>          | <span data-ttu-id="d7f02-162">73</span><span class="sxs-lookup"><span data-stu-id="d7f02-162">73</span></span>    | <span data-ttu-id="d7f02-163">16-битная глубина бит z-буфера, где 15 бит зарезервированы для канала глубины, а 1 бит зарезервирован для канала набора элементов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-163">16-bit z-buffer bit depth where 15 bits are reserved for the depth channel and 1 bit is reserved for the stencil channel.</span></span>                     |
| <span data-ttu-id="d7f02-164">**D3DFMT \_ D24S8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-164">**D3DFMT\_D24S8**</span></span>          | <span data-ttu-id="d7f02-165">75</span><span class="sxs-lookup"><span data-stu-id="d7f02-165">75</span></span>    | <span data-ttu-id="d7f02-166">32-битовая глубина z-буфера, использующая 24 бита для канала глубины и 8 бит для канала набора элементов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-166">32-bit z-buffer bit depth using 24 bits for the depth channel and 8 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="d7f02-167">**D3DFMT \_ D24X8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-167">**D3DFMT\_D24X8**</span></span>          | <span data-ttu-id="d7f02-168">77</span><span class="sxs-lookup"><span data-stu-id="d7f02-168">77</span></span>    | <span data-ttu-id="d7f02-169">32-битовая глубина z-буфера с использованием 24 бит для канала глубины.</span><span class="sxs-lookup"><span data-stu-id="d7f02-169">32-bit z-buffer bit depth using 24 bits for the depth channel.</span></span>                                                                                |
| <span data-ttu-id="d7f02-170">**D3DFMT \_ D24X4S4**</span><span class="sxs-lookup"><span data-stu-id="d7f02-170">**D3DFMT\_D24X4S4**</span></span>        | <span data-ttu-id="d7f02-171">79</span><span class="sxs-lookup"><span data-stu-id="d7f02-171">79</span></span>    | <span data-ttu-id="d7f02-172">32-битовая глубина z-буфера, использующая 24 бита для канала глубины и 4 бита для канала набора элементов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-172">32-bit z-buffer bit depth using 24 bits for the depth channel and 4 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="d7f02-173">**D3DFMT \_ D32F \_ блокируемый**</span><span class="sxs-lookup"><span data-stu-id="d7f02-173">**D3DFMT\_D32F\_LOCKABLE**</span></span> | <span data-ttu-id="d7f02-174">82</span><span class="sxs-lookup"><span data-stu-id="d7f02-174">82</span></span>    | <span data-ttu-id="d7f02-175">Блокируемый формат, в котором значение глубины представлено в виде стандартного числа с плавающей запятой IEEE.</span><span class="sxs-lookup"><span data-stu-id="d7f02-175">A lockable format where the depth value is represented as a standard IEEE floating-point number.</span></span>                                              |
| <span data-ttu-id="d7f02-176">**D3DFMT \_ D24FS8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-176">**D3DFMT\_D24FS8**</span></span>         | <span data-ttu-id="d7f02-177">83</span><span class="sxs-lookup"><span data-stu-id="d7f02-177">83</span></span>    | <span data-ttu-id="d7f02-178">Неблокируемый формат, который содержит 24 бита глубины (в 24-разрядном формате с плавающей запятой-20E4) и 8 битов набора элементов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-178">A non-lockable format that contains 24 bits of depth (in a 24-bit floating point format - 20e4) and 8 bits of stencil.</span></span>                        |
| <span data-ttu-id="d7f02-179">**D3DFMT \_ d32 \_ блокируемый**</span><span class="sxs-lookup"><span data-stu-id="d7f02-179">**D3DFMT\_D32\_LOCKABLE**</span></span>  | <span data-ttu-id="d7f02-180">84</span><span class="sxs-lookup"><span data-stu-id="d7f02-180">84</span></span>    | <span data-ttu-id="d7f02-181">Блокируемый буфер глубины 32 бит.</span><span class="sxs-lookup"><span data-stu-id="d7f02-181">A lockable 32-bit depth buffer.</span></span> <span data-ttu-id="d7f02-182">**Различия между Direct3D 9 и Direct3D 9Ex:** Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d7f02-182">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>  |
| <span data-ttu-id="d7f02-183">**D3DFMT \_ S8 \_ блокируемый**</span><span class="sxs-lookup"><span data-stu-id="d7f02-183">**D3DFMT\_S8\_LOCKABLE**</span></span>   | <span data-ttu-id="d7f02-184">85</span><span class="sxs-lookup"><span data-stu-id="d7f02-184">85</span></span>    | <span data-ttu-id="d7f02-185">Блокируемый 8-битный буфер трафаретов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-185">A lockable 8-bit stencil buffer.</span></span> <span data-ttu-id="d7f02-186">**Различия между Direct3D 9 и Direct3D 9Ex:** Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d7f02-186">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |
| <span data-ttu-id="d7f02-187">**D3DFMT \_ D16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-187">**D3DFMT\_D16**</span></span>            | <span data-ttu-id="d7f02-188">80</span><span class="sxs-lookup"><span data-stu-id="d7f02-188">80</span></span>    | <span data-ttu-id="d7f02-189">16-битная глубина бита z-буфера.</span><span class="sxs-lookup"><span data-stu-id="d7f02-189">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="d7f02-190">**D3DFMT \_ вертексдата**</span><span class="sxs-lookup"><span data-stu-id="d7f02-190">**D3DFMT\_VERTEXDATA**</span></span>     | <span data-ttu-id="d7f02-191">100</span><span class="sxs-lookup"><span data-stu-id="d7f02-191">100</span></span>   | <span data-ttu-id="d7f02-192">Описывает поверхность буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="d7f02-192">Describes a vertex buffer surface.</span></span>                                                                                                            |
| <span data-ttu-id="d7f02-193">**D3DFMT \_ INDEX16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-193">**D3DFMT\_INDEX16**</span></span>        | <span data-ttu-id="d7f02-194">101</span><span class="sxs-lookup"><span data-stu-id="d7f02-194">101</span></span>   | <span data-ttu-id="d7f02-195">Битовая глубина 16-разрядного буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="d7f02-195">16-bit index buffer bit depth.</span></span>                                                                                                                |
| <span data-ttu-id="d7f02-196">**D3DFMT \_ INDEX32**</span><span class="sxs-lookup"><span data-stu-id="d7f02-196">**D3DFMT\_INDEX32**</span></span>        | <span data-ttu-id="d7f02-197">102</span><span class="sxs-lookup"><span data-stu-id="d7f02-197">102</span></span>   | <span data-ttu-id="d7f02-198">32-битовая глубина битового буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="d7f02-198">32-bit index buffer bit depth.</span></span>                                                                                                                |



 

<span data-ttu-id="d7f02-199">Все форматы элементов глубины, за исключением D3DFMT \_ D16 \_ блокируемых, обозначают отсутствие определенного числа битов на пиксель, и драйверу разрешено использовать больше указанного количества бит по глубине (но не по каналу шаблона).</span><span class="sxs-lookup"><span data-stu-id="d7f02-199">All depth-stencil formats except D3DFMT\_D16\_LOCKABLE indicate no particular bit ordering per pixel, and the driver is allowed to consume more than the indicated number of bits-per-depth channel (but not stencil channel).</span></span>

### <a name="dxtn-compressed-texture-formats"></a><span data-ttu-id="d7f02-200">Форматы сжатых текстур Дкстн</span><span class="sxs-lookup"><span data-stu-id="d7f02-200">DXTn Compressed Texture Formats</span></span>

<span data-ttu-id="d7f02-201">Эти флаги используются для сжатых текстур:</span><span class="sxs-lookup"><span data-stu-id="d7f02-201">These flags are used for compressed textures:</span></span>



| <span data-ttu-id="d7f02-202">Флаги сжатой текстуры Дкстн</span><span class="sxs-lookup"><span data-stu-id="d7f02-202">DXTn Compressed Texture flags</span></span> | <span data-ttu-id="d7f02-203">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-203">Value</span></span>                          | <span data-ttu-id="d7f02-204">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-204">Format</span></span>                          |
|-------------------------------|--------------------------------|---------------------------------|
| <span data-ttu-id="d7f02-205">**D3DFMT \_ DXT1**</span><span class="sxs-lookup"><span data-stu-id="d7f02-205">**D3DFMT\_DXT1**</span></span>              | <span data-ttu-id="d7f02-206">МАКЕФАУРКК (D "," X "," T "," 1 ")</span><span class="sxs-lookup"><span data-stu-id="d7f02-206">MAKEFOURCC('D', 'X', 'T', '1')</span></span> | <span data-ttu-id="d7f02-207">Формат текстуры сжатия DXT1</span><span class="sxs-lookup"><span data-stu-id="d7f02-207">DXT1 compression texture format</span></span> |
| <span data-ttu-id="d7f02-208">**D3DFMT \_ DXT2**</span><span class="sxs-lookup"><span data-stu-id="d7f02-208">**D3DFMT\_DXT2**</span></span>              | <span data-ttu-id="d7f02-209">МАКЕФАУРКК (D "," X "," T "," 2 ")</span><span class="sxs-lookup"><span data-stu-id="d7f02-209">MAKEFOURCC('D', 'X', 'T', '2')</span></span> | <span data-ttu-id="d7f02-210">Формат текстуры сжатия DXT2</span><span class="sxs-lookup"><span data-stu-id="d7f02-210">DXT2 compression texture format</span></span> |
| <span data-ttu-id="d7f02-211">**D3DFMT \_ DXT3**</span><span class="sxs-lookup"><span data-stu-id="d7f02-211">**D3DFMT\_DXT3**</span></span>              | <span data-ttu-id="d7f02-212">МАКЕФАУРКК ('D ', ' X ', ', ', ' 3 ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-212">MAKEFOURCC('D', 'X', 'T', '3')</span></span> | <span data-ttu-id="d7f02-213">Формат текстуры сжатия DXT3</span><span class="sxs-lookup"><span data-stu-id="d7f02-213">DXT3 compression texture format</span></span> |
| <span data-ttu-id="d7f02-214">**D3DFMT \_ DXT4**</span><span class="sxs-lookup"><span data-stu-id="d7f02-214">**D3DFMT\_DXT4**</span></span>              | <span data-ttu-id="d7f02-215">МАКЕФАУРКК (D "," X "," T "," 4 ")</span><span class="sxs-lookup"><span data-stu-id="d7f02-215">MAKEFOURCC('D', 'X', 'T', '4')</span></span> | <span data-ttu-id="d7f02-216">Формат текстуры сжатия DXT4</span><span class="sxs-lookup"><span data-stu-id="d7f02-216">DXT4 compression texture format</span></span> |
| <span data-ttu-id="d7f02-217">**D3DFMT \_ DXT5**</span><span class="sxs-lookup"><span data-stu-id="d7f02-217">**D3DFMT\_DXT5**</span></span>              | <span data-ttu-id="d7f02-218">МАКЕФАУРКК (D "," X ", 'T", "5")</span><span class="sxs-lookup"><span data-stu-id="d7f02-218">MAKEFOURCC('D', 'X', 'T', '5')</span></span> | <span data-ttu-id="d7f02-219">Формат текстуры сжатия DXT5</span><span class="sxs-lookup"><span data-stu-id="d7f02-219">DXT5 compression texture format</span></span> |



 

<span data-ttu-id="d7f02-220">Среда выполнения не позволит приложению создать поверхность с помощью формата Дкстн, если размеры поверхности не кратны 4.</span><span class="sxs-lookup"><span data-stu-id="d7f02-220">The runtime will not allow an application to create a surface using a DXTn format unless the surface dimensions are multiples of 4.</span></span> <span data-ttu-id="d7f02-221">Это относится к поверхностям, объектам рендеринга, 2D-текстурам, текстурам кубов и текстурам томов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-221">This applies to offscreen-plain surfaces, render targets, 2D textures, cube textures, and volume textures.</span></span>

### <a name="floating-point-formats"></a><span data-ttu-id="d7f02-222">Форматы Floating-Point</span><span class="sxs-lookup"><span data-stu-id="d7f02-222">Floating-Point Formats</span></span>

<span data-ttu-id="d7f02-223">Эти флаги используются для форматов поверхности с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d7f02-223">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="d7f02-224">Эти 16-битные форматы для каждого канала также называются форматами s10e5.</span><span class="sxs-lookup"><span data-stu-id="d7f02-224">These 16-bits-per-channel formats are also known as s10e5 formats.</span></span>



| <span data-ttu-id="d7f02-225">Флаги с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="d7f02-225">Floating-point flags</span></span>      | <span data-ttu-id="d7f02-226">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-226">Value</span></span> | <span data-ttu-id="d7f02-227">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-227">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-228">**D3DFMT \_ R16F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-228">**D3DFMT\_R16F**</span></span>          | <span data-ttu-id="d7f02-229">111</span><span class="sxs-lookup"><span data-stu-id="d7f02-229">111</span></span>   | <span data-ttu-id="d7f02-230">16-разрядный формат с плавающей запятой, использующий 16 бит для красного канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-230">16-bit float format using 16 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="d7f02-231">**D3DFMT \_ G16R16F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-231">**D3DFMT\_G16R16F**</span></span>       | <span data-ttu-id="d7f02-232">112</span><span class="sxs-lookup"><span data-stu-id="d7f02-232">112</span></span>   | <span data-ttu-id="d7f02-233">32-разрядный формат с плавающей запятой, использующий 16 бит для красного канала и 16 бит для зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-233">32-bit float format using 16 bits for the red channel and 16 bits for the green channel.</span></span> |
| <span data-ttu-id="d7f02-234">**D3DFMT \_ A16B16G16R16F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-234">**D3DFMT\_A16B16G16R16F**</span></span> | <span data-ttu-id="d7f02-235">113</span><span class="sxs-lookup"><span data-stu-id="d7f02-235">113</span></span>   | <span data-ttu-id="d7f02-236">64-разрядный формат с плавающей запятой, использующий 16 бит для каждого канала (альфа-канал, синий, зеленый, красный).</span><span class="sxs-lookup"><span data-stu-id="d7f02-236">64-bit float format using 16 bits for the each channel (alpha, blue, green, red).</span></span>        |



 

### <a name="fourcc-formats"></a><span data-ttu-id="d7f02-237">Форматы FOURCC</span><span class="sxs-lookup"><span data-stu-id="d7f02-237">FOURCC Formats</span></span>

<span data-ttu-id="d7f02-238">Данные в формате FOURCC — это сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="d7f02-238">Data in a FOURCC format is compressed data.</span></span>

### <a name="makefourcc"></a><span data-ttu-id="d7f02-239">макефауркк</span><span class="sxs-lookup"><span data-stu-id="d7f02-239">MAKEFOURCC</span></span>

<span data-ttu-id="d7f02-240">Макрос для создания четырех кодов символов выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7f02-240">A macro for generating four-character codes follows:</span></span>

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

<span data-ttu-id="d7f02-241">Ниже приведены определенные форматы FOURCC:</span><span class="sxs-lookup"><span data-stu-id="d7f02-241">Here are the defined FOURCC formats:</span></span>



| <span data-ttu-id="d7f02-242">Флаги FOURCC</span><span class="sxs-lookup"><span data-stu-id="d7f02-242">FOURCC flags</span></span>              | <span data-ttu-id="d7f02-243">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-243">Value</span></span>                          | <span data-ttu-id="d7f02-244">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-244">Format</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-245">**D3DFMT \_ MULTI2 \_ ARGB8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-245">**D3DFMT\_MULTI2\_ARGB8**</span></span> | <span data-ttu-id="d7f02-246">МАКЕФАУРКК (M ', ' E ', 'T ', ' 1 ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-246">MAKEFOURCC('M','E','T','1')</span></span>    | <span data-ttu-id="d7f02-247">Многоэлементная текстура (не сжатая)</span><span class="sxs-lookup"><span data-stu-id="d7f02-247">MultiElement texture (not compressed)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d7f02-248">**D3DFMT \_ G8R8 \_ G8B8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-248">**D3DFMT\_G8R8\_G8B8**</span></span>    | <span data-ttu-id="d7f02-249">МАКЕФАУРКК (' G ', ' R ', ' G ', ' B ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-249">MAKEFOURCC('G', 'R', 'G', 'B')</span></span> | <span data-ttu-id="d7f02-250">16-битный упакованный формат RGB, аналогичный YUY2 (Y0U0, Y1V0, Y2U2 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d7f02-250">A 16-bit packed RGB format analogous to YUY2 (Y0U0, Y1V0, Y2U2, and so on).</span></span> <span data-ttu-id="d7f02-251">Для правильного представления значения цвета требуется пара пикселей.</span><span class="sxs-lookup"><span data-stu-id="d7f02-251">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="d7f02-252">Первый пиксел в паре содержит 8 битов зеленого цвета (в 8 бит) и 8 битов красного цвета (в младших 8 битах).</span><span class="sxs-lookup"><span data-stu-id="d7f02-252">The first pixel in the pair contains 8 bits of green (in the high 8 bits) and 8 bits of red (in the low 8 bits).</span></span> <span data-ttu-id="d7f02-253">Второй пиксель содержит 8 битов зеленого цвета (в 8 бит) и 8 бит синего (в младших 8 битах).</span><span class="sxs-lookup"><span data-stu-id="d7f02-253">The second pixel contains 8 bits of green (in the high 8 bits) and 8 bits of blue (in the low 8 bits).</span></span> <span data-ttu-id="d7f02-254">Вместе два пиксела используют красный и синий компоненты, а каждый имеет уникальный зеленый компонент (G0R0, G1B0, G2R2 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d7f02-254">Together, the two pixels share the red and blue components, while each has a unique green component (G0R0, G1B0, G2R2, and so on).</span></span> <span data-ttu-id="d7f02-255">Образец текстуры не нормализует цвета при поиске в шейдере пикселей. они остаются в диапазоне от 0,0 f до 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="d7f02-255">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="d7f02-256">Это справедливо для всех программируемых моделей шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="d7f02-256">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="d7f02-257">Для шейдера пикселей с фиксированной функцией оборудование должно быть нормализовано до диапазона от 0. f до 1. f и по сути обрабатывалось как текстура YUY2.</span><span class="sxs-lookup"><span data-stu-id="d7f02-257">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="d7f02-258">Оборудование, предоставляющее этот формат, должно иметь член PixelShader1xMaxValue [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , для которого задано значение, способное обрабатывать этот диапазон.</span><span class="sxs-lookup"><span data-stu-id="d7f02-258">Hardware that exposes this format must have the PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span> |
| <span data-ttu-id="d7f02-259">**D3DFMT \_ R8G8 \_ B8G8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-259">**D3DFMT\_R8G8\_B8G8**</span></span>    | <span data-ttu-id="d7f02-260">МАКЕФАУРКК (' R ', ' G ', ' B ', ' G ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-260">MAKEFOURCC('R', 'G', 'B', 'G')</span></span> | <span data-ttu-id="d7f02-261">16-битный упакованный формат RGB, аналогичный UYVY (U0Y0, V0Y1, U2Y2 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d7f02-261">A 16-bit packed RGB format analogous to UYVY (U0Y0, V0Y1, U2Y2, and so on).</span></span> <span data-ttu-id="d7f02-262">Для правильного представления значения цвета требуется пара пикселей.</span><span class="sxs-lookup"><span data-stu-id="d7f02-262">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="d7f02-263">Первый пиксел в паре содержит 8 битов зеленого цвета (в младших 8 битах) и 8 битов красного цвета (в 8 бит).</span><span class="sxs-lookup"><span data-stu-id="d7f02-263">The first pixel in the pair contains 8 bits of green (in the low 8 bits) and 8 bits of red (in the high 8 bits).</span></span> <span data-ttu-id="d7f02-264">Второй пиксель содержит 8 битов зеленого цвета (в младших 8 битах) и 8 бит синего (в 8 бит).</span><span class="sxs-lookup"><span data-stu-id="d7f02-264">The second pixel contains 8 bits of green (in the low 8 bits) and 8 bits of blue (in the high 8 bits).</span></span> <span data-ttu-id="d7f02-265">Вместе два пиксела используют красный и синий компоненты, а каждый имеет уникальный зеленый компонент (R0G0, B0G1, R2G2 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d7f02-265">Together, the two pixels share the red and blue components, while each has a unique green component (R0G0, B0G1, R2G2, and so on).</span></span> <span data-ttu-id="d7f02-266">Образец текстуры не нормализует цвета при поиске в шейдере пикселей. они остаются в диапазоне от 0,0 f до 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="d7f02-266">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="d7f02-267">Это справедливо для всех программируемых моделей шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="d7f02-267">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="d7f02-268">Для шейдера пикселей с фиксированной функцией оборудование должно быть нормализовано до диапазона от 0. f до 1. f и по сути обрабатывалось как текстура YUY2.</span><span class="sxs-lookup"><span data-stu-id="d7f02-268">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="d7f02-269">Оборудование, предоставляющее этот формат, должно иметь PixelShader1xMaxValue член [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , для которого задано значение, способное обрабатывать этот диапазон.</span><span class="sxs-lookup"><span data-stu-id="d7f02-269">Hardware that exposes this format must have PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span>     |
| <span data-ttu-id="d7f02-270">**D3DFMT \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="d7f02-270">**D3DFMT\_UYVY**</span></span>          | <span data-ttu-id="d7f02-271">МАКЕФАУРКК (' U ', ' Y ', ' V ', ' Y ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-271">MAKEFOURCC('U', 'Y', 'V', 'Y')</span></span> | <span data-ttu-id="d7f02-272">Формат UYVY (соответствие PC98)</span><span class="sxs-lookup"><span data-stu-id="d7f02-272">UYVY format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d7f02-273">**D3DFMT \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="d7f02-273">**D3DFMT\_YUY2**</span></span>          | <span data-ttu-id="d7f02-274">МАКЕФАУРКК (' Y ', ' U ', ' Y ', ' 2 ')</span><span class="sxs-lookup"><span data-stu-id="d7f02-274">MAKEFOURCC('Y', 'U', 'Y', '2')</span></span> | <span data-ttu-id="d7f02-275">Формат YUY2 (соответствие PC98)</span><span class="sxs-lookup"><span data-stu-id="d7f02-275">YUY2 format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a><span data-ttu-id="d7f02-276">Форматы IEEE</span><span class="sxs-lookup"><span data-stu-id="d7f02-276">IEEE Formats</span></span>

<span data-ttu-id="d7f02-277">Эти флаги используются для форматов поверхности с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d7f02-277">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="d7f02-278">Эти форматы 32-бит на канал также называются форматами s23e8.</span><span class="sxs-lookup"><span data-stu-id="d7f02-278">These 32-bits-per-channel formats are also known as s23e8 formats.</span></span>



| <span data-ttu-id="d7f02-279">Флаги с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="d7f02-279">Floating-point flags</span></span>      | <span data-ttu-id="d7f02-280">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-280">Value</span></span> | <span data-ttu-id="d7f02-281">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-281">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-282">**D3DFMT \_ R32F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-282">**D3DFMT\_R32F**</span></span>          | <span data-ttu-id="d7f02-283">114</span><span class="sxs-lookup"><span data-stu-id="d7f02-283">114</span></span>   | <span data-ttu-id="d7f02-284">32-разрядный формат с плавающей запятой с использованием 32 бит для красного канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-284">32-bit float format using 32 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="d7f02-285">**D3DFMT \_ G32R32F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-285">**D3DFMT\_G32R32F**</span></span>       | <span data-ttu-id="d7f02-286">115</span><span class="sxs-lookup"><span data-stu-id="d7f02-286">115</span></span>   | <span data-ttu-id="d7f02-287">64-разрядный формат с плавающей запятой, использующий 32 бит для красного канала и 32 бит для зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-287">64-bit float format using 32 bits for the red channel and 32 bits for the green channel.</span></span> |
| <span data-ttu-id="d7f02-288">**D3DFMT \_ A32B32G32R32F**</span><span class="sxs-lookup"><span data-stu-id="d7f02-288">**D3DFMT\_A32B32G32R32F**</span></span> | <span data-ttu-id="d7f02-289">116</span><span class="sxs-lookup"><span data-stu-id="d7f02-289">116</span></span>   | <span data-ttu-id="d7f02-290">128-разрядный формат с плавающей запятой, использующий 32 бит для каждого канала (альфа-канал, синий, зеленый, красный).</span><span class="sxs-lookup"><span data-stu-id="d7f02-290">128-bit float format using 32 bits for the each channel (alpha, blue, green, red).</span></span>       |



 

### <a name="mixed-formats"></a><span data-ttu-id="d7f02-291">Смешанные форматы</span><span class="sxs-lookup"><span data-stu-id="d7f02-291">Mixed Formats</span></span>

<span data-ttu-id="d7f02-292">Данные в смешанных форматах могут содержать сочетание неподписанных данных и подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="d7f02-292">Data in mixed formats can contain a combination of unsigned data and signed data.</span></span>



| <span data-ttu-id="d7f02-293">Флаги смешанного формата</span><span class="sxs-lookup"><span data-stu-id="d7f02-293">Mixed format flags</span></span>      | <span data-ttu-id="d7f02-294">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-294">Value</span></span> | <span data-ttu-id="d7f02-295">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-295">Format</span></span>                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-296">**D3DFMT \_ L6V5U5**</span><span class="sxs-lookup"><span data-stu-id="d7f02-296">**D3DFMT\_L6V5U5**</span></span>      | <span data-ttu-id="d7f02-297">61</span><span class="sxs-lookup"><span data-stu-id="d7f02-297">61</span></span>    | <span data-ttu-id="d7f02-298">16-разрядный формат схемы выпуклости с яркостью, использующий 6 бит для светимости, и 5 бит для v и вы.</span><span class="sxs-lookup"><span data-stu-id="d7f02-298">16-bit bump-map format with luminance using 6 bits for luminance, and 5 bits each for v and u.</span></span> |
| <span data-ttu-id="d7f02-299">**D3DFMT \_ X8L8V8U8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-299">**D3DFMT\_X8L8V8U8**</span></span>    | <span data-ttu-id="d7f02-300">62</span><span class="sxs-lookup"><span data-stu-id="d7f02-300">62</span></span>    | <span data-ttu-id="d7f02-301">32-битовый формат схемы выпуклости с яркостью, использующей 8 бит для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-301">32-bit bump-map format with luminance using 8 bits for each channel.</span></span>                           |
| <span data-ttu-id="d7f02-302">**D3DFMT \_ A2W10V10U10**</span><span class="sxs-lookup"><span data-stu-id="d7f02-302">**D3DFMT\_A2W10V10U10**</span></span> | <span data-ttu-id="d7f02-303">67</span><span class="sxs-lookup"><span data-stu-id="d7f02-303">67</span></span>    | <span data-ttu-id="d7f02-304">32-разрядный формат схемы выпуклости, использующий 2 бита для альфа и 10 бит для каждого из них для w, v и.</span><span class="sxs-lookup"><span data-stu-id="d7f02-304">32-bit bump-map format using 2 bits for alpha and 10 bits each for w, v, and u.</span></span>                |



 

### <a name="signed-formats"></a><span data-ttu-id="d7f02-305">Форматы со знаком</span><span class="sxs-lookup"><span data-stu-id="d7f02-305">Signed Formats</span></span>

<span data-ttu-id="d7f02-306">Данные в подписанном формате могут быть как положительными, так и отрицательными.</span><span class="sxs-lookup"><span data-stu-id="d7f02-306">Data in a signed format can be both positive and negative.</span></span> <span data-ttu-id="d7f02-307">Форматы со знаком используют сочетания (U), (V), (W) и (Q) данных.</span><span class="sxs-lookup"><span data-stu-id="d7f02-307">Signed formats use combinations of (U), (V), (W), and (Q) data.</span></span>



| <span data-ttu-id="d7f02-308">Флаги формата со знаком</span><span class="sxs-lookup"><span data-stu-id="d7f02-308">Signed format flags</span></span>      | <span data-ttu-id="d7f02-309">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-309">Value</span></span> | <span data-ttu-id="d7f02-310">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-310">Format</span></span>                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-311">**D3DFMT \_ V8U8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-311">**D3DFMT\_V8U8**</span></span>         | <span data-ttu-id="d7f02-312">60</span><span class="sxs-lookup"><span data-stu-id="d7f02-312">60</span></span>    | <span data-ttu-id="d7f02-313">16-разрядный формат схемы выпуклости с использованием 8 бит для каждого из них и данных v.</span><span class="sxs-lookup"><span data-stu-id="d7f02-313">16-bit bump-map format using 8 bits each for u and v data.</span></span>                                                |
| <span data-ttu-id="d7f02-314">**D3DFMT \_ Q8W8V8U8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-314">**D3DFMT\_Q8W8V8U8**</span></span>     | <span data-ttu-id="d7f02-315">63</span><span class="sxs-lookup"><span data-stu-id="d7f02-315">63</span></span>    | <span data-ttu-id="d7f02-316">32-разрядный формат схемы выпуклости, использующий 8 бит для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-316">32-bit bump-map format using 8 bits for each channel.</span></span>                                                     |
| <span data-ttu-id="d7f02-317">**D3DFMT \_ V16U16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-317">**D3DFMT\_V16U16**</span></span>       | <span data-ttu-id="d7f02-318">64</span><span class="sxs-lookup"><span data-stu-id="d7f02-318">64</span></span>    | <span data-ttu-id="d7f02-319">32-разрядный формат схемы выпуклости, использующий 16 бит для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-319">32-bit bump-map format using 16 bits for each channel.</span></span>                                                    |
| <span data-ttu-id="d7f02-320">**D3DFMT \_ Q16W16V16U16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-320">**D3DFMT\_Q16W16V16U16**</span></span> | <span data-ttu-id="d7f02-321">110</span><span class="sxs-lookup"><span data-stu-id="d7f02-321">110</span></span>   | <span data-ttu-id="d7f02-322">64-разрядный формат схемы выпуклости, использующий 16 бит для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d7f02-322">64-bit bump-map format using 16 bits for each component.</span></span>                                                  |
| <span data-ttu-id="d7f02-323">**D3DFMT \_ CxV8U8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-323">**D3DFMT\_CxV8U8**</span></span>       | <span data-ttu-id="d7f02-324">117</span><span class="sxs-lookup"><span data-stu-id="d7f02-324">117</span></span>   | <span data-ttu-id="d7f02-325">16-разрядный формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="d7f02-325">16-bit normal compression format.</span></span> <span data-ttu-id="d7f02-326">Образец текстуры рассчитывает канал C: C = sqrt (1-U ²-V ²).</span><span class="sxs-lookup"><span data-stu-id="d7f02-326">The texture sampler computes the C channel from: C = sqrt(1 - U² - V²).</span></span> |



 

### <a name="unsigned-formats"></a><span data-ttu-id="d7f02-327">Неподписанные форматы</span><span class="sxs-lookup"><span data-stu-id="d7f02-327">Unsigned Formats</span></span>

<span data-ttu-id="d7f02-328">Данные в формате без знака должны быть положительными.</span><span class="sxs-lookup"><span data-stu-id="d7f02-328">Data in an unsigned format must be positive.</span></span> <span data-ttu-id="d7f02-329">Неподписанные форматы используют сочетания (R) ED, (G) Рин, (B) Лю, (A) ЛФА, (L) уминанце и (P) алетте данных.</span><span class="sxs-lookup"><span data-stu-id="d7f02-329">Unsigned formats use combinations of (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance, and (P)alette data.</span></span> <span data-ttu-id="d7f02-330">Данные палитры также называются индексируемыми цветом данными, так как данные используются для индексации цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="d7f02-330">Palette data is also referred to as color indexed data because the data is used to index a color palette.</span></span>



| <span data-ttu-id="d7f02-331">Флаги неподписанного формата</span><span class="sxs-lookup"><span data-stu-id="d7f02-331">Unsigned format flags</span></span>             | <span data-ttu-id="d7f02-332">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-332">Value</span></span> | <span data-ttu-id="d7f02-333">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-333">Format</span></span>                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-334">**D3DFMT \_ R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-334">**D3DFMT\_R8G8B8**</span></span>                | <span data-ttu-id="d7f02-335">20</span><span class="sxs-lookup"><span data-stu-id="d7f02-335">20</span></span>    | <span data-ttu-id="d7f02-336">24-битный формат пикселей RGB с 8 битами на канал.</span><span class="sxs-lookup"><span data-stu-id="d7f02-336">24-bit RGB pixel format with 8 bits per channel.</span></span>                                                                                                                          |
| <span data-ttu-id="d7f02-337">**D3DFMT \_ A8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-337">**D3DFMT\_A8R8G8B8**</span></span>              | <span data-ttu-id="d7f02-338">21</span><span class="sxs-lookup"><span data-stu-id="d7f02-338">21</span></span>    | <span data-ttu-id="d7f02-339">32-разрядный формат пикселей ARGB в Alpha с использованием 8 бит на канал.</span><span class="sxs-lookup"><span data-stu-id="d7f02-339">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="d7f02-340">**D3DFMT \_ X8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-340">**D3DFMT\_X8R8G8B8**</span></span>              | <span data-ttu-id="d7f02-341">22</span><span class="sxs-lookup"><span data-stu-id="d7f02-341">22</span></span>    | <span data-ttu-id="d7f02-342">32-разрядный формат пикселей RGB, где 8 бит зарезервированы для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="d7f02-342">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="d7f02-343">**D3DFMT \_ R5G6B5**</span><span class="sxs-lookup"><span data-stu-id="d7f02-343">**D3DFMT\_R5G6B5**</span></span>                | <span data-ttu-id="d7f02-344">23</span><span class="sxs-lookup"><span data-stu-id="d7f02-344">23</span></span>    | <span data-ttu-id="d7f02-345">16-битный формат пикселей RGB с 5 битами на красный, 6 бит для зеленого и 5 бит для синего.</span><span class="sxs-lookup"><span data-stu-id="d7f02-345">16-bit RGB pixel format with 5 bits for red, 6 bits for green, and 5 bits for blue.</span></span>                                                                                       |
| <span data-ttu-id="d7f02-346">**D3DFMT \_ X1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="d7f02-346">**D3DFMT\_X1R5G5B5**</span></span>              | <span data-ttu-id="d7f02-347">24</span><span class="sxs-lookup"><span data-stu-id="d7f02-347">24</span></span>    | <span data-ttu-id="d7f02-348">16-разрядный формат пикселей, где 5 бит зарезервированы для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="d7f02-348">16-bit pixel format where 5 bits are reserved for each color.</span></span>                                                                                                             |
| <span data-ttu-id="d7f02-349">**D3DFMT \_ A1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="d7f02-349">**D3DFMT\_A1R5G5B5**</span></span>              | <span data-ttu-id="d7f02-350">25</span><span class="sxs-lookup"><span data-stu-id="d7f02-350">25</span></span>    | <span data-ttu-id="d7f02-351">16-разрядный формат пикселей, где 5 бит зарезервированы для каждого цвета, а 1 бит зарезервирован для альфа.</span><span class="sxs-lookup"><span data-stu-id="d7f02-351">16-bit pixel format where 5 bits are reserved for each color and 1 bit is reserved for alpha.</span></span>                                                                             |
| <span data-ttu-id="d7f02-352">**D3DFMT \_ A4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="d7f02-352">**D3DFMT\_A4R4G4B4**</span></span>              | <span data-ttu-id="d7f02-353">26</span><span class="sxs-lookup"><span data-stu-id="d7f02-353">26</span></span>    | <span data-ttu-id="d7f02-354">16-разрядный формат пикселей ARGB с 4 битами для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-354">16-bit ARGB pixel format with 4 bits for each channel.</span></span>                                                                                                                    |
| <span data-ttu-id="d7f02-355">**D3DFMT \_ R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="d7f02-355">**D3DFMT\_R3G3B2**</span></span>                | <span data-ttu-id="d7f02-356">27</span><span class="sxs-lookup"><span data-stu-id="d7f02-356">27</span></span>    | <span data-ttu-id="d7f02-357">8-разрядный формат текстуры RGB, использующий 3 бита для красного, 3 бит для зеленого и 2 бит для синего.</span><span class="sxs-lookup"><span data-stu-id="d7f02-357">8-bit RGB texture format using 3 bits for red, 3 bits for green, and 2 bits for blue.</span></span>                                                                                     |
| <span data-ttu-id="d7f02-358">**D3DFMT \_ A8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-358">**D3DFMT\_A8**</span></span>                    | <span data-ttu-id="d7f02-359">28</span><span class="sxs-lookup"><span data-stu-id="d7f02-359">28</span></span>    | <span data-ttu-id="d7f02-360">только 8-разрядный альфа.</span><span class="sxs-lookup"><span data-stu-id="d7f02-360">8-bit alpha only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="d7f02-361">**D3DFMT \_ A8R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="d7f02-361">**D3DFMT\_A8R3G3B2**</span></span>              | <span data-ttu-id="d7f02-362">29</span><span class="sxs-lookup"><span data-stu-id="d7f02-362">29</span></span>    | <span data-ttu-id="d7f02-363">16-разрядный формат текстуры ARGB, использующий 8 бит для альфа, 3 бита для красного и зеленого и 2 бита для синего.</span><span class="sxs-lookup"><span data-stu-id="d7f02-363">16-bit ARGB texture format using 8 bits for alpha, 3 bits each for red and green, and 2 bits for blue.</span></span>                                                                    |
| <span data-ttu-id="d7f02-364">**D3DFMT \_ X4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="d7f02-364">**D3DFMT\_X4R4G4B4**</span></span>              | <span data-ttu-id="d7f02-365">30</span><span class="sxs-lookup"><span data-stu-id="d7f02-365">30</span></span>    | <span data-ttu-id="d7f02-366">16-битный формат пикселей RGB, использующий 4 бита для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="d7f02-366">16-bit RGB pixel format using 4 bits for each color.</span></span>                                                                                                                      |
| <span data-ttu-id="d7f02-367">**D3DFMT \_ A2B10G10R10**</span><span class="sxs-lookup"><span data-stu-id="d7f02-367">**D3DFMT\_A2B10G10R10**</span></span>           | <span data-ttu-id="d7f02-368">31</span><span class="sxs-lookup"><span data-stu-id="d7f02-368">31</span></span>    | <span data-ttu-id="d7f02-369">32-разрядный формат пикселей, использующий 10 бит для каждого цвета и 2 бита для альфа.</span><span class="sxs-lookup"><span data-stu-id="d7f02-369">32-bit pixel format using 10 bits for each color and 2 bits for alpha.</span></span>                                                                                                    |
| <span data-ttu-id="d7f02-370">**D3DFMT \_ A8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-370">**D3DFMT\_A8B8G8R8**</span></span>              | <span data-ttu-id="d7f02-371">32</span><span class="sxs-lookup"><span data-stu-id="d7f02-371">32</span></span>    | <span data-ttu-id="d7f02-372">32-разрядный формат пикселей ARGB в Alpha с использованием 8 бит на канал.</span><span class="sxs-lookup"><span data-stu-id="d7f02-372">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="d7f02-373">**D3DFMT \_ X8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-373">**D3DFMT\_X8B8G8R8**</span></span>              | <span data-ttu-id="d7f02-374">33</span><span class="sxs-lookup"><span data-stu-id="d7f02-374">33</span></span>    | <span data-ttu-id="d7f02-375">32-разрядный формат пикселей RGB, где 8 бит зарезервированы для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="d7f02-375">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="d7f02-376">**D3DFMT \_ G16R16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-376">**D3DFMT\_G16R16**</span></span>                | <span data-ttu-id="d7f02-377">34</span><span class="sxs-lookup"><span data-stu-id="d7f02-377">34</span></span>    | <span data-ttu-id="d7f02-378">32-разрядный формат пикселей, использующий 16 бит для зеленого и Красного.</span><span class="sxs-lookup"><span data-stu-id="d7f02-378">32-bit pixel format using 16 bits each for green and red.</span></span>                                                                                                                 |
| <span data-ttu-id="d7f02-379">**D3DFMT \_ A2R10G10B10**</span><span class="sxs-lookup"><span data-stu-id="d7f02-379">**D3DFMT\_A2R10G10B10**</span></span>           | <span data-ttu-id="d7f02-380">35</span><span class="sxs-lookup"><span data-stu-id="d7f02-380">35</span></span>    | <span data-ttu-id="d7f02-381">32-разрядный формат пикселей, использующий по 10 бит для красного, зеленого и синего, а 2 бита для альфа.</span><span class="sxs-lookup"><span data-stu-id="d7f02-381">32-bit pixel format using 10 bits each for red, green, and blue, and 2 bits for alpha.</span></span>                                                                                    |
| <span data-ttu-id="d7f02-382">**D3DFMT \_ A16B16G16R16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-382">**D3DFMT\_A16B16G16R16**</span></span>          | <span data-ttu-id="d7f02-383">36</span><span class="sxs-lookup"><span data-stu-id="d7f02-383">36</span></span>    | <span data-ttu-id="d7f02-384">64-разрядный формат пикселей, использующий 16 бит для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d7f02-384">64-bit pixel format using 16 bits for each component.</span></span>                                                                                                                     |
| <span data-ttu-id="d7f02-385">**D3DFMT \_ A8P8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-385">**D3DFMT\_A8P8**</span></span>                  | <span data-ttu-id="d7f02-386">40</span><span class="sxs-lookup"><span data-stu-id="d7f02-386">40</span></span>    | <span data-ttu-id="d7f02-387">8-битовый цвет, индексируемый 8 битами альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="d7f02-387">8-bit color indexed with 8 bits of alpha.</span></span>                                                                                                                                 |
| <span data-ttu-id="d7f02-388">**D3DFMT \_ P8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-388">**D3DFMT\_P8**</span></span>                    | <span data-ttu-id="d7f02-389">41</span><span class="sxs-lookup"><span data-stu-id="d7f02-389">41</span></span>    | <span data-ttu-id="d7f02-390">8-разрядный индексированный цвет.</span><span class="sxs-lookup"><span data-stu-id="d7f02-390">8-bit color indexed.</span></span>                                                                                                                                                      |
| <span data-ttu-id="d7f02-391">**D3DFMT \_ 8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-391">**D3DFMT\_L8**</span></span>                    | <span data-ttu-id="d7f02-392">50</span><span class="sxs-lookup"><span data-stu-id="d7f02-392">50</span></span>    | <span data-ttu-id="d7f02-393">только 8-разрядная светимость.</span><span class="sxs-lookup"><span data-stu-id="d7f02-393">8-bit luminance only.</span></span>                                                                                                                                                     |
| <span data-ttu-id="d7f02-394">**D3DFMT \_ L16**</span><span class="sxs-lookup"><span data-stu-id="d7f02-394">**D3DFMT\_L16**</span></span>                   | <span data-ttu-id="d7f02-395">81</span><span class="sxs-lookup"><span data-stu-id="d7f02-395">81</span></span>    | <span data-ttu-id="d7f02-396">16-разрядная светимость.</span><span class="sxs-lookup"><span data-stu-id="d7f02-396">16-bit luminance only.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d7f02-397">**D3DFMT \_ A8L8**</span><span class="sxs-lookup"><span data-stu-id="d7f02-397">**D3DFMT\_A8L8**</span></span>                  | <span data-ttu-id="d7f02-398">51</span><span class="sxs-lookup"><span data-stu-id="d7f02-398">51</span></span>    | <span data-ttu-id="d7f02-399">16-разрядная с использованием 8 бит для альфа и светимости.</span><span class="sxs-lookup"><span data-stu-id="d7f02-399">16-bit using 8 bits each for alpha and luminance.</span></span>                                                                                                                         |
| <span data-ttu-id="d7f02-400">**D3DFMT \_ A4L4**</span><span class="sxs-lookup"><span data-stu-id="d7f02-400">**D3DFMT\_A4L4**</span></span>                  | <span data-ttu-id="d7f02-401">52</span><span class="sxs-lookup"><span data-stu-id="d7f02-401">52</span></span>    | <span data-ttu-id="d7f02-402">8-разрядное использование 4 бит для альфа и светимости.</span><span class="sxs-lookup"><span data-stu-id="d7f02-402">8-bit using 4 bits each for alpha and luminance.</span></span>                                                                                                                          |
| <span data-ttu-id="d7f02-403">**D3DFMT \_ a1**</span><span class="sxs-lookup"><span data-stu-id="d7f02-403">**D3DFMT\_A1**</span></span>                    | <span data-ttu-id="d7f02-404">118</span><span class="sxs-lookup"><span data-stu-id="d7f02-404">118</span></span>   | <span data-ttu-id="d7f02-405">1-разрядный монохромный.</span><span class="sxs-lookup"><span data-stu-id="d7f02-405">1-bit monochrome.</span></span> <span data-ttu-id="d7f02-406">**Различия между Direct3D 9 и Direct3D 9Ex:** Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d7f02-406">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                            |
| <span data-ttu-id="d7f02-407">**D3DFMT \_ A2B10G10R10 \_ XR \_**</span><span class="sxs-lookup"><span data-stu-id="d7f02-407">**D3DFMT\_A2B10G10R10\_XR\_BIAS**</span></span> | <span data-ttu-id="d7f02-408">119</span><span class="sxs-lookup"><span data-stu-id="d7f02-408">119</span></span>   | <span data-ttu-id="d7f02-409">2,8-смещенная Фиксированная точка.</span><span class="sxs-lookup"><span data-stu-id="d7f02-409">2.8-biased fixed point.</span></span> <span data-ttu-id="d7f02-410">**Различия между Direct3D 9 и Direct3D 9Ex:** Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d7f02-410">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                      |
| <span data-ttu-id="d7f02-411">**D3DFMT \_ бинарибуффер**</span><span class="sxs-lookup"><span data-stu-id="d7f02-411">**D3DFMT\_BINARYBUFFER**</span></span>          | <span data-ttu-id="d7f02-412">199</span><span class="sxs-lookup"><span data-stu-id="d7f02-412">199</span></span>   | <span data-ttu-id="d7f02-413">Двоичный формат, указывающий, что данные не имеют встроенного типа.</span><span class="sxs-lookup"><span data-stu-id="d7f02-413">Binary format indicating that the data has no inherent type.</span></span> <span data-ttu-id="d7f02-414">**Различия между Direct3D 9 и Direct3D 9Ex:** Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d7f02-414">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

### <a name="other"></a><span data-ttu-id="d7f02-415">Другое</span><span class="sxs-lookup"><span data-stu-id="d7f02-415">Other</span></span>

<span data-ttu-id="d7f02-416">Этот флаг используется для неопределенных форматов.</span><span class="sxs-lookup"><span data-stu-id="d7f02-416">This flag is used for undefined formats.</span></span>



| <span data-ttu-id="d7f02-417">Другие флаги</span><span class="sxs-lookup"><span data-stu-id="d7f02-417">Other flags</span></span>         | <span data-ttu-id="d7f02-418">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-418">Value</span></span> | <span data-ttu-id="d7f02-419">Формат</span><span class="sxs-lookup"><span data-stu-id="d7f02-419">Format</span></span>                    |
|---------------------|-------|---------------------------|
| <span data-ttu-id="d7f02-420">**D3DFMT \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="d7f02-420">**D3DFMT\_UNKNOWN**</span></span> | <span data-ttu-id="d7f02-421">0</span><span class="sxs-lookup"><span data-stu-id="d7f02-421">0</span></span>     | <span data-ttu-id="d7f02-422">Формат поверхности неизвестен</span><span class="sxs-lookup"><span data-stu-id="d7f02-422">Surface format is unknown</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d7f02-423">Требования</span><span class="sxs-lookup"><span data-stu-id="d7f02-423">Requirements</span></span>



| <span data-ttu-id="d7f02-424">Требование</span><span class="sxs-lookup"><span data-stu-id="d7f02-424">Requirement</span></span> | <span data-ttu-id="d7f02-425">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f02-425">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f02-426">Header</span><span class="sxs-lookup"><span data-stu-id="d7f02-426">Header</span></span><br/> | <dl> <span data-ttu-id="d7f02-427"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f02-427"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f02-428">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7f02-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f02-429">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="d7f02-429">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




