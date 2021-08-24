---
description: Возвращает массив значений с плавающей запятой.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'Метод ID3DXBaseEffect:: Жетфлоатаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9d4d675a368c927ca8f33197f754a64e83b8beef109c6b0d12e95121f60a2915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791004"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a>Метод ID3DXBaseEffect:: Жетфлоатаррай

Возвращает массив значений с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Общая папка* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Возвращает массив значений с плавающей запятой.

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число значений с плавающей запятой в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**сетфлоатаррай**](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
