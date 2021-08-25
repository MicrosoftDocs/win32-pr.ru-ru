---
description: Параметры переноса текстур для API-интерфейсов вычисления ИМТ.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: Перечисление ФЛАГов D3DXIMT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3209021b73bc9d17f43386d7df85082887a76600540c44955c41228da3d17379
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857024"
---
# <a name="d3dximt-flags-enumeration"></a>Перечисление ФЛАГов D3DXIMT

Параметры переноса текстур для API-интерфейсов вычисления ИМТ.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT в \_ оболочке \_ U**
</dt> <dd>

Текстура переносится в сторону U.

</dd> <dt>

<span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ переносить \_ V**
</dt> <dd>

Текстура переносится в направлении V.

</dd> <dt>

<span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ переносить \_ UV**
</dt> <dd>

Текстура переносится в обоих направлениях.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[**D3DXComputeIMTFromPerTexelSignal**](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[**D3DXComputeIMTFromPerVertexSignal**](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




