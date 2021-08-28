---
description: С учетом сцены, содержащей много объектов, использующих одну геометрию, можно нарисовать множество экземпляров этой геометрии с различными ориентациями, размерами, цветами и т. д. Благодаря значительному повышению производительности, уменьшая объем данных, необходимых для модуля подготовки отчетов.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Эффективная прорисовка нескольких экземпляров геометрии (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70586142b58076e5010083f61aeff360aa245a298e5d010fb487aed8b5843ec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122379"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Эффективная прорисовка нескольких экземпляров геометрии (Direct3D 9)

С учетом сцены, содержащей много объектов, использующих одну геометрию, можно нарисовать множество экземпляров этой геометрии с различными ориентациями, размерами, цветами и т. д. Благодаря значительному повышению производительности, уменьшая объем данных, необходимых для модуля подготовки отчетов.

Это можно сделать с помощью двух методов: первый для рисования индексированной геометрии и второй для неиндексированной геометрии. Оба метода используют два буфера вершин: один для предоставления геометрических данных, а другой — для передачи данных экземпляра каждого объекта. Данные экземпляра могут представлять собой широкий спектр сведений, таких как преобразование, цветовые данные или освещение данных, в основном все, что можно описать в объявлении вершины. Рисование большого количества экземпляров геометрии с помощью этих методов может значительно сократить объем данных, отправляемых в модуль подготовки отчетов.

-   [Рисование индексированной геометрии](#drawing-indexed-geometry)
    -   [Сравнение производительности индексированных геометрических объектов](#indexed-geometry-performance-comparison)
-   [Рисование неиндексированной геометрии](#drawing-non-indexed-geometry)
    -   [Сравнение производительности неиндексированных геометрических объектов](#non-indexed-geometry-performance-comparison)
-   [Связанные темы](#related-topics)

## <a name="drawing-indexed-geometry"></a>Рисование индексированной геометрии

Буфер вершин содержит данные по вершинам, определяемые объявлением вершины. Предположим, что часть каждой вершины содержит геометрические данные, а часть каждой вершины содержит данные экземпляра для каждого объекта, как показано на следующей схеме.

![схема буфера вершин для индексированной геометрии](images/drawingmultipleinstances.png)

Для этого способа требуется устройство, которое поддерживает 3 \_ 0 модель шейдера вершин. Этот метод работает с любым программируемым шейдером, но не с фиксированным конвейером функций.

Для буферов вершин, показанных выше, приведены соответствующие объявления буфера вершин:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Эти объявления определяют два буфера вершин. Первое объявление (для потока 0, обозначенное нулями в столбце 1) определяет геометрические данные, состоящие из: положение, нормаль, тангенс, бинормал и данные координаты текстуры.

Второе объявление (для потока 1, обозначенное элементами в столбце 1) определяет данные экземпляра для каждого объекта. Каждый экземпляр определяется с помощью числа с плавающей запятой 4 4 компонентов и цвета из четырех компонентов. Первые четыре значения можно использовать для инициализации матрицы 4x4, что означает, что эти данные будут иметь уникальный размер, расположение и поворот каждого экземпляра геометрии. Первые четыре компонента используют семантику координат текстуры, которая, в данном случае, означает, что это общее 4-компонентное число. При использовании произвольных данных в объявлении вершины используйте семантику координат текстуры, чтобы пометить ее. Последний элемент в потоке используется для цветовых данных. Это можно применить в шейдере вершин, чтобы присвоить каждому экземпляру уникальный цвет.

Перед отрисовкой необходимо вызвать [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) , чтобы привязать потоки буфера вершин к устройству. Ниже приведен пример, в котором привязываются как буферы вершин:


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**Сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) использует [D3DSTREAMSOURCE \_ индекседдата](other-direct3d-constants.md) для обнаружения индексированных геометрических данных. В этом случае Stream 0 содержит индексированные данные, описывающие геометрию объекта. Это значение логически объединяется с числом экземпляров геометрии для рисования.

Обратите внимание, что D3DSTREAMSOURCE \_ индекседдата и количество экземпляров для рисования всегда должны быть заданы в потоке 0.

Во втором вызове [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) использует [D3DSTREAMSOURCE \_ инстанцедата](other-direct3d-constants.md) для обнаружения потока, содержащего данные экземпляра. Это значение логически объединяется с 1, так как каждая вершина содержит один набор данных экземпляра.

Последние два вызова [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывают указатели буфера вершин к устройству.

После завершения подготовки к просмотру данных экземпляра убедитесь, что частота потока вершин сброшена обратно в состояние по умолчанию (что не использует создание экземпляров). Так как в этом примере используются два потока, установите оба потока, как показано ниже:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Сравнение производительности индексированных геометрических объектов

Хотя невозможно выполнить одно заключение о том, насколько этот метод может сократить время визуализации в каждом приложении, учитывайте разницу в объеме потоковых данных в среде выполнения и количестве изменений состояния, которые будут сокращены при использовании метода создания экземпляров. Эта последовательность визуализации использует преимущества рисования нескольких экземпляров одной и той же геометрии:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Обратите внимание, что цикл визуализации вызывается один раз, данные геометрии передаются в потоке, а n экземпляров — в потоковой передаче один раз. Следующая последовательность отображения идентична функциональности, но не использует преимущества создания экземпляров:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Обратите внимание, что весь цикл рендеринга упаковывается вторым циклом для рисования каждого объекта. Теперь геометрические данные передаются в модуль подготовки отчетов n раз (вместо одного раза), а все состояния конвейера также могут быть установлены избыточно для каждого рисуемого объекта. Эта последовательность отображения, скорее всего, будет значительно ниже. Обратите внимание, что параметры [**дравиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) не изменились между двумя циклами отрисовки.

## <a name="drawing-non-indexed-geometry"></a>Рисование неиндексированной геометрии

При [рисовании индексированной геометрии](#drawing-indexed-geometry)буферы вершин были настроены для рисования нескольких экземпляров индексированной геометрии с большей эффективностью. Для рисования неиндексированной геометрии можно также использовать [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) . Для этого требуется другой макет буфера вершин и другие ограничения. Чтобы нарисовать неиндексированную геометрию, подготовьте буферы вершин, как на следующей схеме.

![схема буфера вершин для неиндексированной геометрии](images/olderstyleinstancing.png)

Этот метод не поддерживается аппаратным ускорением на любом устройстве. Она поддерживается только при обработке вершин программного обеспечения и будет работать только с шейдерами [VS \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .

Поскольку этот метод работает с неиндексированной геометрией, буфер индекса отсутствует. Как показано на схеме, буфер вершин, содержащий геометрию, содержит n копий геометрических данных. Для каждого рисуемого экземпляра данные геометрии считываются из первого буфера вершин, а данные экземпляра считываются из второго буфера вершин.

Ниже приведены соответствующие объявления буфера вершин.


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Эти объявления идентичны объявлениям, выполненным в примере индексированной геометрии. Опять же, первое объявление (для потока 0) определяет геометрические данные, а второе объявление (для потока 1) определяет данные экземпляра для каждого объекта. При создании первого буфера вершин обязательно загрузите его с числом экземпляров геометрических данных, которые будут изображены.

Перед отрисовкой необходимо настроить разделитель, который сообщает среде выполнения о том, как разделить первый буфер вершин на n экземпляров. Затем установите разделитель с помощью [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) следующим образом:


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



Первый вызов [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) говорит, что поток 0 содержит n экземпляров m вершин. Затем [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывает поток 0 к буферу вершинной геометрии.

Во втором вызове [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) определяет поток 1 в качестве источника данных экземпляра. Вторым параметром является количество вершин в каждом объекте (m). Помните, что поток данных экземпляра должен всегда объявляться как второй поток. Затем [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывает поток 1 к буферу вершин, содержащему данные экземпляра.

После завершения подготовки к просмотру данных экземпляра убедитесь, что частота потока вершин сброшена обратно в состояние по умолчанию. Так как в этом примере используются два потока, установите оба потока, как показано ниже:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Сравнение производительности неиндексированных геометрических объектов

Основным преимуществом этого стиля создания экземпляров является то, что его можно использовать для неиндексированной геометрии. Хотя невозможно выполнить одно заключение о том, насколько этот метод может сократить время визуализации в каждом приложении, рассмотрите разницу в объеме потоковых данных в среде выполнения и количестве изменений состояния, которые будут сокращены для следующей последовательности визуализации:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Обратите внимание, что цикл визуализации вызывается один раз. Геометрические данные передаются по потоковой передаче один раз, хотя для потоковой передачи существует n экземпляров геометрических объектов. Данные из буфера вершин экземпляра передаются в потоковую передачу один раз. Следующая последовательность отображения идентична функциональности, но не использует преимущества создания экземпляров:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Без создания экземпляров для рисования каждого объекта цикл визуализации должен быть заключен во второй цикл. Устраняя второй цикл рендеринга, следует рассчитывать на лучшую производительность из-за меньшего количества изменений состояния визуализации, которые вызываются внутри цикла.

В целом, разумно рассчитывать на то, что индексированный метод ([Рисование индексированной геометрии](#drawing-indexed-geometry)) будет работать лучше, чем неиндексированный метод ([Рисование неиндексированной геометрии](#drawing-non-indexed-geometry)), так как индексированный метод выполняет только потоковую передачу только одной копии данных геометрии. Обратите внимание, что параметры для [**дравиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) не изменялись для всех последовательностей отрисовки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Дополнительные разделы](advanced-topics.md)
</dt> <dt>

[Пример создания экземпляров](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
