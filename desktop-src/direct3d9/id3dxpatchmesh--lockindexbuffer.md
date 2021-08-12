---
description: Блокировка буфера индекса.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'Метод ID3DXPatchMesh:: Локкиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd0e4fc41507e6b01dcbf77ae19a69dbc4b8e3df981f4c3366f441f4e4854aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294347"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a>Метод ID3DXPatchMesh:: Локкиндексбуффер

Блокировка буфера индекса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки. Для этого метода допустимы следующие флаги:

-   D3DLOCK \_ отбросить
-   D3DLOCK \_ без \_ "грязного" \_ обновления
-   D3DLOCK \_ носислокк
-   D3DLOCK \_ ReadOnly

Описание флагов см. в разделе [D3DLOCK](d3dlock.md).

</dd> <dt>

*ппдата* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***

\*Указатель void на буфер памяти, содержащий возвращенные данные индекса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Буфер индексов обычно блокируется, записывается в, а затем разблокируется для чтения. Буферы индекса сети исправлений представляют собой 16-битные буферы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
