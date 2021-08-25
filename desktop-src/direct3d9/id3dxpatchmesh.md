---
description: Этот интерфейс инкапсулирует функциональность сетки исправлений.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Интерфейс ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44899ccee6f13aa25b01e284df5a892196d657610c3f89d546fc0b646eeaa069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856284"
---
# <a name="id3dxpatchmesh-interface"></a>Интерфейс ID3DXPatchMesh

Этот интерфейс инкапсулирует функциональность сетки исправлений.

## <a name="members"></a>Элементы

Интерфейс **ID3DXPatchMesh** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPatchMesh** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXPatchMesh** содержит следующие методы.



| Метод                                                                           | Описание                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**клонемеш**](id3dxpatchmesh--clonemesh.md)                                   | Создает новую сетку исправлений с указанным объявлением вершины.<br/>                      |
| [**женератеаджаценци**](id3dxpatchmesh--generateadjacency.md)                   | Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.<br/>                  |
| [**жетконтролвертицесперпатч**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Возвращает число вершин управления на каждое исправление.<br/>                                       |
| [**Объявление о выходе**](id3dxpatchmesh--getdeclaration.md)                         | Возвращает объявление вершины.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Возвращает устройство, создавшее сетку.<br/>                                               |
| [**жетдисплацепарам**](id3dxpatchmesh--getdisplaceparam.md)                     | Возвращает параметры смещения геометрического объекта сетки.<br/>                                          |
| [**жетиндексбуффер**](id3dxpatchmesh--getindexbuffer.md)                         | Возвращает буфер индекса сетки.<br/>                                                          |
| [**жетнумпатчес**](id3dxpatchmesh--getnumpatches.md)                           | Возвращает число исправлений в сетке.<br/>                                              |
| [**жетнумвертицес**](id3dxpatchmesh--getnumvertices.md)                         | Возвращает количество вершин в сетке.<br/>                                             |
| [**Параметры команды**](id3dxpatchmesh--getoptions.md)                                 | Возвращает тип исправления.<br/>                                                              |
| [**жетпатчинфо**](id3dxpatchmesh--getpatchinfo.md)                             | Возвращает атрибуты исправления.<br/>                                                    |
| [**жеттесссизе**](id3dxpatchmesh--gettesssize.md)                               | Возвращает размер тесселяции сетки по заданному уровню тесселяции.<br/>                   |
| [**жетвертексбуффер**](id3dxpatchmesh--getvertexbuffer.md)                       | Возвращает буфер вершин сетки.<br/>                                                         |
| [**локкаттрибутебуффер**](id3dxpatchmesh--lockattributebuffer.md)               | Блокирует буфер атрибута.<br/>                                                          |
| [**локкиндексбуффер**](id3dxpatchmesh--lockindexbuffer.md)                       | Блокировка буфера индекса.<br/>                                                               |
| [**локквертексбуффер**](id3dxpatchmesh--lockvertexbuffer.md)                     | Блокировка буфера вершин.<br/>                                                              |
| [**Оптимизация**](id3dxpatchmesh--optimize.md)                                     | Оптимизирует сетку исправлений для эффективной тесселяции.<br/>                                 |
| [**сетдисплацепарам**](id3dxpatchmesh--setdisplaceparam.md)                     | Задает параметры смещения геометрических объектов сетки.<br/>                                          |
| [**Проводить тесселяцию**](id3dxpatchmesh--tessellate.md)                                 | Выполняет однородную тесселяцию на основе уровня тесселяции.<br/>                       |
| [**тесселлатеадаптиве**](id3dxpatchmesh--tessellateadaptive.md)                 | Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.<br/> |
| [**унлоккаттрибутебуффер**](id3dxpatchmesh--unlockattributebuffer.md)           | Разблокируйте буфер атрибута.<br/>                                                         |
| [**унлоккиндексбуффер**](id3dxpatchmesh--unlockindexbuffer.md)                   | Разблокируйте буфер индексов.<br/>                                                             |
| [**унлокквертексбуффер**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Разблокируйте буфер вершин.<br/>                                                            |



 

## <a name="remarks"></a>Remarks

Сетка исправлений — это сетка, которая состоит из серии исправлений.

Чтобы получить интерфейс **ID3DXPatchMesh** , вызовите функцию [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .

Тип LPD3DXPATCHMESH определяется как указатель на интерфейс **ID3DXPatchMesh** следующим образом:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
