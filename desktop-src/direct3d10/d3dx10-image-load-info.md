---
description: При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. Значение D3DX10 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Структура D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713913"
---
# <a name="d3dx10_image_load_info-structure"></a>\_ \_ \_ Структура сведений о загрузке образа D3DX10

При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. Значение D3DX10 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Целевая Ширина текстуры. Если фактическая ширина текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую ширину.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Целевая Высота текстуры. Если фактическая высота текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую высоту.

</dd> <dt>

**Depth**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Глубина текстуры. Это относится только к текстурам томов.

</dd> <dt>

**фирстмиплевел**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Уровень mipmap наивысшего разрешения текстуры. Если это значение больше 0, после загрузки текстуры Фирстмиплевел будет сопоставлен с mipmap уровнем 0.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Максимальное число уровней mipmap, которое будет иметь текстура. Использование значения 0 или D3DX10 \_ по умолчанию приведет к созданию всей цепочки mipmap.

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **\_ Использование D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

Способ использования ресурса текстуры. См. раздел [**\_ Использование D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**биндфлагс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Этапы конвейера, к которым может быть привязана текстура. См. раздел [**\_ \_ флаг привязки D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**кпуакцессфлагс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Разрешения на доступ, которые будут иметь ЦП для ресурса текстуры. См. раздел [**\_ \_ \_ флаг доступа к ЦП D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

</dd> <dt>

**мискфлагс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Прочие свойства ресурсов (см. раздел [**D3D10 \_ Resource, \_ \_ флаг**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[ **\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Формат текстуры будет находиться после загрузки. См. раздел [**\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Фильтр**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Отфильтровать текстуру с помощью указанного фильтра (только при интерполяции). См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).

</dd> <dt>

**мипфилтер**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Фильтрация уровней MIP текстуры с помощью указанного фильтра (только при создании MIP-карты). Допустимые значения: D3DX10 \_ Filter \_ None, D3DX10 Filter \_ \_ , D3DX10 \_ \_ линейный фильтр или \_ треугольник фильтра D3DX10 \_ . См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).

</dd> <dt>

**псрЦинфо**
</dt> <dd>

Тип: **[ **\_ \_ сведения об образе D3DX10**](d3dx10-image-info.md)\***

</dd> <dd>

Сведения о исходном образе. См [**. \_ \_ сведения об образе D3DX10**](d3dx10-image-info.md). Можно получить с помощью [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)или [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

При инициализации структуры можно задать любой элемент D3DX10 \_ Default, и D3DX будет инициализировать его со значением по умолчанию из текстуры источника при загрузке текстуры.

Эта структура может использоваться интерфейсами API, которые:

-   Создайте ресурсы, такие как [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Создание обработчиков данных, таких как [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) или [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
