---
description: В материалах описывается, как многоугольники отражают освещение или отображаются для эмиссии освещения в трехмерной сцене.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Материалы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564148"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="bc5a0-103">Материалы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="bc5a0-104">В материалах описывается, как многоугольники отражают освещение или отображаются для эмиссии освещения в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="bc5a0-105">Свойства материала. подробные сведения о порождаемом диффузии, отражении окружающей среды, светлых излучений и характеристиках отражения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="bc5a0-106">Direct3D использует структуру [**D3DMATERIAL9**](d3dmaterial9.md) для получения всех сведений о свойствах материалов.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="bc5a0-107">За исключением отраженного свойства, каждое свойство описывается как цвет RGBA, который показывает, какая часть красной, зеленой и синей частей данного типа освещения отражается, и коэффициент альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="bc5a0-108">Рассеянное и внешнее отражение</span><span class="sxs-lookup"><span data-stu-id="bc5a0-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="bc5a0-109">Элементы диффузной и внешней среды структуры [**D3DMATERIAL9**](d3dmaterial9.md) описывают, как материал отражает внешний и рассеянный свет в сцене.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="bc5a0-110">Поскольку большинство сцен содержат гораздо больше света, чем внешний свет, Рассеянное отражение играет наибольшую часть в определении цвета.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="bc5a0-111">Кроме того, так как рассеянный свет является направленным, то его угол влияет на общую интенсивность отражения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="bc5a0-112">Рассеянное отражение очень большое, когда свет размещает вершину параллельно с нормальной вершиной.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="bc5a0-113">При увеличении угла уменьшается воздействие размытого отражения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="bc5a0-114">Интенсивность освещения — это косинус угла между входящими источниками и нормальными вершинами, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![Иллюстрация величины отраженного освещения](images/incident.png)

<span data-ttu-id="bc5a0-116">Отражение окружения, как и внешний свет, является ненаправленным.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="bc5a0-117">Отражение окружения оказывает меньшее влияние на видимый цвет отображаемого объекта, но он влияет на общий цвет и является наиболее заметным, когда немалое освещение отразится на материале.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="bc5a0-118">Внешнее отражение материала затронет внешний свет, заданный для сцены, вызывая метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) с \_ флагом окружения D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="bc5a0-119">Рассеянное и внешнее отражение работают вместе для определения воспринимаемого цвета объекта и обычно являются идентичными значениями.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="bc5a0-120">Например, чтобы визуализировать синий объект кристаллине, необходимо создать материал, отражающий только синий компонент рассеянного и внешнего света.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="bc5a0-121">При помещении в комнату с белым освещением кристалл отображается синим цветом.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="bc5a0-122">Однако в комнате, которая имеет только красный свет, тот же кристалл кажется черним, так как его материал не отражает красный свет.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="bc5a0-123">Вывода</span><span class="sxs-lookup"><span data-stu-id="bc5a0-123">Emission</span></span>

<span data-ttu-id="bc5a0-124">Материалы можно использовать, чтобы сделать готовый к просмотру объект самолуминаус.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="bc5a0-125">Элемент эмиссионный структуры [**D3DMATERIAL9**](d3dmaterial9.md) используется для описания цвета и прозрачности порожденного освещения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="bc5a0-126">Излучение влияет на цвет объекта и может, например, сделать темный материал ярче и частично перенять излучаемый цвет.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="bc5a0-127">Свойство эмиссионный материала можно использовать для добавления иллюзии, что объект порождает освещение, без затрат на вычислительные издержки, возникающие при добавлении освещения в сцену.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="bc5a0-128">В случае синего кристалла свойство эмиссионный полезно, если нужно сделать так, чтобы Crystal отображался светло, но не приводить освещение к другим объектам в сцене.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="bc5a0-129">Помните, что материалы со свойствами эмиссионный не создают освещение, которое может быть отражено другими объектами в сцене.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="bc5a0-130">Чтобы добиться этого отраженного освещения, необходимо поместить дополнительный источник в сцену.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="bc5a0-131">Отраженное отражение</span><span class="sxs-lookup"><span data-stu-id="bc5a0-131">Specular Reflection</span></span>

