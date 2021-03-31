---
description: Использование сопоставления выпуклости (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Использование сопоставления выпуклости (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495759"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="f0a28-103">Использование сопоставления выпуклости (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f0a28-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="f0a28-104">Обнаружение поддержки для отображения рельефов</span><span class="sxs-lookup"><span data-stu-id="f0a28-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="f0a28-105">Устройство может выполнять сопоставление выпуклости, если оно поддерживает \_ \_ операцию смешения текстур D3DTOP БУМПЕНВМАП или D3DTOP бумпенвмаплуминанце.</span><span class="sxs-lookup"><span data-stu-id="f0a28-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="f0a28-106">Используйте [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) с D3DUSAGE \_ Query \_ легацибумпмап, чтобы узнать, поддерживается ли формат для сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="f0a28-107">Кроме того, приложения должны проверить возможности устройства, чтобы убедиться, что устройство поддерживает соответствующее количество стадий смешения, обычно по крайней мере три, и предоставляет по крайней мере один формат пикселей сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="f0a28-108">В следующем примере кода выполняется проверка возможностей устройства, чтобы обнаружить поддержку для сопоставления выпуклости на текущем устройстве, используя заданные критерии.</span><span class="sxs-lookup"><span data-stu-id="f0a28-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="f0a28-109">Создание текстуры с картой выпуклости</span><span class="sxs-lookup"><span data-stu-id="f0a28-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="f0a28-110">Вы создаете текстуру карт выпуклости, аналогичную любой другой текстуре.</span><span class="sxs-lookup"><span data-stu-id="f0a28-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="f0a28-111">Приложение проверяет поддержку сопоставления выпуклости и извлекает допустимый формат пикселей, как описано в разделе Обнаружение поддержки для отображения выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="f0a28-112">После создания поверхности можно загрузить каждый пиксель с соответствующими разностными значениями и светимостью, если формат поверхности включает светимость.</span><span class="sxs-lookup"><span data-stu-id="f0a28-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="f0a28-113">Значения для каждого компонента пикселей описаны в разделе [форматы точек выпуклости (Direct3D 9)](bump-map-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="f0a28-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="f0a28-114">Настройка параметров сопоставления выпуклости</span><span class="sxs-lookup"><span data-stu-id="f0a28-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="f0a28-115">Когда приложение создает карту выпуклости и устанавливает содержимое каждого пикселя, можно подготовиться к подготовке к просмотру, настроив параметры сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="f0a28-116">Параметры сопоставления выпуклости включают настройку требуемых текстур и их операции смешения, а также элементы управления преобразованием и яркостью для самой карты выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="f0a28-117">Установите базовую карту текстуры, если она используется, а также карту выпуклости и карту окружения в этапы смешения текстур.</span><span class="sxs-lookup"><span data-stu-id="f0a28-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="f0a28-118">Установите операции смешения цвета и альфа-канала для каждой стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="f0a28-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="f0a28-119">Задайте матрицу преобразования карт выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="f0a28-120">При необходимости задайте значения параметров "масштаб светимости" и "смещение".</span><span class="sxs-lookup"><span data-stu-id="f0a28-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="f0a28-121">В следующем примере кода задаются три текстуры (базовая текстура, схема выпуклости и гиперкарта) для соответствующих этапов смешения текстур.</span><span class="sxs-lookup"><span data-stu-id="f0a28-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="f0a28-122">После установки текстур на стадии смешения в следующем примере кода подготавливаются операции смешения и аргументы для каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="f0a28-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="f0a28-123">Если заданы операции смешения и аргументы, то в следующем примере кода матрица сопоставления «выпуклость 2x2» устанавливается в матрицу идентификаторов, задавая \_ элементы D3DTSS BUMPENVMAPMAT00 и D3DTSS \_ BUMPENVMAPMAT11 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) в 1,0.</span><span class="sxs-lookup"><span data-stu-id="f0a28-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="f0a28-124">Настройка матрицы для идентификации приводит к тому, что система использует разностные значения в карте выпуклости без изменений, но это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f0a28-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="f0a28-125">Если для операции отображения рельефа задана светимость (D3DTOP \_ бумпенвмаплуминанце), необходимо задать элементы управления яркостью.</span><span class="sxs-lookup"><span data-stu-id="f0a28-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="f0a28-126">Элементы управления яркостью настраивают, как система рассчитывает светимость, прежде чем модулатинг цвет из текстуры на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="f0a28-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="f0a28-127">Дополнительные сведения см. в разделе [формулы сопоставления выпуклости (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="f0a28-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="f0a28-128">После того как приложение настроит параметры сопоставления выпуклости, оно может быть отображено как нормальное, а отображаемые многоугольники получают эффекты отображения выпуклости.</span><span class="sxs-lookup"><span data-stu-id="f0a28-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="f0a28-129">Обратите внимание, что в предыдущем примере показаны параметры, настроенные для сопоставления с зеркальной средой.</span><span class="sxs-lookup"><span data-stu-id="f0a28-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="f0a28-130">При выполнении рассеянного освещения приложения устанавливают операцию смешения текстуры для последнего этапа, чтобы D3DTOPая \_ модуляция.</span><span class="sxs-lookup"><span data-stu-id="f0a28-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="f0a28-131">Дополнительные сведения см. в разделе [диффузная легкая карта (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="f0a28-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a28-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f0a28-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a28-133">Сопоставление рельефов</span><span class="sxs-lookup"><span data-stu-id="f0a28-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
