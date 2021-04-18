---
description: Создает новую сетку и заполняет ее данными ранее загруженной сетки.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Метод ID3DX10Mesh:: Клонемеш (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713851"
---
# <a name="id3dx10meshclonemesh-method"></a>Метод ID3DX10Mesh:: Клонемеш

Создает новую сетку и заполняет ее данными ранее загруженной сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Флаги создания, применяемые к новой сетке. См. раздел [**\_ Сетка D3DX10**](d3dx10-mesh.md).

</dd> <dt>

*ппоссемантик* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Семантическое имя для данных о положении.

</dd> <dt>

*пдеск* \[ окне\]
</dt> <dd>

Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Массив \_ структуры входного \_ элемента D3D10 \_ , описывающий формат вершины для возвращенной сетки. См [**. \_ элемент D3D10 input \_ element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*Деклкаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число элементов в массиве Пдеск.

</dd> <dt>

*ппклонемеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Новая сетка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

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

 

 
