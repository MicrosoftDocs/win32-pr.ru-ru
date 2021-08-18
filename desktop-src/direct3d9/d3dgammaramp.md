---
description: Содержит красную, зеленую и синюю данные пандуса.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Структура D3DGAMMARAMP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fbd3acc35b7fd4998f5ba536c1fe4a28cf2a17153bf24aacde1f9f39bbbcd09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751004"
---
# <a name="d3dgammaramp-structure"></a>Структура D3DGAMMARAMP

Содержит красную, зеленую и синюю данные пандуса.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Члены

<dl> <dt>

**отмечен**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Массив элементов WORD 256, описывающих красный цвет гаммы.

</dd> <dt>

**зеленого**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Массив элементов WORD 256, описывающий зеленый цвет гаммы.

</dd> <dt>

**выделен**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Массив элементов WORD 256, описывающих синюю гамму цветов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**жетгаммарамп**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**сетгаммарамп**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
