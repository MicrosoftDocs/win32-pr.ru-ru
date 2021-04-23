---
description: Схема выпуклости — это объект IDirect3DTexture9, который использует специализированный формат пикселей.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Форматы пикселей выпуклого распределения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072513"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="a94d5-103">Форматы пикселей выпуклого распределения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a94d5-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="a94d5-104">Схема выпуклости — это объект [**IDirect3DTexture9**](/windows/desktop/api) , который использует специализированный формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="a94d5-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="a94d5-105">Вместо того чтобы хранить компоненты красного, зеленого и синего цветов, каждый пиксель на карте выпуклости сохраняет значения Дельта для вас и v (D<sub>U</sub> <sub>и D)</sub>и иногда является компонентом светимости L. Эти значения применяются системой, как описано в разделе [формулы сопоставления выпуклости (Direct3D 9)](bump-mapping-formulas.md) .</span><span class="sxs-lookup"><span data-stu-id="a94d5-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="a94d5-106">Можно указать формат пикселей гиперкарты, задав один из следующих форматов: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 или D3DFMT \_ V16U16.</span><span class="sxs-lookup"><span data-stu-id="a94d5-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="a94d5-107">Описание см. в разделе [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="a94d5-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="a94d5-108">Компоненты точки<sub>d и</sub> d<sub>V</sub> имеют значения со знаком в диапазоне от-1,0 до + 1,0.</span><span class="sxs-lookup"><span data-stu-id="a94d5-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="a94d5-109">Компонент светимости, при использовании, является целочисленным значением без знака в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="a94d5-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="a94d5-110">Прежде чем выбрать формат пикселей гиперкарты, проверьте, поддерживается ли определенный формат.</span><span class="sxs-lookup"><span data-stu-id="a94d5-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="a94d5-111">Дополнительные сведения см. [в разделе Использование сопоставления выпуклости (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="a94d5-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a94d5-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a94d5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94d5-113">Сопоставление рельефов</span><span class="sxs-lookup"><span data-stu-id="a94d5-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



