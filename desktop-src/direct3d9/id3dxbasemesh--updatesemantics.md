---
description: Этот метод позволяет пользователю изменить объявление сетки, не изменяя макет данных в буфере вершин. Вызов допустим только в том случае, если форматы старого и нового объявлений имеют одинаковый размер вершины.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Метод ID3DXBaseMesh:: Упдатесемантикс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081877"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>Метод ID3DXBaseMesh:: Упдатесемантикс

Этот метод позволяет пользователю изменить объявление сетки, не изменяя макет данных в буфере вершин. Вызов допустим только в том случае, если форматы старого и нового объявлений имеют одинаковый размер вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Объявление* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки. Верхний предел этого массива декларатора — [**Max \_ фвф \_ DECL \_ size**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

[**ID3DXBaseMesh:: клонемеш**](id3dxbasemesh--clonemesh.md) используется для переформатирования и изменения макета данных вершин. Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.

**ID3DXBaseMesh:: упдатесемантикс** — это метод обновления объявления вершины с другой семантической информацией без изменения макета буфера вершин. Например, используйте его для переметки координаты трехмерной текстуры как бинормал или тангенса или наоборот.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh:: Клонемешфвф**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
