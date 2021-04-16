---
description: Запрашивает освобождение объекта контейнера сетки.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: 'ID3DXAllocateHierarchy: метод:D Естроймешконтаинер (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548119"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>ID3DXAllocateHierarchy: метод:D Естроймешконтаинер

Запрашивает освобождение объекта контейнера сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешконтаинертофри* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Указатель на объект контейнера сетки, который будет освобожден.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




