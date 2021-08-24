---
description: Возвращает матрицу смещения кости.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'Метод ID3DXSkinInfo:: Жетбонеоффсетматрикс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d10586fc9d4008ebd22b7edf2fa955628ffa0ab703ef70ed06cb2f2cb1fd8d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492304"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>Метод ID3DXSkinInfo:: Жетбонеоффсетматрикс

Возвращает матрицу смещения кости.

## <a name="syntax"></a>Синтаксис


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кость* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Номер кости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Возвращает указатель на матрицу смещения кости. Не освобождайте этот указатель.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**сетбонеоффсетматрикс**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**жетнумбонес**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
