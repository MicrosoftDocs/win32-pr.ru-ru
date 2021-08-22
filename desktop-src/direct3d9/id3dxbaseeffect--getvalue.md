---
description: Получение значения произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры. Этот метод можно использовать вместо почти всех вызовов Жеткскскс в ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'Метод ID3DXBaseEffect:: GetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f957ae3b59f10a086f2326e82478afb6b0ba7fd85bbf6b3f78df5746b7fcb56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494704"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>Метод ID3DXBaseEffect:: GetValue

Получение значения произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры. Этот метод можно использовать вместо почти всех вызовов Жеткскскс в [**ID3DXBaseEffect**](id3dxbaseeffect.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Возвращает буфер, содержащий значение.

</dd> <dt>

*Байт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

\[в \] байтах в буфере. \_Если вы уверены, что размер буфера достаточно велик, чтобы вместить весь параметр, и вы хотите пропустить проверку размера, передайте значение D3DX по умолчанию.

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

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
