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
ms.openlocfilehash: 3a9a628c16e7f4a26db9953298be1adcba2cef364153d4bb2e6b29dbc4d9ef83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607324"
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

## <a name="remarks"></a>Remarks

[**ID3DXBaseMesh:: клонемеш**](id3dxbasemesh--clonemesh.md) используется для переформатирования и изменения макета данных вершин. Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.

**ID3DXBaseMesh:: упдатесемантикс** — это метод обновления объявления вершины с другой семантической информацией без изменения макета буфера вершин. Например, используйте его для переметки координаты трехмерной текстуры как бинормал или тангенса или наоборот.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh:: Клонемешфвф**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
