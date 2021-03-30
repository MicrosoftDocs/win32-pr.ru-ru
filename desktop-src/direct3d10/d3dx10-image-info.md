---
description: Возвращает описание исходного содержимого файла изображения.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Структура D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354440"
---
# <a name="d3dx10_image_info-structure"></a>\_ \_ Структура сведений об ОБРАЗе D3DX10

Возвращает описание исходного содержимого файла изображения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина исходного изображения в пикселях.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота исходного изображения в пикселях.

</dd> <dt>

**Depth**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Глубина исходного изображения в пикселях.

</dd> <dt>

**ArraySize**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер массива текстуры. *Размера массива* будет иметь значение 1 для одного образа.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число уровней mipmap в исходном изображении.

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

Значение из перечислимого типа в [**\_ формате DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , которое наиболее точно описывает данные в исходном изображении.

</dd> <dt>

**ресаурцедименсион**
</dt> <dd>

Тип: **[ **D3D10 \_ ресурс \_ измерение**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Представляет тип текстуры, хранящейся в файле. См. раздел [**\_ \_ измерение ресурсов D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**имажефилеформат**
</dt> <dd>

Тип: **[ **D3DX10 \_ image \_ File \_ Format**](d3dx10-image-file-format.md)**

</dd> <dd>

Представляет формат файла изображения. См. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
