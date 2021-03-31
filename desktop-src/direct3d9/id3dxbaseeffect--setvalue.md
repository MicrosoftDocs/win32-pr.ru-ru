---
description: Задайте значение произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'Метод ID3DXBaseEffect:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157215"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>Метод ID3DXBaseEffect:: SetValue

Задайте значение произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий данные.

</dd> <dt>

*Байт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

\[в \] байтах в буфере. \_Если вы уверены, что размер буфера достаточно велик, чтобы вместить весь параметр, и вы хотите пропустить проверку размера, передайте значение D3DX по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод можно использовать вместо почти всех вызовов API набора эффектов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
