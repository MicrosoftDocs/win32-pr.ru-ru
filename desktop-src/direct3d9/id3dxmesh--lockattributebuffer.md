---
description: Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Метод ID3DXMesh:: Локкаттрибутебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ca767c6bc223c40d6013b93162de057aac9f4fb1b71303990f9128e4eca1ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802157"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>Метод ID3DXMesh:: Локкаттрибутебуффер

Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
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

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Адрес указателя на буфер, содержащий DWORD для каждой грани в сетке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Если был вызван [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) , в сетке также будет таблица атрибутов, доступ к которой можно получить с помощью метода [**ID3DXBaseMesh:: жетаттрибутетабле**](id3dxbasemesh--getattributetable.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: Унлоккаттрибутебуффер**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh:: Жетаттрибутетабле**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh:: Сетаттрибутетабле**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
