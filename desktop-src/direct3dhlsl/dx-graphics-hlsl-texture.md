---
title: Тип текстуры
description: Используйте следующий синтаксис для объявления переменной текстуры.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Тип текстуры HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "103789133"
---
# <a name="texture-type"></a><span data-ttu-id="62236-104">Тип текстуры</span><span class="sxs-lookup"><span data-stu-id="62236-104">Texture type</span></span>

<span data-ttu-id="62236-105">Используйте следующий синтаксис для объявления переменной текстуры.</span><span class="sxs-lookup"><span data-stu-id="62236-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="62236-106">**Имя типа;**</span><span class="sxs-lookup"><span data-stu-id="62236-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="62236-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="62236-107">Parameters</span></span>
| <span data-ttu-id="62236-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="62236-108">Item</span></span>                                                                                     | <span data-ttu-id="62236-109">Описание</span><span class="sxs-lookup"><span data-stu-id="62236-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62236-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="62236-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="62236-111">Один из следующих типов: текстура (нетипизированный, для обеспечения обратной совместимости), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Текстурекубе.</span><span class="sxs-lookup"><span data-stu-id="62236-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="62236-112">Размер элемента должен соответствовать 4 32-разрядному количеству.</span><span class="sxs-lookup"><span data-stu-id="62236-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="62236-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="62236-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="62236-114">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="62236-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="62236-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="62236-115">Remarks</span></span>

<span data-ttu-id="62236-116">Текстура состоит из трех частей.</span><span class="sxs-lookup"><span data-stu-id="62236-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="62236-117">Объявление переменной текстуры.</span><span class="sxs-lookup"><span data-stu-id="62236-117">Declaring a texture variable.</span></span> <span data-ttu-id="62236-118">Это делается с помощью синтаксиса, показанного выше.</span><span class="sxs-lookup"><span data-stu-id="62236-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="62236-119">Например, это допустимые объявления.</span><span class="sxs-lookup"><span data-stu-id="62236-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="62236-120">\- или -</span><span class="sxs-lookup"><span data-stu-id="62236-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="62236-121">Объявление и инициализация объекта образца.</span><span class="sxs-lookup"><span data-stu-id="62236-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="62236-122">Для этого используется немного другой синтаксис в Direct3D 9 и Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="62236-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="62236-123">Дополнительные сведения о синтаксисе объектов образца см. в разделе [тип образца (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="62236-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="62236-124">Вызов функции текстуры в шейдере.</span><span class="sxs-lookup"><span data-stu-id="62236-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="62236-125">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="62236-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="62236-126">Direct3D 9 использует [встроенные функции текстуры](dx-graphics-hlsl-intrinsic-functions.md) для выполнения операций с текстурами.</span><span class="sxs-lookup"><span data-stu-id="62236-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="62236-127">Этот пример взят из [примера басичлсл](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) и использует [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) для выполнения выборки текстур.</span><span class="sxs-lookup"><span data-stu-id="62236-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="62236-128">Вместо этого в Direct3D 10 используются [объекты текстур с шаблонами](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="62236-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="62236-129">Ниже приведен пример эквивалентной операции текстуры.</span><span class="sxs-lookup"><span data-stu-id="62236-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="62236-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62236-130">See also</span></span>

[<span data-ttu-id="62236-131">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62236-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
