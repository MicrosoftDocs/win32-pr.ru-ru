---
description: Этот раздел содержит сведения о внутренней организации форматов сжатых текстур.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Форматы сжатых текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807750"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="5db7e-103">Форматы сжатых текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5db7e-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="5db7e-104">Этот раздел содержит сведения о внутренней организации форматов сжатых текстур.</span><span class="sxs-lookup"><span data-stu-id="5db7e-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="5db7e-105">Эти сведения не нужны для использования сжатых текстур, так как функции D3DX можно использовать для преобразования в сжатые форматы и из них.</span><span class="sxs-lookup"><span data-stu-id="5db7e-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="5db7e-106">Однако эта информация окажется полезной, если потребуется выполнять операции со сжатыми поверхностными данными напрямую.</span><span class="sxs-lookup"><span data-stu-id="5db7e-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="5db7e-107">В Direct3D используется формат сжатия, который делит карты текстур на текстовые блоки 4x4.</span><span class="sxs-lookup"><span data-stu-id="5db7e-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="5db7e-108">Если текстура не имеет прозрачности (то есть является непрозрачной) или прозрачность задана 1-разрядным альфа-значением, 8-байтный блок представляет блок карты текстуры.</span><span class="sxs-lookup"><span data-stu-id="5db7e-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="5db7e-109">Если карта текстуры не содержит прозрачных текселей, использующих альфа-канал, его представляет 16-байтный блок.</span><span class="sxs-lookup"><span data-stu-id="5db7e-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="5db7e-110">Непрозрачные и 1-разрядные текстуры Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5db7e-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="5db7e-111">Текстуры с альфа-каналами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5db7e-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="5db7e-112">Любая текстура должна указывать, что ее данные хранятся по 64 или 128 битов на группу из 16 текселей.</span><span class="sxs-lookup"><span data-stu-id="5db7e-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="5db7e-113">Если 64-разрядные блоки, то есть формат DXT1-используется для текстуры, можно смешивать непрозрачные и одноразрядные альфа-форматы для каждого блока в пределах той же текстуры.</span><span class="sxs-lookup"><span data-stu-id="5db7e-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="5db7e-114">Иными словами, сравнение целочисленной величины без знака \_ для цвета 0 и цвета \_ 1 выполняется уникальным образом для каждого блока 16 пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="5db7e-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="5db7e-115">Если используются 128-разрядные блоки, то для всей текстуры канал альфа должен быть указан в явном (Format DXT2 или DXT3) или режиме интерполяции (Format DXT4 или DXT5).</span><span class="sxs-lookup"><span data-stu-id="5db7e-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="5db7e-116">Как и с цветом, при использовании интерполированного режима на уровне блоков можно использовать режим восьми или шести интерполированных альфа-каналов.</span><span class="sxs-lookup"><span data-stu-id="5db7e-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="5db7e-117">Опять же, сравнение значений альфа \_ 0 и альфа \_ 1 выполняется отдельно для каждого блока.</span><span class="sxs-lookup"><span data-stu-id="5db7e-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="5db7e-118">Высота форматов Дкстн отличается от того, что было возвращено в DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="5db7e-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="5db7e-119">Шаг теперь измеряется в байтах (не блоках).</span><span class="sxs-lookup"><span data-stu-id="5db7e-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="5db7e-120">Например, если у вас ширина 16, то у вас будет шаг четырех блоков (4 \* 8 для DXT1, 4 \* 16 для DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="5db7e-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5db7e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5db7e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5db7e-122">Сжатые ресурсы текстуры</span><span class="sxs-lookup"><span data-stu-id="5db7e-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



