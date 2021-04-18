---
title: Структура D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. | Структура D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO структура Direct3D 11
- Указатель структуры LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987206"
---
# <a name="d3dx11_image_load_info-structure"></a>\_ \_ \_ Структура сведений о загрузке образа D3DX11

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. Значение D3DX11 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Участники

<dl> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Целевая Ширина текстуры. Если фактическая ширина текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую ширину.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Целевая Высота текстуры. Если фактическая высота текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую высоту.

</dd> <dt>

**Depth**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Глубина текстуры. Это относится только к текстурам томов.

</dd> <dt>

**фирстмиплевел**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Уровень mipmap наивысшего разрешения текстуры. Если это значение больше 0, после загрузки текстуры Фирстмиплевел будет сопоставлен с mipmap уровнем 0.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Максимальное число уровней mipmap в текстуре. См. примечания в разделе [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Использование значения 0 или D3DX11 \_ по умолчанию приведет к созданию всей цепочки mipmap.

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **\_ Использование D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

Способ использования ресурса текстуры. См. раздел [**\_ Использование D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**биндфлагс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Этапы конвейера, к которым может быть привязана текстура. См. раздел [**\_ \_ флаг привязки D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**кпуакцессфлагс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Разрешения на доступ, которые будут иметь ЦП для ресурса текстуры. См. раздел [**\_ \_ \_ флаг доступа к ЦП D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**мискфлагс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Прочие свойства ресурсов (см. раздел [**D3D11 \_ Resource, \_ \_ флаг**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Перечисление [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , указывающее формат, в котором будет располагаться текстура после ее загрузки.

</dd> <dt>

**Фильтр**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Отфильтровать текстуру с помощью указанного фильтра (только при интерполяции). См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**мипфилтер**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Фильтрация уровней MIP текстуры с помощью указанного фильтра (только при создании MIP-карты). Допустимые значения: D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ , D3DX11 \_ \_ линейный фильтр или \_ треугольник фильтра D3DX11 \_ . См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**псрЦинфо**
</dt> <dd>

Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***

</dd> <dd>

Сведения о исходном образе. См [**. \_ \_ сведения об образе D3DX11**](d3dx11-image-info.md). Можно получить с помощью [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)или [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Примечания

При инициализации структуры можно задать любой элемент D3DX11 \_ Default, и D3DX будет инициализировать его со значением по умолчанию из текстуры источника при загрузке текстуры.

Эта структура может использоваться интерфейсами API, которые:

-   Создайте ресурсы, такие как [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Создание обработчиков данных, таких как [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) или [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

Значения по умолчанию:


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Ниже приведен краткий пример, в котором эта структура используется для предоставления формата пикселей при загрузке текстуры. Полный код см. в разделе HDRFormats10. cpp в [примере HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

