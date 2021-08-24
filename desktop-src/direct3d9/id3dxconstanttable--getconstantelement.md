---
description: Возвращает константу из массива констант. Массив состоит из элементов.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Метод ID3DXConstantTable:: Жетконстантелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb1adacadb92cf3a2f9a3e041e4a94a840994db3244233509350448008bd675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748784"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>Метод ID3DXConstantTable:: Жетконстантелемент

Возвращает константу из массива констант. Массив состоит из элементов.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор массива констант. Это значение не может быть **равно NULL**.

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс элемента в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает уникальный идентификатор для константы элемента.

## <a name="remarks"></a>Remarks

Чтобы получить константу, которая не является частью массива, используйте [**ID3DXConstantTable::-Constant**](id3dxconstanttable--getconstant.md) или [**ID3DXConstantTable:: жетконстантбинаме**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
