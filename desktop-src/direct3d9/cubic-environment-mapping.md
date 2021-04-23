---
description: Карты в кубических средах (иногда называемые картами кубов) — это текстуры, которые содержат графические данные, представляющие сцену вокруг объекта, как если бы объект находился в центре куба.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Сопоставление кубических сред (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423478"
---
# <a name="cubic-environment-mapping-direct3d-9"></a><span data-ttu-id="126b8-103">Сопоставление кубических сред (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="126b8-103">Cubic Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="126b8-104">Карты в кубических средах (иногда называемые картами кубов) — это текстуры, которые содержат графические данные, представляющие сцену вокруг объекта, как если бы объект находился в центре куба.</span><span class="sxs-lookup"><span data-stu-id="126b8-104">Cubic environment maps - sometimes referred to as cube maps - are textures that contain image data representing the scene surrounding an object, as if the object were in the center of a cube.</span></span> <span data-ttu-id="126b8-105">Каждая грань схемы кубической среды охватывает поле в виде поля с 90 по горизонтали и вертикали, а на карте Куба — шесть лиц.</span><span class="sxs-lookup"><span data-stu-id="126b8-105">Each face of the cubic environment map covers a 90-degree field of view in the horizontal and vertical, and there are six faces per cube map.</span></span> <span data-ttu-id="126b8-106">Ориентация сторон показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="126b8-106">The orientation of the faces is shown in the following illustration.</span></span>

![Иллюстрация Куба с центральными осями координат, перпендикулярными граням Куба](images/cubemap-cube.png)

<span data-ttu-id="126b8-108">Каждое лицо Куба ориентировано перпендикулярно плоскости x/y, y/z или x/z в мировом пространстве.</span><span class="sxs-lookup"><span data-stu-id="126b8-108">Each face of the cube is oriented perpendicular to the x/y, y/z, or x/z plane, in world space.</span></span> <span data-ttu-id="126b8-109">На следующем рисунке показано, как каждая плоскость соответствует грани.</span><span class="sxs-lookup"><span data-stu-id="126b8-109">The following illustration shows how each plane corresponds to a face.</span></span>

![Иллюстрация граней Куба с координатами проекции с плоскостей](images/cube-faces.png)

<span data-ttu-id="126b8-111">Карты кубических сред реализуются как ряд объектов текстуры.</span><span class="sxs-lookup"><span data-stu-id="126b8-111">Cubic environment maps are implemented as a series of texture objects.</span></span> <span data-ttu-id="126b8-112">Приложения могут использовать статические изображения для сопоставления в кубических средах или они могут быть отображены в лицах карты Куба для выполнения динамического сопоставления среды.</span><span class="sxs-lookup"><span data-stu-id="126b8-112">Applications can use static images for cubic environment mapping, or they can render into the faces of the cube map to perform dynamic environment mapping.</span></span> <span data-ttu-id="126b8-113">Этот метод требует, чтобы поверхности схемы куба были допустимыми областями визуализации, созданными с \_ установленным флагом РЕНДЕРТАРЖЕТ D3DUSAGE.</span><span class="sxs-lookup"><span data-stu-id="126b8-113">This technique requires that the cube-map surfaces be valid render-target surfaces, created with the D3DUSAGE\_RENDERTARGET flag set.</span></span>

<span data-ttu-id="126b8-114">Грани схемы куба не обязательно должны содержать чрезвычайно детализированные рендерингы окружающей сцены.</span><span class="sxs-lookup"><span data-stu-id="126b8-114">The faces of a cube map don't need to contain extremely detailed renderings of the surrounding scene.</span></span> <span data-ttu-id="126b8-115">В большинстве случаев карты среды применяются к изогнутым поверхности.</span><span class="sxs-lookup"><span data-stu-id="126b8-115">In most cases, environment maps are applied to curved surfaces.</span></span> <span data-ttu-id="126b8-116">Учитывая величину кривизны, используемую большинством приложений, полученное отраженное искажение дает очень подробную информацию в схеме среды, непроизводительна с точки зрения памяти и объема работ по подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="126b8-116">Given the amount of curvature used by most applications, the resulting reflective distortion makes extreme detail in the environment map wasteful in terms of memory and rendering overhead.</span></span>

## <a name="mipmapped-cubic-environment-maps"></a><span data-ttu-id="126b8-117">Карты мипмаппед кубической среды</span><span class="sxs-lookup"><span data-stu-id="126b8-117">Mipmapped Cubic Environment Maps</span></span>

<span data-ttu-id="126b8-118">Карты куба могут быть мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="126b8-118">Cube maps can be mipmapped.</span></span> <span data-ttu-id="126b8-119">Чтобы создать карту Куба мипмаппед, задайте для параметра Levels метода [**креатекубетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) нужное количество уровней.</span><span class="sxs-lookup"><span data-stu-id="126b8-119">To create a mipmapped cube map, set the Levels parameter of the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method to the number of levels that you want.</span></span> <span data-ttu-id="126b8-120">Вы можете представить топографии этих поверхностей, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="126b8-120">You can envision the topography of these surfaces as shown in the following diagram.</span></span>

![Схема схемы куба мипмаппед с n уровнями MIP](images/cubemap-mipped.png)

<span data-ttu-id="126b8-122">Приложения, создающие карты среды мипмаппед Безье, могут обращаться к каждому из них, вызывая метод [**жеткубемапсурфаце**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="126b8-122">Applications that create mipmapped cubic environment maps can access each face by calling the [**GetCubeMapSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="126b8-123">Начните с установки соответствующего значения из перечислимого [**типа \_ D3DCUBEMAP**](./d3dcubemap-faces.md) , как описано в разделе [Создание поверхностей схемы кубической среды (Direct3D 9)](creating-cubic-environment-map-surfaces.md).</span><span class="sxs-lookup"><span data-stu-id="126b8-123">Start by setting the appropriate value from the [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated type, as discussed in [Creating Cubic Environment Map Surfaces (Direct3D 9)](creating-cubic-environment-map-surfaces.md).</span></span> <span data-ttu-id="126b8-124">Затем выберите уровень для получения, задав для параметра уровня **жеткубемапсурфаце** нужный уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="126b8-124">Next, select the level to retrieve by setting the **GetCubeMapSurface** level parameter to the mipmap level that you want.</span></span> <span data-ttu-id="126b8-125">Помните, что 0 соответствует изображению верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="126b8-125">Remember that 0 corresponds with the top-level image.</span></span>

## <a name="texture-coordinates-for-cubic-environment-maps"></a><span data-ttu-id="126b8-126">Координаты текстуры для карт кубических сред</span><span class="sxs-lookup"><span data-stu-id="126b8-126">Texture Coordinates for Cubic Environment Maps</span></span>

<span data-ttu-id="126b8-127">Координаты текстуры, которые индексируют карту кубической среды, не являются простыми координатами в стиле u и v, как это используется при применении стандартных текстур.</span><span class="sxs-lookup"><span data-stu-id="126b8-127">Texture coordinates that index a cubic environment map aren't simple u, v style coordinates, as used when standard textures are applied.</span></span> <span data-ttu-id="126b8-128">Фактически, карты в кубических средах не используют координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="126b8-128">In fact, cubic environment maps don't use texture coordinates at all.</span></span> <span data-ttu-id="126b8-129">Вместо набора координат текстуры для карт кубической среды требуется трехмерный вектор.</span><span class="sxs-lookup"><span data-stu-id="126b8-129">In place of a set of texture coordinates, cubic environment maps require a 3D vector.</span></span> <span data-ttu-id="126b8-130">Необходимо указать правильный формат вершины.</span><span class="sxs-lookup"><span data-stu-id="126b8-130">You must take care to specify a proper vertex format.</span></span> <span data-ttu-id="126b8-131">Помимо указания системы на количество наборов координат текстуры, используемых приложением, необходимо предоставить сведения о количестве элементов в каждом наборе.</span><span class="sxs-lookup"><span data-stu-id="126b8-131">In addition to telling the system how many sets of texture coordinates your application uses, you must provide information about how many elements are in each set.</span></span> <span data-ttu-id="126b8-132">Для этой цели Direct3D предлагает набор макросов [**D3DFVF \_ текскурдсизен**](d3dfvf-texcoordsizen.md) .</span><span class="sxs-lookup"><span data-stu-id="126b8-132">Direct3D offers the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros for this purpose.</span></span> <span data-ttu-id="126b8-133">Эти макросы принимают один параметр, определяя индекс набора координат текстуры, для которого описывается размер.</span><span class="sxs-lookup"><span data-stu-id="126b8-133">These macros accept a single parameter, identifying the index of the texture coordinate set for which the size is being described.</span></span> <span data-ttu-id="126b8-134">В случае трехмерного вектора вы включаете битовый шаблон, созданный с помощью \_ макроса D3DFVF TEXCOORDSIZE3.</span><span class="sxs-lookup"><span data-stu-id="126b8-134">In the case of a 3D vector, you include the bit pattern created by the D3DFVF\_TEXCOORDSIZE3 macro.</span></span> <span data-ttu-id="126b8-135">В следующем примере кода показано, как используется этот макрос.</span><span class="sxs-lookup"><span data-stu-id="126b8-135">The following code example shows how this macro is used.</span></span>


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



<span data-ttu-id="126b8-136">В некоторых случаях, таких как рассеянное освещение, для вектора используется нормальная вершина камеры.</span><span class="sxs-lookup"><span data-stu-id="126b8-136">In some cases, such as diffuse light mapping, you use the camera-space vertex normal for the vector.</span></span> <span data-ttu-id="126b8-137">В других случаях, например при сопоставлении с зеркальной средой, используется вектор отражения.</span><span class="sxs-lookup"><span data-stu-id="126b8-137">In other cases, like specular environment mapping, you use a reflection vector.</span></span> <span data-ttu-id="126b8-138">Так как преобразованные нормали вершин широко понятны, информация здесь сосредоточена на вычислении вектора отражения.</span><span class="sxs-lookup"><span data-stu-id="126b8-138">Because transformed vertex normals are widely understood, the information here concentrates on computing a reflection vector.</span></span>

<span data-ttu-id="126b8-139">Вычисление собственного вектора отражения требует понимания расположения каждой вершины и вектора от точки зрения к этой вершине.</span><span class="sxs-lookup"><span data-stu-id="126b8-139">Computing a reflection vector on your own requires understanding of the position of each vertex, and of a vector from the viewpoint to that vertex.</span></span> <span data-ttu-id="126b8-140">Direct3D может автоматически вычислять векторы отражения для своей геометрии.</span><span class="sxs-lookup"><span data-stu-id="126b8-140">Direct3D can automatically compute the reflection vectors for your geometry.</span></span> <span data-ttu-id="126b8-141">Использование этой функции экономит память, так как вам не нужно включать координаты текстуры для схемы среды.</span><span class="sxs-lookup"><span data-stu-id="126b8-141">Using this feature saves memory because you don't need to include texture coordinates for the environment map.</span></span> <span data-ttu-id="126b8-142">Это также сокращает пропускную способность и, в случае с устройством&L HAL, оно может быть значительно быстрее, чем вычисления, которые приложение может сделать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="126b8-142">It also reduces bandwidth and, in the case of a T&L HAL Device, it can be significantly faster than the computations that your application can make on its own.</span></span> <span data-ttu-id="126b8-143">Чтобы использовать эту функцию, на стадии текстуры, содержащей карту кубической среды, задайте в качестве \_ состояния этапа текстуры D3DTSS текскурдиндекс сочетание \_ элемента D3DTSS тЦи Камераспацерефлектионвектор в \_ [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) и индекс набора координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="126b8-143">To use this feature, in the texture stage that contains the cubic environment map, set the D3DTSS\_TEXCOORDINDEX texture stage state to a combination of the D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR member of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) and the index of a texture coordinate set.</span></span> <span data-ttu-id="126b8-144">В некоторых ситуациях, например при сопоставлении рассеянного освещения, можно использовать D3DTSS \_ тЦи \_ Камераспаценормал в **D3DTEXTURESTAGESTATETYPE**, что приводит к тому, что система использует преобразованную, камеру-пространство, нормаль к вершине в качестве вектора адресации для текстуры.</span><span class="sxs-lookup"><span data-stu-id="126b8-144">In some situations, like diffuse light mapping, you might use the D3DTSS\_TCI\_CAMERASPACENORMAL member of **D3DTEXTURESTAGESTATETYPE**, which causes the system to use the transformed, camera-space, vertex normal as the addressing vector for the texture.</span></span> <span data-ttu-id="126b8-145">Индекс используется системой для определения режима обтекания текстуры.</span><span class="sxs-lookup"><span data-stu-id="126b8-145">The index is only used by the system to determine the wrapping mode for the texture.</span></span>

<span data-ttu-id="126b8-146">В следующем примере кода показано, как используется это значение.</span><span class="sxs-lookup"><span data-stu-id="126b8-146">The following code example shows how this value is used.</span></span>


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



<span data-ttu-id="126b8-147">При включении автоматического создания координат текстуры система использует одну из двух формул для вычисления вектора отражения для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="126b8-147">When you enable automatic texture coordinate generation, the system uses one of two formulas to compute the reflection vector for each vertex.</span></span> <span data-ttu-id="126b8-148">Если \_ для состояния отрисовки D3DRS локалвиевер задано **значение true**, используется следующая формула.</span><span class="sxs-lookup"><span data-stu-id="126b8-148">When the D3DRS\_LOCALVIEWER render state is set to **TRUE**, the following formula is used.</span></span>

![Формула вектора отражения (r = 2 (EXN) n-e)](images/reflection-vector-local.png)

<span data-ttu-id="126b8-150">В предыдущей формуле R является вычисляемым вектором отражения, E — нормализованным вектором «позиционирование на глаз», а «N» — вершиной вершины на камере.</span><span class="sxs-lookup"><span data-stu-id="126b8-150">In the preceding formula, R is the reflection vector being computed, E is the normalized position-to-eye vector, and N is the camera-space vertex normal.</span></span>

<span data-ttu-id="126b8-151">Если \_ для состояния отрисовки D3DRS локалвиевер задано **значение false**, система использует следующую формулу.</span><span class="sxs-lookup"><span data-stu-id="126b8-151">When the D3DRS\_LOCALVIEWER render state is set to **FALSE**, the system uses the following formula.</span></span>

![Формула вектора отражения (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

<span data-ttu-id="126b8-153">Элементы R и N в этой формуле идентичны предыдущей формуле.</span><span class="sxs-lookup"><span data-stu-id="126b8-153">The R and N elements in this formula are identical to the previous formula.</span></span> <span data-ttu-id="126b8-154">Элемент N<sub>z</sub> — это международный символ z вершины нормали, а I — вектор (0, 0, 1) неограниченной непрямой точки зрения.</span><span class="sxs-lookup"><span data-stu-id="126b8-154">The N<sub>Z</sub> element is the world-space z of the vertex normal, and I is the vector (0,0,1) of an infinitely distant viewpoint.</span></span> <span data-ttu-id="126b8-155">Система использует Вектор отражения из любой формулы для выбора и адресации соответствующей грани схемы куба.</span><span class="sxs-lookup"><span data-stu-id="126b8-155">The system uses the reflection vector from either formula to select and address the appropriate face of the cube map.</span></span>

> [!Note]  
> <span data-ttu-id="126b8-156">В большинстве случаев приложения должны включать автоматическую нормализацию нормалей вершин.</span><span class="sxs-lookup"><span data-stu-id="126b8-156">In most cases, applications should enable automatic normalization of vertex normals.</span></span> <span data-ttu-id="126b8-157">Для этого задайте для параметра D3DRS \_ нормализенормалс значение **true**.</span><span class="sxs-lookup"><span data-stu-id="126b8-157">To do this, set D3DRS\_NORMALIZENORMALS to **TRUE**.</span></span> <span data-ttu-id="126b8-158">Если не включить это состояние рендеринга, внешний вид схемы среды будет радикально отличаться от предполагаемого.</span><span class="sxs-lookup"><span data-stu-id="126b8-158">If you do not enable this render state, the appearance of the environment map will be drastically different than you might expect.</span></span>

 

<span data-ttu-id="126b8-159">Дополнительные сведения содержатся в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="126b8-159">Additional information is contained in the following topic.</span></span>

-   [<span data-ttu-id="126b8-160">Создание поверхностей карт кубической среды (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="126b8-160">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a><span data-ttu-id="126b8-161">См. также</span><span class="sxs-lookup"><span data-stu-id="126b8-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="126b8-162">Сопоставление окружения</span><span class="sxs-lookup"><span data-stu-id="126b8-162">Environment Mapping</span></span>](environment-mapping.md)
</dt> </dl>

 

 
