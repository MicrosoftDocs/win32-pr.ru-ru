---
title: Автоматически создаваемые координаты текстуры (Direct3D 9)
description: Система может использовать преобразованное расположение камеры или нормали от вершины в качестве координат текстуры или вычислить три вектора элементов, используемых для адресации схемы кубической среды.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843295"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="62418-103">Автоматически создаваемые координаты текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62418-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="62418-104">Система может использовать преобразованное расположение камеры или нормали от вершины в качестве координат текстуры или вычислить три вектора элементов, используемых для адресации схемы кубической среды.</span><span class="sxs-lookup"><span data-stu-id="62418-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="62418-105">Как и координаты текстуры, явно указанные в вершине, в качестве входных данных для преобразования координат текстуры можно использовать автоматически созданные координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="62418-106">Автоматически созданные координаты текстуры могут значительно снизить пропускную способность, необходимую для геометрических данных, устраняя необходимость в явных координатах текстуры в формате вершин.</span><span class="sxs-lookup"><span data-stu-id="62418-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="62418-107">Во многих случаях координаты текстуры, формируемые системой, можно использовать с преобразованиями для создания специальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="62418-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="62418-108">Конечно, это специальная функция, и вы будете использовать явные координаты текстуры во многих случаях.</span><span class="sxs-lookup"><span data-stu-id="62418-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="62418-109">Настройка автоматически создаваемых координат текстуры</span><span class="sxs-lookup"><span data-stu-id="62418-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="62418-110">В C++ \_ состояние этапа текстуры D3DTSS текскурдиндекс (из перечислимого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) определяет, как система создает координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="62418-111">Как правило, это состояние указывает системе на использование определенного набора координат текстуры, закодированных в формате вершин.</span><span class="sxs-lookup"><span data-stu-id="62418-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="62418-112">При включении \_ \_ флагов D3DTSS тЦи КАМЕРАСПАЦЕНОРМАЛ, D3DTSS \_ ТЦИ \_ камераспацепоситион или D3DTSS \_ тЦи камераспацерефлектионвектор \_ в значении, назначенном этому состоянию, поведение системы сильно отличается.</span><span class="sxs-lookup"><span data-stu-id="62418-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="62418-113">При наличии любого из этих флагов стадия текстуры не учитывает координаты текстуры в пределах формата вершин в пользу координат, создаваемых системой.</span><span class="sxs-lookup"><span data-stu-id="62418-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="62418-114">В следующем списке приведены значения для каждого флага.</span><span class="sxs-lookup"><span data-stu-id="62418-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="62418-115">D3DTSS \_ тЦи \_ камераспаценормал</span><span class="sxs-lookup"><span data-stu-id="62418-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="62418-116">Используйте нормальную вершину, преобразованную в пространство камеры, в качестве координат входной текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="62418-117">D3DTSS \_ тЦи \_ камераспацепоситион</span><span class="sxs-lookup"><span data-stu-id="62418-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="62418-118">Используйте расположение вершины, преобразованное в область камеры, в качестве координат входной текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="62418-119">D3DTSS \_ тЦи \_ камераспацерефлектионвектор</span><span class="sxs-lookup"><span data-stu-id="62418-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="62418-120">Используйте Вектор отражения, преобразованный в пространство камеры, в качестве координат входной текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="62418-121">Вектор отражения вычисляются на основе расположения входной вершины и обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="62418-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="62418-122">Флаги индекса координаты текстуры являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="62418-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="62418-123">В этом примере используется:</span><span class="sxs-lookup"><span data-stu-id="62418-123">This example uses:</span></span>

-   <span data-ttu-id="62418-124">Координата вершины (на камере) как входные координаты текстуры для этой стадии текстуры</span><span class="sxs-lookup"><span data-stu-id="62418-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="62418-125">Режим переноса, заданный в \_ состоянии рендеринга D3DRENDERSTATE WRAP1</span><span class="sxs-lookup"><span data-stu-id="62418-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="62418-126">Автоматически созданные координаты текстуры наиболее полезны в качестве входных значений для преобразования координат текстуры или для исключения необходимости в приложении для расчета векторов с тремя элементами для карт кубической среды.</span><span class="sxs-lookup"><span data-stu-id="62418-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="62418-127">При сопоставлении сфер используется предварительно вычисленная Текстурная схема (во времени модели), которая содержит всю среду, как отражается в сфере Chrome.</span><span class="sxs-lookup"><span data-stu-id="62418-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="62418-128">В Direct3D предусмотрена функция создания координат текстуры с помощью визуализации State D3DTSS \_ тЦи \_ камераспаценормал, которая принимает нормальную вершину в пространстве камеры и помещает ее через преобразование текстуры для создания координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="62418-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62418-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="62418-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62418-130">Обработка координат текстуры</span><span class="sxs-lookup"><span data-stu-id="62418-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="62418-131">Преобразования координат текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62418-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="62418-132">Сопоставление кубических сред (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62418-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
