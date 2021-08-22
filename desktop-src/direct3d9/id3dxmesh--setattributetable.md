---
description: 'Метод ID3DXMesh:: Сетаттрибутетабле — задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Метод ID3DXMesh:: Сетаттрибутетабле (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e93bc3f077d239fb93ac23898635dfc2fe5157ed5d78c32719fca6980606658c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606944"
---
# <a name="id3dxmeshsetattributetable-method"></a>Метод ID3DXMesh:: Сетаттрибутетабле

Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паттрибтабле* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Указатель на массив структур [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , представляющий записи в таблице атрибутов сетки.

</dd> <dt>

*каттрибтаблесизе* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число атрибутов в таблице атрибутов сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Если приложение отслеживает сведения в таблице атрибутов и переупорядочивает таблицу в результате изменений атрибутов или лиц, этот метод позволяет приложению обновлять таблицы атрибутов вместо вызова [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: Локкаттрибутебуффер**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh:: Локкаттрибутебуффер**
</dt> </dl>

 

 
