---
description: Задает массив логических значений.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'Метод ID3DXBaseEffect:: Сетбуларрай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647806"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a>Метод ID3DXBaseEffect:: Сетбуларрай

Задает массив логических значений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Pb* \[ окне\]
</dt> <dd>

Тип: **const [**bool**](../winprog/windows-data-types.md) \***

Массив логических значений.

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число логических значений в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**жетбуларрай**](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
