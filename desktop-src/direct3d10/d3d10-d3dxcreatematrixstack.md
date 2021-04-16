---
description: Создание стека матриц.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Функция D3DXCreateMatrixStack (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424473"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a>Функция D3DXCreateMatrixStack (D3DX10Math. h)

Создание стека матриц.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Не реализован. Укажите нуль.

</dd> <dt>

*ппстакк* \[ заполняет\]
</dt> <dd>

Тип: **LPD3DXMATRIXSTACK \***

Адрес указателя на стек матрицы (см. [**интерфейс ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
