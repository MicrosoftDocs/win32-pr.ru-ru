---
description: Задает массив векторов.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'Метод ID3DXBaseEffect:: Сетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79018873b512b54277f2b63da23a9360389e10b32672be59807e7ef47c9884f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790644"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a>Метод ID3DXBaseEffect:: Сетвектораррай

Задает массив векторов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пвектор* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Массив векторов с плавающей точкой 4D.

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество векторов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Если векторы назначения меньше, чем исходные векторы, дополнительные компоненты исходных векторов будут игнорироваться.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**жетвектораррай**](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
