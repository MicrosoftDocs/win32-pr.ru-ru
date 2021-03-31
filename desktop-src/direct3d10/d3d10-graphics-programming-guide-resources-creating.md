---
description: Создание буферов требует определения данных, которые будут храниться в буфере, предоставления данных инициализации и настройки соответствующих флагов использования и привязки. Сведения о создании текстур см. в разделе Создание ресурсов текстуры (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Создание ресурсов буфера (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807535"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Создание ресурсов буфера (Direct3D 10)

Создание буферов требует определения данных, которые будут храниться в буфере, предоставления данных инициализации и настройки соответствующих флагов использования и привязки. Сведения о создании текстур см. в разделе [Создание ресурсов текстуры (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Создание буфера вершин](#create-a-vertex-buffer)
    -   [Создание описания буфера](#create-a-buffer-description)
    -   [Создание данных инициализации для буфера](#create-the-initialization-data-for-the-buffer)
    -   [Создание буфера](#create-the-buffer)
-   [Создание буфера индекса](#create-an-index-buffer)
-   [Создание буфера констант](#create-a-constant-buffer)
-   [См. также](#related-topics)

## <a name="create-a-vertex-buffer"></a>Создание буфера вершин

Ниже приведены шаги по созданию [буфера вершин](d3d10-graphics-programming-guide-resources-types.md) .

-   [Создание описания буфера](#create-a-buffer-description)
-   [Создание данных инициализации для буфера](#create-the-initialization-data-for-the-buffer)
-   [Создание буфера](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Создание описания буфера

При создании буфера вершин описание буфера (см. [**D3D10 \_ buffer \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) используется для определения того, как данные организованы в буфере, как конвейер может получить доступ к буферу и как будет использоваться буфер.

В следующем примере показано, как создать описание буфера для одного треугольника с вершинами, содержащими значения позиций и цветов.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



В этом примере описание буфера инициализируется почти всеми параметрами по умолчанию для [**использования**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**доступа ЦП**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) и [**прочих флагов**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag). Другие параметры предназначены для [**флага привязки**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) , который определяет ресурс как буфер вершин и размер буфера.

Флаги использования и доступа к ЦП важны для повышения производительности. Эти два флага вместе определяют частоту доступа к ресурсу, тип памяти, в которую может быть загружен ресурс, и то, какой процессор должен получить доступ к ресурсу. Использование по умолчанию этот ресурс не будет обновляться очень часто. Установка значения "доступ ЦП" равным 0 означает, что ЦП не должен считывать или записывать ресурс. В сочетании это означает, что среда выполнения может загрузить ресурс в наиболее производительную память для GPU, так как ресурс не требует доступа к ЦП.

Как и ожидалось, существует компромисс между оптимальной производительностью и любым уровнем доступности любого из процессоров. Например, использование по умолчанию без доступа к ЦП означает, что ресурс можно сделать доступным только для GPU. Это может включать загрузку ресурса в память, не доступную напрямую ЦП. Ресурс можно изменить только с помощью [**упдатесубресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).

### <a name="create-the-initialization-data-for-the-buffer"></a>Создание данных инициализации для буфера

Буфер — это просто коллекция элементов, которая располагается в виде массива 1D. В результате одновременное прорезание системной памяти и шаг среза системной памяти одинаковы. Размер объявления данных вершин. Приложение может предоставлять данные инициализации при создании буфера с помощью [**описания подресурса**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), которое содержит указатель на фактические данные ресурса и содержит сведения о размере и структуре этих данных.

Любой буфер, созданный с неизменяемым использованием (см. раздел [**D3D10 \_ Usage \_ unmutable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)), должен быть инициализирован во время создания. Буферы, использующие любой из других флагов использования, могут быть обновлены после инициализации с помощью [**копиресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**кописубресаурцерегион**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)и [**упдатесубресаурце**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)или доступа к его базовой памяти с помощью метода [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .

### <a name="create-the-buffer"></a>Создание буфера

Используя описание буфера и данные инициализации (необязательно), вызовите [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) , чтобы создать буфер вершин. В следующем фрагменте кода показано, как создать буфер вершин из массива данных вершин, объявленных приложением.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Создание буфера индекса

Создание буфера индекса очень похоже на создание буфера вершин; с двумя различиями. Буфер индексов содержит только 16-разрядные или 32-разрядные данные (вместо широкого диапазона форматов, доступных для буфера вершин. Буфер индексов также требует наличия флага привязки index-buffer.

В следующем примере показано, как создать буфер индекса из массива данных индекса.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Создание буфера констант

В Direct3D 10 появился буфер констант. Буфер константы или буфер констант шейдера — это буфер, содержащий константы шейдера. Ниже приведен пример создания буфера констант, взятого из [примера HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Обратите внимание, что при использовании интерфейса [**интерфейса ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) процесс создания, привязки и передачи постоянного буфера обрабатывается экземпляром **интерфейса ID3D10Effect** . В этом случае можно только получить переменную из воздействия с помощью одного из методов несцесари, таких как [**жетвариаблебинаме**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , и обновить переменную с помощью одного из методов SetVariable, таких как [**сетматрикс**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Пример использования **интерфейса ID3D10Effect** для управления буфером констант см. в [руководстве 7. Сопоставление текстур и буферы констант](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ресурсы (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



