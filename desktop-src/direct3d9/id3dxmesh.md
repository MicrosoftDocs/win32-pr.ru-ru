---
description: Приложения используют методы интерфейса ID3DXMesh для управления объектами сетки.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Интерфейс ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355713"
---
# <a name="id3dxmesh-interface"></a>Интерфейс ID3DXMesh

Приложения используют методы интерфейса ID3DXMesh для управления объектами сетки.

## <a name="members"></a>Элементы

Интерфейс **ID3DXMesh** наследует от [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXMesh** содержит следующие методы.



| Метод                                                            | Описание                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**локкаттрибутебуффер**](id3dxmesh--lockattributebuffer.md)     | Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.<br/>                                   |
| [**Увеличить**](id3dxmesh--optimize.md)                           | Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.<br/>                                     |
| [**оптимизеинплаце**](id3dxmesh--optimizeinplace.md)             | Создает сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования. Этот метод переупорядочивает существующую сетку.<br/> |
| [**сетаттрибутетабле**](id3dxmesh--setattributetable.md)         | Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.<br/>                                          |
| [**унлоккаттрибутебуффер**](id3dxmesh--unlockattributebuffer.md) | Разблокирует буфер атрибута.<br/>                                                                                                |



 

## <a name="remarks"></a>Комментарии

Чтобы получить интерфейс **ID3DXMesh** , вызовите функцию [**D3DXCreateMesh**](d3dxcreatemesh.md) или [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .

Этот интерфейс наследует дополнительные функциональные возможности интерфейса [**ID3DXBaseMesh**](id3dxbasemesh.md) .

Тип LPD3DXMESH определяется как указатель на интерфейс **ID3DXMesh** .


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




