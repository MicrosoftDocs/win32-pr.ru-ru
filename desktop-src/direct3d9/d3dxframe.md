---
description: Инкапсулирует кадр преобразования в иерархии фрейма преобразования.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Структура D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273778"
---
# <a name="d3dxframe-structure"></a>Структура D3DXFRAME

Инкапсулирует кадр преобразования в иерархии фрейма преобразования.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Члены

<dl> <dt>

**Name**
</dt> <dd>

Тип: **LPSTR**

</dd> <dd>

Имя кадра.

</dd> <dt>

**трансформатионматрикс**
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Матрица преобразования.

</dd> <dt>

**пмешконтаинер**
</dt> <dd>

Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Указатель на контейнер сетки.

</dd> <dt>

**пфрамесиблинг**
</dt> <dd>

Тип: * * * * D3DXFRAME **\***

</dd> <dd>

Указатель на одноуровневый фрейм.

</dd> <dt>

**пфрамефирстчилд**
</dt> <dd>

Тип: * * * * D3DXFRAME **\***

</dd> <dd>

Указатель на дочерний фрейм.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Приложение может быть производным от этой структуры для добавления других данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




