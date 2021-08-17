---
description: Изменяет число выборок, содержащихся в буфере.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'Метод ID3DXPRTBuffer:: resize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c6da4c5de4b38f5fe86b36622b7032e10ffe1be794ee8990ba19362cfd77d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730077"
---
# <a name="id3dxprtbufferresize-method"></a>Метод ID3DXPRTBuffer:: resize

Изменяет число выборок, содержащихся в буфере.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*NewSize* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число выборок, которые должны содержаться в буфере.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. Если метод завершается с ошибкой, будет возвращено следующее значение: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
