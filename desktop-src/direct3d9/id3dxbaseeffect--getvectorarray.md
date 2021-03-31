---
description: Возвращает массив векторов.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'Метод ID3DXBaseEffect:: Жетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354123"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a>Метод ID3DXBaseEffect:: Жетвектораррай

Возвращает массив векторов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пвектор* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Возвращает массив векторов с плавающей точкой 4D.

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество векторов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Если векторы назначения больше, чем исходные векторы, будут заполнены только исходные компоненты каждого целевого вектора, а остальные компоненты вектора назначения будут равны нулю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**сетвектораррай**](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
