---
description: Задает вектор.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'Метод ID3DXBaseEffect:: Сетвектор (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714009"
---
# <a name="id3dxbaseeffectsetvector-method"></a>Метод ID3DXBaseEffect:: Сетвектор

Задает вектор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
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

Указатель на вектор 4D.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Если вектор назначения меньше, чем исходный вектор, дополнительные компоненты исходного вектора будут игнорироваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**Вектор**](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




