---
description: Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания. Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'Метод ID3DXSkinInfo:: пересопоставления (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941a71539184b7d49e35627c932da77b4494486c35506b1b4e5f69ad52c40829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727784"
---
# <a name="id3dxskininforemap-method"></a>Метод ID3DXSkinInfo:: пересопоставления

Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания. Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин для повторного сопоставления.

</dd> <dt>

*пвертексремап* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Массив DWORD, длина которого задается параметром Нумвертицес.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Каждый элемент в Пвертексремап указывает предыдущий индекс вершины для этой позиции. Например, если вершина находится в положении 3, но была повторно сопоставлена с позицией 5, то Пятый элемент Пвертексремап должен содержать 3. Можно использовать массив сопоставления вершин, возвращаемый [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
