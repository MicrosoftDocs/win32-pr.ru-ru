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
ms.openlocfilehash: 42b7669d974fffde76c8c8f1e7beb4f8d78bf58fda3810130b255d4bc5a693df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118684"
---
# <a name="id3dxeffectpool-interface"></a>Интерфейс ID3DXEffectPool

Приложения используют интерфейс **ID3DXEffectPool** для задания параметров, которые будут совместно использоваться различными эффектами. См. раздел Совместное использование параметров в [клонировании и совместном использовании (Direct3D 9)](cloning-and-sharing.md). У этого интерфейса нет методов.

## <a name="members"></a>Элементы

Интерфейс **ID3DXEffectPool** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="remarks"></a>Remarks

Интерфейс ID3DXEffectPool получается путем вызова [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

Тип LPD3DXEFFECTPOOL определяется как указатель на этот интерфейс.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
