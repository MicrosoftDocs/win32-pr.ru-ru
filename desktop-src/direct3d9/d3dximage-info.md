---
description: Структура D3DXIMAGE_INFO — Возвращает описание исходного содержимого файла изображения.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Структура D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090542"
---
# <a name="d3dximage_info-structure"></a>\_Структура сведений о D3DXIMAGE

Возвращает описание исходного содержимого файла изображения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
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

**Глубина**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Глубина исходного изображения в пикселях.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число уровней MIP в исходном изображении.

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Значение из перечислимого типа [D3DFORMAT](d3dformat.md) , которое наиболее точно описывает данные в исходном изображении.

</dd> <dt>

**ResourceType**
</dt> <dd>

Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Представляет тип текстуры, хранящейся в файле. Это либо D3DRTYPEная \_ текстура, D3DRTYPE \_ волуметекстуре, либо D3DRTYPE \_ кубетекстуре.

</dd> <dt>

**имажефилеформат**
</dt> <dd>

Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

</dd> <dd>

Представляет формат файла изображения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
