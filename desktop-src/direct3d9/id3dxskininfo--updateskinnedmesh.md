---
description: Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Метод ID3DXSkinInfo:: Упдатескиннедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729456"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>Метод ID3DXSkinInfo:: Упдатескиннедмеш

Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбонетрансформс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Матрица преобразования костей.

</dd> <dt>

*пбонеинвтранспосетрансформс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Обратная трансформация матрицы преобразования костей.

</dd> <dt>

*пвертицессрк* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий исходные вершины.

</dd> <dt>

*пвертицесдст* \[ окне\]
</dt> <dd>

Тип: **[ **PVOID**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий целевые вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

При использовании для обложки вершин с двумя элементами позиционирования этот метод обрисовывает второй элемент расположения с обратной стороны кости, а не саму кость.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
