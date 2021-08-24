---
description: Интерфейс ID3DXBuffer используется в качестве буфера данных, сохраняя сведения о вершинах, соседях и материалах во время оптимизации сетки и операций загрузки.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Интерфейс ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121682"
---
# <a name="id3dxbuffer-interface"></a>Интерфейс ID3DXBuffer

Интерфейс ID3DXBuffer используется в качестве буфера данных, сохраняя сведения о вершинах, соседях и материалах во время оптимизации сетки и операций загрузки. Объект buffer используется для возврата произвольных данных о длине. Кроме того, объекты буфера используются для возврата объектного кода и сообщений об ошибках в методах, собирающих шейдеры вершин и пикселей.

## <a name="members"></a>Элементы

Интерфейс **ID3DXBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBuffer** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXBuffer** содержит следующие методы.



| Метод                                                    | Описание                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**жетбуфферпоинтер**](id3dxbuffer--getbufferpointer.md) | Извлекает указатель на данные в буфере.<br/>      |
| [**жетбуфферсизе**](id3dxbuffer--getbuffersize.md)       | Возвращает общий размер данных в буфере.<br/> |



 

## <a name="remarks"></a>Remarks

Интерфейс **ID3DXBuffer** получается путем вызова функции [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .

Тип LPD3DXBUFFER определяется как указатель на интерфейс **ID3DXBuffer** .


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
