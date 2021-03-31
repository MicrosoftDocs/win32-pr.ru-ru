---
description: Ресурс текстуры — это структурированная коллекция данных.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Создание ресурсов текстуры (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990605"
---
# <a name="creating-texture-resources-direct3d-10"></a>Создание ресурсов текстуры (Direct3D 10)

Ресурс [текстуры](d3d10-graphics-programming-guide-resources-types.md) — это структурированная коллекция данных. Обычно значения цвета хранятся в текстурах и доступны во время отрисовки [конвейера](d3d10-graphics-programming-guide-pipeline-stages.md) на различных этапах для входа и выхода. Создание текстур и определение того, как они будут использоваться, — важная часть визуализации интересных сцен в Direct3D 10.

Несмотря на то, что текстуры обычно содержат сведения о цвете, создание текстур с помощью различных [**\_ форматов DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) позволяет им хранить различные типы данных. Эти данные можно затем использовать в конвейере Direct3D 10 в нетрадиционных способах.

Все текстуры имеют ограничения на объем используемой памяти и количество пикселей текстуры, которые они содержат. Эти ограничения задаются [константами ресурсов](d3d10-graphics-reference-resource-constants.md).

-   [Создание текстуры из файла](#create-a-texture-from-a-file)
    -   [Создание текстуры и представления отдельно](#create-texture-and-view-separately)
    -   [Одновременное создание текстур и представлений](#create-texture-and-view-simultaneously)
-   [Создание пустых текстур](#creating-empty-textures)
    -   [Подготовка к отображению текстуры](#rendering-to-a-texture)
    -   [Заполнение текстур вручную](#filling-textures-manually)
-   [Несколько Рендертаржетс](#multiple-rendertargets)
-   [См. также](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Создание текстуры из файла

> [!Note]  
> [Библиотека служебной программы D3DX](d3d10-graphics-reference-d3dx10.md) устарела для Windows 8 и не поддерживается для приложений Магазина Windows.

 

При создании текстуры в Direct3D 10 необходимо также создать [представление](d3d10-graphics-programming-guide-resources-access-views.md). Представление — это объект, сообщающий устройству, как осуществляется доступ к текстуре во время подготовки к просмотру. Самый распространенный способ доступа к текстуре — чтение из него с помощью [шейдера](../direct3dhlsl/dx-graphics-hlsl.md). Представление ресурсов шейдера покажет шейдеру способ чтения из текстуры во время подготовки к просмотру. Вид представления, который будет использоваться текстурой, должен быть указан при его создании.

Создание текстуры и загрузка исходных данных можно выполнить двумя разными способами: создать текстуру и представление отдельно или одновременно создать текстуру и представление. API предоставляет обе методики, что позволяет выбрать подходящий вариант.

### <a name="create-texture-and-view-separately"></a>Создание текстуры и представления отдельно

Самый простой способ создать текстуру — загрузить ее из файла изображения. Чтобы создать текстуру, просто заполните одну структуру и укажите имя текстуры [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



Функция D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) выполняет три вещи: сначала создается объект текстуры Direct3D 10. Во вторых, он считывает входной файл изображения. в третьих, данные изображения сохраняются в объекте текстуры. В приведенном выше примере загружается файл BMP, но функция может загружать различные типы файлов.

Флаг привязки указывает, что текстура будет создана как ресурс шейдера, что позволяет этапу шейдера считывать из текстуры во время отрисовки.

В приведенном выше примере не указаны все параметры загрузки. На самом деле, часто бывает полезно просто обнулить параметры загрузки, так как это позволяет D3DX выбирать соответствующие значения на основе входного изображения. Если вы хотите, чтобы входной образ определил все параметры, с которыми создается текстура, просто укажите **значение NULL** для параметра **лоадинфо** следующим образом:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



Указание **значения NULL** для сведений о загрузке является простым, но мощным ярлыком.

Теперь, когда текстура создана, необходимо создать представление шейдера, чтобы текстуру можно было привязать как входные данные для шейдера. Поскольку [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) возвращает указатель на ресурс, а не указатель на текстуру, необходимо определить точный тип ресурса, который был загружен, а затем создать представление "шейдер-ресурс" с помощью [**креатешадерресаурцевиев**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Хотя в приведенном выше примере создается 2D-представление ресурсов, код для создания других типов представлений ресурсов шейдера очень похож. Теперь любой этап шейдера может использовать эту текстуру в качестве входных данных.

Использование [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**креатешадерресаурцевиев**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) для создания текстуры и связанного с ней представления — один из способов подготовки текстуры к привязке к этапу шейдера. Другой способ сделать это — создать одновременно текстуру и ее представление, что рассматривается в следующем разделе.

### <a name="create-texture-and-view-simultaneously"></a>Одновременное создание текстур и представлений

Для считывания из текстуры во время выполнения Direct3D 10 требуется как текстура, так и шейдер — представление ресурсов. Так как создание текстуры и представления шейдера — это типичная задача, D3DX предоставляет [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) для вас.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



При одном вызове D3DX создаются и текстура, и шейдер-представление ресурсов. Функции параметра **лоадинфо** не изменяются; его можно использовать для настройки способа создания текстуры или получения необходимых параметров из входного файла, указав **значение NULL** для параметра **лоадинфо** .

Объект [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) , возвращаемый функцией [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) , можно впоследствии использовать для получения исходного интерфейса [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) , если он необходим. Это можно [**сделать, вызвав метод метода**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) WebMethod.

D3DX предоставляет единую функцию для создания текстуры и представления шейдеров в виде конвиениенце; Вы решаете решить, какой метод создания текстуры и представления лучше удовлетворять потребностям вашего приложения.

Теперь, когда вы узнали, как создать текстуру и ее представление шейдеров, в следующем разделе будет показано, как можно выполнить выборку (чтение) из текстуры с помощью шейдера.

## <a name="creating-empty-textures"></a>Создание пустых текстур

Иногда приложения хотят создать текстуру и вычислить данные, которые будут храниться в текстуре, или использовать графический [конвейер](d3d10-graphics-programming-guide-pipeline-stages.md) для визуализации в эту текстуру, а затем использовать результаты в другой обработке. Эти текстуры могут быть обновлены графическим конвейером или самим приложением, в зависимости от того, какой тип [**использования**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) был указан для текстуры при ее создании.

### <a name="rendering-to-a-texture"></a>Подготовка к отображению текстуры

Наиболее распространенным случаем создания пустой текстуры для заполнения данными во время выполнения является ситуация, когда приложению требуется выполнить отрисовку на текстуру, а затем использовать результаты операции визуализации в последующем проходе. Текстуры, созданные с этой целью, должны указывать [**Использование**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)по умолчанию.

В следующем примере кода создается пустая текстура, которую конвейер может визуализировать и впоследствии использовать в качестве входных данных для [шейдера](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



Для создания текстуры приложение должно указать некоторые сведения о свойствах, которые будет иметь текстура. Ширина и высота текстуры в пикселей текстуры заданы как 256. Для этого целевого объекта рендеринга требуется только один уровень mipmap. Требуется только один целевой объект рендеринга, поэтому размер массива устанавливается равным 1. Каждый шаг текселя содержит 4 32-разрядные значения с плавающей запятой, которые можно использовать для хранения очень точной информации (см. [**\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Необходимо всего один пример на пиксель. Для использования задано значение по умолчанию, так как это позволяет наиболее эффективно размещать целевой объект отрисовки в памяти. Наконец, тот факт, что текстура будет привязана в качестве целевого объекта отрисовки и указан ресурс шейдера в разные моменты времени.

Текстуры невозможно привязать для отрисовки в конвейере напрямую; Используйте представление целевого объекта визуализации, как показано в следующем примере кода.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



Формат представления «рендеринг-целевой объект» просто устанавливается в формат исходной текстуры. Информация в ресурсе должна интерпретироваться как двухмерная текстура, и мы хотим использовать только первый уровень mipmap целевого объекта рендеринга.

Аналогично тому, как должно быть создано представление визуализации целевого объекта, чтобы целевой объект отрисовки мог быть привязан к потоку вывода в конвейере, необходимо создать представление шейдера, чтобы целевой объект отрисовки можно было привязать к конвейеру в качестве входных данных. Это показано в следующем образце кода.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



Параметры описаний представления "шейдер-представление ресурсов" очень похожи на описания представления целевого объекта визуализации и были выбраны по тем же причинам.

### <a name="filling-textures-manually"></a>Заполнение текстур вручную

Иногда приложения хотели бы вычислять значения во время выполнения, поместив их в текстуру вручную, а затем, чтобы графический [конвейер](d3d10-graphics-programming-guide-pipeline-stages.md) использовал эту текстуру в последующих операциях визуализации. Для этого приложение должно создать пустую текстуру таким образом, чтобы ЦП может получить доступ к базовой памяти. Это делается путем создания динамической текстуры и получения доступа к базовой памяти путем вызова определенного метода. В следующем образце кода показано, как это сделать.


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Обратите внимание, что для формата задано значение 32 бит на пиксель, где каждый компонент определен 8 битами. Параметр Usage имеет значение Dynamic, тогда как флаги привязки настроены на указание текстуры, к которой будет обращаться шейдер. Оставшаяся часть описания текстуры аналогична созданию целевого объекта рендеринга.

Вызов [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) позволяет приложению получить доступ к базовой памяти текстуры. Полученный указатель используется для заполнения текстурой данными. Это можно увидеть в следующем примере кода.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Несколько Рендертаржетс

До восьми представлений представления подготовки к просмотру может быть привязано к конвейеру за раз (с [**омсетрендертаржетс**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Для каждого пикселя (или каждого образца при включенной множественной выборки) смешивание выполняется независимо для каждого представления целевого объекта рендеринга. Две переменные состояния смешения — Бленденабле и Рендертаржетвритемаск — массивы из восьми, каждый элемент массива соответствует представлению целевого объекта визуализации. При использовании нескольких целевых объектов рендеринга каждый целевой объект отрисовки должен иметь один и тот же [тип ресурса](d3d10-graphics-programming-guide-resources-types.md) (буфер, текстура 1d, массив 2D-текстуры и т. д.) и иметь одинаковое измерение (ширину, высоту, глубину для трехмерных текстур и размер массива для массивов текстуры). Если целевые объекты отрисовки являются многовыборочными, то все они должны иметь одинаковое количество выборок на пиксель.

Активным может быть только один буфер трафарета глубины, независимо от того, сколько активных объектов рендеринга активно. При использовании массивов текстуры в качестве целевых объектов рендеринга все измерения представления должны совпадать. Целевые объекты рендеринга не должны иметь одинаковый формат текстуры.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ресурсы (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
