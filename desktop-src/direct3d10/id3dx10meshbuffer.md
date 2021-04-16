---
description: Буфер сетки — это буфер, содержащий данные о сетке.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Интерфейс ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651551"
---
# <a name="id3dx10meshbuffer-interface"></a>Интерфейс ID3DX10MeshBuffer

Буфер сетки — это буфер, содержащий данные о сетке. Он может содержать один из пяти различных типов данных: данные вершин, индексные данные, соседство, данные атрибутов или данные-контейнеры. Эта структура используется для доступа к этим пяти фрагментам данных с помощью следующих пяти API: [**ID3DX10Mesh:: жетвертексбуффер**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: жетиндексбуффер**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: Жетаджаценцибуффер**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: жетаттрибутебуффер**](id3dx10mesh-getattributebuffer.md)или [**ID3DX10Mesh:: жетпоинтрепбуффер**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Элементы

Интерфейс **ID3DX10MeshBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10MeshBuffer** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10MeshBuffer** содержит следующие методы.



| Метод                                       | Описание                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Возвращает размер буфера сетки в байтах.<br/>                      |
| [**Таблица**](id3dx10meshbuffer-map.md)         | Получите указатель на память буфера сетки, чтобы изменить ее содержимое.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Отмена сопоставления буфера.<br/>                                                 |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
