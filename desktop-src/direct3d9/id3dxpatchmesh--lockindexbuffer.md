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
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548135"
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

## <a name="remarks"></a>Комментарии

Буфер индексов обычно блокируется, записывается в, а затем разблокируется для чтения. Буферы индекса сети исправлений представляют собой 16-битные буферы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
