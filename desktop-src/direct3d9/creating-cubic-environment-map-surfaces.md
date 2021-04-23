---
description: Текстуру с картой кубической среды можно создать, вызвав метод Креатекубетекстуре. Текстуры карт кубической среды должны быть квадратными, с измерениями, которые являются степенью числа двух.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Создание поверхностей карт кубической среды (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539029"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="7e179-104">Создание поверхностей карт кубической среды (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7e179-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="7e179-105">Текстуру с картой кубической среды можно создать, вызвав метод [**креатекубетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="7e179-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="7e179-106">Текстуры карт кубической среды должны быть квадратными, с измерениями, которые являются степенью числа двух.</span><span class="sxs-lookup"><span data-stu-id="7e179-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="7e179-107">В следующем примере кода показано, как приложение C++ может создать простую карту кубической среды.</span><span class="sxs-lookup"><span data-stu-id="7e179-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="7e179-108">Доступ к граням карт кубической среды</span><span class="sxs-lookup"><span data-stu-id="7e179-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="7e179-109">С помощью метода [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) можно перемещаться между лицами схемы кубической среды.</span><span class="sxs-lookup"><span data-stu-id="7e179-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="7e179-110">В следующем примере кода используется [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) для получения поверхности схемы куба, используемой для положительного y-Face (лицевой стороны 2).</span><span class="sxs-lookup"><span data-stu-id="7e179-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="7e179-111">Первый параметр, [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) , принимает значение [**D3DCUBEMAP, \_**](./d3dcubemap-faces.md) которое описывает присоединенную поверхность, которую должен извлечь метод.</span><span class="sxs-lookup"><span data-stu-id="7e179-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="7e179-112">Второй параметр указывает Direct3D, какой уровень текстуры Куба мипмаппед нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="7e179-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="7e179-113">Третий параметр принимает адрес интерфейса [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , представляющего возвращенную поверхность текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="7e179-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="7e179-114">Так как этот куб-Map не является мипмаппед, здесь используется 0.</span><span class="sxs-lookup"><span data-stu-id="7e179-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="7e179-115">После вызова этого метода увеличивается число внутренних ссылок на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="7e179-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="7e179-116">Когда вы завершите работу с этой поверхностью, обязательно вызовите метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для этого интерфейса **IDirect3DSurface9** или получите утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="7e179-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="7e179-117">Визуализация на картах кубических сред</span><span class="sxs-lookup"><span data-stu-id="7e179-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="7e179-118">Изображения можно копировать в отдельные лица схемы куба точно так же, как любые другие текстуры или объекты Surface.</span><span class="sxs-lookup"><span data-stu-id="7e179-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="7e179-119">Самое важное, что необходимо сделать перед отрисовкой на лицевой стороне, — установить матрицы преобразования таким образом, чтобы камера правильно позиционируется и указывала на правильное направление для этого лица: Forward (+ z), назад (-z), Left (-x), Right (+ x), up (+ y) или Down (-y).</span><span class="sxs-lookup"><span data-stu-id="7e179-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="7e179-120">Следующий пример кода C++ подготавливает и задает матрицу представления в соответствии с отображаемым лицом.</span><span class="sxs-lookup"><span data-stu-id="7e179-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



<span data-ttu-id="7e179-121">Помните, что каждая поверхность схемы кубической среды представляет собой поле зрения в 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="7e179-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="7e179-122">Если приложению не требуется другое поле угла представления, для специальных эффектов, например, необходимо настроить матрицу проекции соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="7e179-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="7e179-123">В этом примере кода создается и задается матрица проекции для наиболее распространенного случая.</span><span class="sxs-lookup"><span data-stu-id="7e179-123">This code example creates and sets a projection matrix for the most common case.</span></span>


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



<span data-ttu-id="7e179-124">Если камера находится в положении, а матрица проекции задана, то можно визуализировать сцену.</span><span class="sxs-lookup"><span data-stu-id="7e179-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="7e179-125">Каждый объект в сцене должен располагаться как обычно.</span><span class="sxs-lookup"><span data-stu-id="7e179-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="7e179-126">В следующем примере кода, предоставленном для полноты, описана эта задача.</span><span class="sxs-lookup"><span data-stu-id="7e179-126">The following code example, provided for completeness, outlines this task.</span></span>


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



<span data-ttu-id="7e179-127">Обратите внимание на вызов метода [**сетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="7e179-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="7e179-128">При подготовке к просмотру на стороне схемы куба необходимо назначить грань в качестве текущей поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="7e179-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="7e179-129">Приложения, использующие буферы глубины, могут явно создать буфер глубины для целевого объекта рендеринга или переназначить существующий буфер глубины для поверхности целевого объекта визуализации.</span><span class="sxs-lookup"><span data-stu-id="7e179-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="7e179-130">В приведенном выше примере кода используется второй подход.</span><span class="sxs-lookup"><span data-stu-id="7e179-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e179-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7e179-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e179-132">Сопоставление кубических сред</span><span class="sxs-lookup"><span data-stu-id="7e179-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
