---
description: Этот интерфейс реализуется приложением для выделения или освобождения объектов контейнера фрейма и сетки. Методы для этого вызываются во время загрузки и уничтожения иерархий фреймов.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Интерфейс ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081934"
---
# <a name="id3dxallocatehierarchy-interface"></a>Интерфейс ID3DXAllocateHierarchy

Этот интерфейс реализуется приложением для выделения или освобождения объектов контейнера фрейма и сетки. Методы для этого вызываются во время загрузки и уничтожения иерархий фреймов.

## <a name="members"></a>Элементы

Интерфейс **ID3DXAllocateHierarchy** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAllocateHierarchy** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXAllocateHierarchy** содержит следующие методы.



| Метод                                                                       | Описание                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**креатефраме**](id3dxallocatehierarchy--createframe.md)                   | Запрашивает выделение объекта Frame.<br/>            |
| [**креатемешконтаинер**](id3dxallocatehierarchy--createmeshcontainer.md)   | Запрашивает выделение объекта контейнера сетки.<br/>   |
| [**дестройфраме**](id3dxallocatehierarchy--destroyframe.md)                 | Запрашивает освобождение объекта Frame.<br/>          |
| [**дестроймешконтаинер**](id3dxallocatehierarchy--destroymeshcontainer.md) | Запрашивает освобождение объекта контейнера сетки.<br/> |



 

## <a name="remarks"></a>Комментарии

Тип LPD3DXALLOCATEHIERARCHY определяется как указатель на этот интерфейс.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
