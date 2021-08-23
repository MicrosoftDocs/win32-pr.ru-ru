---
description: Определяет сведения о положении, текстуре и цвете спрайта.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Структура D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ec8b220d55d3ac55d2a8b68fa3b95398a395611da150235d03314114055214e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753514"
---
# <a name="d3dx10_sprite-structure"></a>\_Структура D3DX10 спрайта

Определяет сведения о положении, текстуре и цвете спрайта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>Члены

<dl> <dt>

**матворлд**
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Преобразование модели спрайта в мир. Определяет положение и ориентацию спрайта в мировом пространстве.

</dd> <dt>

**текскурд**
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Смещение от верхнего левого угла текстуры, указывающего, где в текстуре должно начинаться изображение спрайта. **Текскурд** находится в координатах текстуры.

</dd> <dt>

**текссизе**
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Вектор, содержащий ширину и высоту спрайта в координатах текстуры.

</dd> <dt>

**колормодулате**
</dt> <dd>

Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Цвет, который будет умножен до цвета пикселя перед отрисовкой.

</dd> <dt>

**птекстуре**
</dt> <dd>

Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Указатель на представление шейдера, представляющее текстуру спрайта. См. раздел [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

**текстуреиндекс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Индекс текстуры. Если Птекстуре не представляет массив текстуры, это значение должно быть равно 0.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
