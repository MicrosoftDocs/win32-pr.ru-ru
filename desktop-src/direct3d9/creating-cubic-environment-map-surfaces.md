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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Создание поверхностей карт кубической среды (Direct3D 9)

Текстуру с картой кубической среды можно создать, вызвав метод [**креатекубетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) . Текстуры карт кубической среды должны быть квадратными, с измерениями, которые являются степенью числа двух.

В следующем примере кода показано, как приложение C++ может создать простую карту кубической среды.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Доступ к граням карт кубической среды

С помощью метода [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) можно перемещаться между лицами схемы кубической среды.

В следующем примере кода используется [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) для получения поверхности схемы куба, используемой для положительного y-Face (лицевой стороны 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Первый параметр, [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) , принимает значение [**D3DCUBEMAP, \_**](./d3dcubemap-faces.md) которое описывает присоединенную поверхность, которую должен извлечь метод. Второй параметр указывает Direct3D, какой уровень текстуры Куба мипмаппед нужно извлечь. Третий параметр принимает адрес интерфейса [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , представляющего возвращенную поверхность текстуры Куба. Так как этот куб-Map не является мипмаппед, здесь используется 0.

> [!Note]
>
> После вызова этого метода увеличивается число внутренних ссылок на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Когда вы завершите работу с этой поверхностью, обязательно вызовите метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для этого интерфейса **IDirect3DSurface9** или получите утечку памяти.

 

## <a name="rendering-to-cubic-environment-maps"></a>Визуализация на картах кубических сред

Изображения можно копировать в отдельные лица схемы куба точно так же, как любые другие текстуры или объекты Surface. Самое важное, что необходимо сделать перед отрисовкой на лицевой стороне, — установить матрицы преобразования таким образом, чтобы камера правильно позиционируется и указывала на правильное направление для этого лица: Forward (+ z), назад (-z), Left (-x), Right (+ x), up (+ y) или Down (-y).

Следующий пример кода C++ подготавливает и задает матрицу представления в соответствии с отображаемым лицом.


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



Помните, что каждая поверхность схемы кубической среды представляет собой поле зрения в 90 градусов. Если приложению не требуется другое поле угла представления, для специальных эффектов, например, необходимо настроить матрицу проекции соответствующим образом.

В этом примере кода создается и задается матрица проекции для наиболее распространенного случая.


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



Если камера находится в положении, а матрица проекции задана, то можно визуализировать сцену. Каждый объект в сцене должен располагаться как обычно. В следующем примере кода, предоставленном для полноты, описана эта задача.


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



Обратите внимание на вызов метода [**сетрендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . При подготовке к просмотру на стороне схемы куба необходимо назначить грань в качестве текущей поверхности целевого объекта рендеринга. Приложения, использующие буферы глубины, могут явно создать буфер глубины для целевого объекта рендеринга или переназначить существующий буфер глубины для поверхности целевого объекта визуализации. В приведенном выше примере кода используется второй подход.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление кубических сред](cubic-environment-mapping.md)
</dt> </dl>

 

 
