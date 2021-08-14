---
description: Состояния преобразования 256-511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Использование индексированного смешения вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519479"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Использование индексированного смешения вершин (Direct3D 9)

Состояния преобразования 256-511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов. Используйте макрос [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , чтобы сопоставлять индексы 0-255 с соответствующими состояниями преобразования. В следующем примере кода показано, как использовать метод [**IDirect3DDevice9:: сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) , чтобы установить матрицу с состоянием преобразования с номером 256 в матрицу идентификаторов.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Чтобы включить или отключить индексирование вершин, установите \_ для состояния отрисовки D3DRS Индекседвертексбленденабле **значение true**. Если состояние отрисовки включено, то индексы матрицы необходимо передавать в виде упакованных DWORD с каждой вершиной. Если состояние рендеринга отключено и включено смешение вершин, то оно эквивалентно тому, что в каждой вершине матрица имеет индексы 0, 1, 2 и 3. В приведенном ниже примере кода используется метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) для включения индексированного смешения вершин.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Чтобы включить или отключить смешение вершин, установите для состояния отрисовки [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) значение, отличное от D3DRS \_ Disable из перечислимого типа [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Если для этого состояния рендеринга не задано значение D3DRS \_ Disable, необходимо передать необходимое число весов для каждой вершины. В следующем примере кода используется **IDirect3DDevice9:: сетрендерстате** для включения смешения вершин с тремя весовыми коэффициентами для каждой вершины.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Определение поддержки индексированного смешения вершин

Чтобы определить максимальный размер для матричной матрицы смешения вершин, проверьте элемент Максвертексблендматриксиндекс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . В приведенном ниже примере кода для получения этого размера используется метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Если значение, заданное в Максвертексблендматриксиндекс, равно 0, устройство не поддерживает индексированные матрицы.

> [!Note]  
> При использовании программной обработки вершин можно использовать матрицы 256 для индексированного смешения вершин с нормальным смешением или без них.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Передача индексов матрицы в Direct3D

Индексы в мировых матрицах можно передавать в Direct3D с помощью устаревших шейдеров вершин-ФВФ-или объявлений.

В приведенном ниже примере кода показано, как использовать устаревшие шейдеры вершин.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



Если используется устаревший шейдер вершин, индексы матрицы передаются вместе с позициями вершин с помощью \_ флагов КСИЗБН D3DFVF. Индексы матрицы передаются как байты внутри DWORD и должны присутствовать сразу после последнего веса вершины. Весовые коэффициенты вершин также передаются с помощью D3DFVF \_ ксизбн. Упакованный DWORD содержит index3, index2, index1 и index0, где index0 находится в наименьшем байте DWORD. Количество используемых индексов в мировом виде равно числу, переданному количеству матриц, используемых для смешения, как определено в [**D3DRS \_ вертексбленд**](./d3drenderstatetype.md).

При использовании объявления D3DVSDE \_ блендиндицес определяет входной регистр вершин для получения индексов матрицы. Индексы матрицы должны передаваться как D3DVSDT \_ UBYTE4.

В приведенном ниже примере кода показано, как использовать объявления. Обратите внимание, что порядок компонентов больше не важен, если не используется Вершинный шейдер с фиксированной функцией.

Ниже приведено описание вершины.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Ниже приведено соответствующее объявление регистра.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Наложение индексированных вершин](indexed-vertex-blending.md)
</dt> </dl>

 

 
