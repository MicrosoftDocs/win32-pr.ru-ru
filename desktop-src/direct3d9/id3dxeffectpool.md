---
description: Приложения используют интерфейс ID3DXEffectPool для задания параметров, которые будут совместно использоваться различными эффектами. См. раздел Совместное использование параметров в клонировании и совместном использовании (Direct3D 9). У этого интерфейса нет методов.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Интерфейс ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424338"
---
# <a name="id3dxeffectpool-interface"></a>Интерфейс ID3DXEffectPool

Приложения используют интерфейс **ID3DXEffectPool** для задания параметров, которые будут совместно использоваться различными эффектами. См. раздел Совместное использование параметров в [клонировании и совместном использовании (Direct3D 9)](cloning-and-sharing.md). У этого интерфейса нет методов.

## <a name="members"></a>Элементы

Интерфейс **ID3DXEffectPool** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="remarks"></a>Комментарии

Интерфейс ID3DXEffectPool получается путем вызова [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

Тип LPD3DXEFFECTPOOL определяется как указатель на этот интерфейс.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
