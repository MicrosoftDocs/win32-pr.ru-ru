---
description: Рисует подмножество сетки.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: 'ID3DX10Mesh: метод:D Равсубсет (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674699"
---
# <a name="id3dx10meshdrawsubset-method"></a>ID3DX10Mesh: метод:D Равсубсет

Рисует подмножество сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аттрибид* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Указывает подмножество рисуемой сетки. Это значение используется для различения лиц в сетке как принадлежащих одной или нескольким группам атрибутов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д. Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
