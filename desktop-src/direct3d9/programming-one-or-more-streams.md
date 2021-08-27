---
description: В этом разделе описываются шейдеры, которые можно использовать для программируемой модели потока.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: программирование одного или нескольких Потоки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92440abfb6e343bdd3440f5608d6446c0390b1271e5c4c6686a3a46e578476ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118604"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>программирование одного или нескольких Потоки (Direct3D 9)

В этом разделе описываются шейдеры, которые можно использовать для программируемой модели потока.

## <a name="using-streams"></a>использование Потоки

В DirectX 8 представлено понятие потока для привязки данных к входным регистрам для использования шейдерами. Поток — это универсальный массив данных компонента, каждый компонент которого состоит из одного или нескольких элементов, представляющих одну сущность, такую как «расположение», «нормальный», «цвет» и т. д. Потоки включить графические микросхемы для параллельного доступа к памяти из нескольких буферов вершин, а также обеспечить более естественное сопоставление данных приложения. Они также позволяют использовать тривиальные многотекстурные и многопроходные. Его следует рассматривать следующим образом:

-   Вершина состоит из n потоков.
-   Поток состоит из элементов m.
-   Элемент — это \[ положение, цвет, нормальная Координата текстуры \] .

Метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api) привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки. Фактические ссылки на потоковые данные не выполняются до тех пор, пока не будет вызван метод рисования, например [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Сопоставление входных элементов вершины с входными регистрами вершин для программируемых шейдеров вершин определяется в объявлении шейдера, но входные элементы вершины не имеют определенной семантики их использования. Интерпретация входных элементов вершин программируется с помощью инструкций шейдера. Функция шейдера вершин определяется массивом инструкций, которые применяются к каждой вершине. Выходные регистры вершин явным образом записываются в, используя инструкции в функции шейдера.

Тем не менее, в этом обсуждении стоит меньше внимания на семантической сопоставлении элементов для регистрации и, что более важно для использования потоков и проблемы, решаемой с помощью потоков. Основное преимущество потоков заключается в том, что они удаляют затраты на вершину данных, ранее связанные с многотекстурной обсчетом. Перед потоками пользователь должен был либо дублировать наборы данных вершин, чтобы обрабатывать одиночный и многотекстурный регистр без неиспользуемых элементов данных, либо содержать элементы данных, которые не будут использоваться, за исключением многотекстурного случая.

Ниже приведен пример использования двух наборов данных вершин: один для одной текстуры и один для многотекстурного.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Альтернативой было наличие одного элемента вершины, содержащего оба набора координат текстуры.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



При использовании этих данных вершин только одна копия данных о положении и цвете переносится в память, за счет того, что оба набора координат текстуры обрабатываются для отрисовки даже в одном случае текстуры.

Теперь, когда компромисс понятен, потоки предоставляют элегантное исправление для этого дилеммой. Ниже приведен набор определений вершин для поддержки трех потоков: один с положением и цветом, один с первым набором координат текстуры, а второй — со вторым набором координат текстуры.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



Объявление вершины будет выглядеть следующим образом:


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



Теперь создайте объект объявления вершины и задайте его, как показано ниже.


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Примеры комбинаций

### <a name="one-stream-diffuse-color"></a>Один поток рассеянный цвет

Объявления вершин и параметры потока для рендеринга рассеянного цвета будут выглядеть следующим образом:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>два Потоки с цветом и текстурой

Объявления вершин и параметры потока для отрисовки одной текстуры будут выглядеть следующим образом:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>два Потоки с цветом и двумя текстурами

Объявления вершин и параметры потока для отрисовки с несколькими текстурами будут выглядеть следующим образом:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



В каждом случае достаточно [**:D IDirect3DDevice9ного вызова равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Это показывает гибкость потоков в решении проблемы дублирования данных и избыточной передачи данных по шине (то есть расход полосы пропускания).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объявление вершины](vertex-declaration.md)
</dt> </dl>

 

 
