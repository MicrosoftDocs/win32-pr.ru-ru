---
description: 'Метод ID3DX10Mesh:: Сетаттрибутетабле — задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'Метод ID3DX10Mesh:: Сетаттрибутетабле (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6cdaedef52693810519ebb92e6f523afbfe078df68a2a13b7fae7ce0fad98fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634544"
---
# <a name="id3dx10meshsetattributetable-method"></a>Метод ID3DX10Mesh:: Сетаттрибутетабле

Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паттрибтабле* \[ окне\]
</dt> <dd>

Тип: **\* [**\_ \_ диапазон атрибутов const D3DX10**](d3dx10-attribute-range.md)**

Указатель на массив \_ структур диапазона АТРИБУТОВ D3DX10 \_ , представляющий записи в таблице атрибутов сетки.

</dd> <dt>

*каттрибтаблесизе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число атрибутов в таблице атрибутов сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Если приложение отслеживает сведения в таблице атрибутов и переупорядочивает таблицу в результате изменений атрибутов или лиц, этот метод позволяет приложению обновлять таблицы атрибутов вместо вызова ID3DX10Mesh:: optimize.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
