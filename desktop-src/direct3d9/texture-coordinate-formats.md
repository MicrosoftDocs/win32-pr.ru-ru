---
description: Координаты текстуры в Direct3D могут включать один, два, три или четыре элемента с плавающей запятой для адресации текстур с различными уровнями измерения.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Форматы координат текстуры (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806862"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="163f5-103">Форматы координат текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="163f5-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="163f5-104">Координаты текстуры в Direct3D могут включать один, два, три или четыре элемента с плавающей запятой для адресации текстур с различными уровнями измерения.</span><span class="sxs-lookup"><span data-stu-id="163f5-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="163f5-105">Поверхностная текстура — Текстурная поверхность с размерами 1-на n пикселей текстуры — адресованы одной координате текстуры.</span><span class="sxs-lookup"><span data-stu-id="163f5-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="163f5-106">Наиболее распространенный случай — двумерные текстуры с двумя координатами текстуры, обычно именуемыми и v.</span><span class="sxs-lookup"><span data-stu-id="163f5-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="163f5-107">Direct3D поддерживает два типа трехмерных текстур: карты в кубических средах и текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="163f5-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="163f5-108">Карты в кубических средах не являются по-настоящему трехмерными, но они решаются с помощью трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="163f5-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="163f5-109">Дополнительные сведения см. в разделе [кубические сопоставления среды (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="163f5-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="163f5-110">Как описано в разделе [фиксированная функция Фвф Codes (Direct3D 9)](fixed-function-fvf-codes.md), приложения кодируют координаты текстуры в формате вершин.</span><span class="sxs-lookup"><span data-stu-id="163f5-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="163f5-111">Формат вершины может включать несколько наборов координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="163f5-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="163f5-112">Используйте D3DFVF \_ TEX0 через D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) , чтобы описать формат вершин, который не включает координаты текстуры, или столько же восьми наборов.</span><span class="sxs-lookup"><span data-stu-id="163f5-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="163f5-113">Каждый набор координат текстуры может иметь от одного до четырех элементов.</span><span class="sxs-lookup"><span data-stu-id="163f5-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="163f5-114">\_Флаги D3DFVF TEXTUREFORMAT1 через D3DFVF \_ TEXTUREFORMAT4 описывают количество элементов в координатах текстуры в наборе, но эти флаги не используются сами по себе.</span><span class="sxs-lookup"><span data-stu-id="163f5-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="163f5-115">Вместо этого набор макросов [**D3DFVF \_ текскурдсизен**](d3dfvf-texcoordsizen.md) использует эти флаги для создания битовых шаблонов, описывающих количество элементов, используемых определенным набором координат текстуры в формате вершины.</span><span class="sxs-lookup"><span data-stu-id="163f5-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="163f5-116">Эти макросы принимают один параметр, который определяет индекс набора координат, число элементов в котором определяется.</span><span class="sxs-lookup"><span data-stu-id="163f5-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="163f5-117">В следующем примере показано, как используются эти макросы.</span><span class="sxs-lookup"><span data-stu-id="163f5-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="163f5-118">За исключением сопоставлений в кубических средах и текстур томов, средства программной прорисовки не могут использовать текстуры с использованием более чем двух элементов.</span><span class="sxs-lookup"><span data-stu-id="163f5-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="163f5-119">Приложения могут предоставлять до трех элементов для координаты текстуры, но только в том случае, если текстура является картой Куба, текстурой тома или \_ флагом преобразования D3DTTFF прогнозной текстуры.</span><span class="sxs-lookup"><span data-stu-id="163f5-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="163f5-120">\_Флаг прогноза D3DTTFF заставляет средство программной прорисовки разделить первые два элемента на третий (или n) элемент.</span><span class="sxs-lookup"><span data-stu-id="163f5-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="163f5-121">Дополнительные сведения см. в разделе [преобразования координат текстуры (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="163f5-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="163f5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="163f5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="163f5-123">Координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="163f5-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



