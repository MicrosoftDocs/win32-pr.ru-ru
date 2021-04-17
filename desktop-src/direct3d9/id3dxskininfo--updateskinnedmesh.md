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
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713445"
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

## <a name="remarks"></a>Комментарии

При использовании для обложки вершин с двумя элементами позиционирования этот метод обрисовывает второй элемент расположения с обратной стороны кости, а не саму кость.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
