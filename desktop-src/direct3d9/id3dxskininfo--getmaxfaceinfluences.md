---
description: Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'Метод ID3DXSkinInfo:: Жетмаксфацеинфлуенцес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424314"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>Метод ID3DXSkinInfo:: Жетмаксфацеинфлуенцес

Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПИБ* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Указатель на индексный буфер, содержащий данные индекса сетки.

</dd> <dt>

*Нумфацес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число лиц в сетке.

</dd> <dt>

*максфацеинфлуенцес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на максимальное влияние на лицо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
