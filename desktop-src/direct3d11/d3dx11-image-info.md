---
title: Структура D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. | Структура D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO структура Direct3D 11
- Указатель структуры LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987209"
---
# <a name="d3dx11_image_info-structure"></a>\_ \_ Структура сведений об ОБРАЗе D3DX11

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. Значение D3DX11 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
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

**ArraySize**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Количество элементов в массиве.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Максимальное число уровней mipmap в текстуре. См. примечания в разделе [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Использование значения 0 или D3DX11 \_ по умолчанию приведет к созданию всей цепочки mipmap.

</dd> <dt>

**мискфлагс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Различные свойства ресурсов, заданные с помощью флага [**D3D11 \_ ресурса " \_ \_ Прочие**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ".

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Перечисление [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , определяющее формат, в котором текстура будет находиться после загрузки.

</dd> <dt>

**ресаурцедименсион**
</dt> <dd>

Тип: **[ **D3D11 \_ ресурс \_ измерение**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Значение [**\_ \_ измерения ресурса D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , которое определяет тип ресурса.

</dd> <dt>

**имажефилеформат**
</dt> <dd>

Тип: **[ **D3DX11 \_ image \_ File \_ Format**](d3dx11-image-file-format.md)**

</dd> <dd>

Значение [**\_ \_ \_ формата файла изображения D3DX11**](d3dx11-image-file-format.md) , определяющее формат изображения.

</dd> </dl>

## <a name="remarks"></a>Примечания

Эта структура используется такими методами, как: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)или [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