<span data-ttu-id="bc5a0-132">Отраженное отражение создает выделения для объектов, делая их блестящими.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="bc5a0-133">Структура [**D3DMATERIAL9**](d3dmaterial9.md) содержит два элемента, описывающих цвет отраженного выделения, а также общий коэффициента блеска материала.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="bc5a0-134">Вы устанавливаете цвет отраженных светов, устанавливая для элемента отражения нужный цвет RGBA, наиболее распространенные цвета — белые или светло-серые.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="bc5a0-135">Значения, заданные в элементе управления "член электропитания", насколько остры отраженные эффекты.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="bc5a0-136">Отраженные блики могут создавать значительные эффекты.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="bc5a0-137">Повторное рисование на синем аналоговом устройстве. более высокое значение питания создает визуальные блики, что делает кристалл довольно блестящим.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="bc5a0-138">Меньшие значения увеличивают область действия, создавая тусклое отражение, которое делает Crystal Фрости.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="bc5a0-139">Чтобы сделать объект действительно матовым, установите для элемента питания значение 0, а для параметра цвет в отражении — черный.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="bc5a0-140">Поэкспериментируйте с различными уровнями отражения, чтобы получить реалистичный внешний вид для ваших нужд.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="bc5a0-141">На следующем рисунке показаны две идентичные модели.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="bc5a0-142">В левой части используется отражающая степень отражения 10; модель справа не имеет отраженного отражения.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![Иллюстрация моделей отраженного отражения](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="bc5a0-144">Задание свойств материала</span><span class="sxs-lookup"><span data-stu-id="bc5a0-144">Setting Material Properties</span></span>

<span data-ttu-id="bc5a0-145">Устройства рендеринга Direct3D могут быть отображены одновременно с одним набором свойств материала.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="bc5a0-146">В приложении C++ вы задаете свойства материала, используемые системой, подготавливая структуру [**D3DMATERIAL9**](d3dmaterial9.md) , а затем вызывая метод [**IDirect3DDevice9:: сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .</span><span class="sxs-lookup"><span data-stu-id="bc5a0-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="bc5a0-147">Чтобы подготовить структуру [**D3DMATERIAL9**](d3dmaterial9.md) для использования, установите сведения о свойствах в структуре, чтобы создать желаемый результат во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="bc5a0-148">В следующем примере кода настраивается структура **D3DMATERIAL9** для фиолетовых материалов с четкими белыми отражающими светами.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="bc5a0-149">После подготовки структуры [**D3DMATERIAL9**](d3dmaterial9.md) необходимо применить свойства, вызвав метод [**IDirect3DDevice9:: сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) устройства отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="bc5a0-150">Этот метод принимает адрес подготовленной структуры **D3DMATERIAL9** в качестве единственного параметра.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="bc5a0-151">При необходимости можно вызвать **IDirect3DDevice9:: сетматериал** с новыми сведениями для обновления свойств материала устройства.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="bc5a0-152">В следующем примере кода показано, как это может выглядеть в коде.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="bc5a0-153">При создании устройства Direct3D текущий материал автоматически устанавливается в значение по умолчанию, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="bc5a0-154">Член</span><span class="sxs-lookup"><span data-stu-id="bc5a0-154">Member</span></span>   | <span data-ttu-id="bc5a0-155">Значение</span><span class="sxs-lookup"><span data-stu-id="bc5a0-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="bc5a0-156">Диффузное</span><span class="sxs-lookup"><span data-stu-id="bc5a0-156">Diffuse</span></span>  | <span data-ttu-id="bc5a0-157">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="bc5a0-158">Отражающее</span><span class="sxs-lookup"><span data-stu-id="bc5a0-158">Specular</span></span> | <span data-ttu-id="bc5a0-159">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="bc5a0-160">Окружающее</span><span class="sxs-lookup"><span data-stu-id="bc5a0-160">Ambient</span></span>  | <span data-ttu-id="bc5a0-161">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="bc5a0-162">Эмиссионное</span><span class="sxs-lookup"><span data-stu-id="bc5a0-162">Emissive</span></span> | <span data-ttu-id="bc5a0-163">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="bc5a0-164">Мощный</span><span class="sxs-lookup"><span data-stu-id="bc5a0-164">Power</span></span>    | <span data-ttu-id="bc5a0-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="bc5a0-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="bc5a0-166">Получение свойств материалов</span><span class="sxs-lookup"><span data-stu-id="bc5a0-166">Retrieving Material Properties</span></span>

<span data-ttu-id="bc5a0-167">Вы получаете свойства материала, которые в настоящее время использует устройство отрисовки, вызывая метод [**IDirect3DDevice9::-Material**](/windows/desktop/api) для устройства.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="bc5a0-168">В отличие от метода [**IDirect3DDevice9:: сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9:: Material** не требует подготовки.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="bc5a0-169">Метод **IDirect3DDevice9::** D3DMATERIAL9 принимает адрес структуры [](d3dmaterial9.md) и заполняет предоставленную структуру данными, описывающими текущие свойства материала, перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="bc5a0-170">Если приложение не указывает свойства материала для подготовки к просмотру, система использует материал по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="bc5a0-171">Материал по умолчанию отражает все освещение светло-белого цвета, например без внешнего или отраженного отражения и не имеет цвета эмиссионный.</span><span class="sxs-lookup"><span data-stu-id="bc5a0-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc5a0-172">См. также</span><span class="sxs-lookup"><span data-stu-id="bc5a0-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc5a0-173">Индикаторы и материалы</span><span class="sxs-lookup"><span data-stu-id="bc5a0-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
