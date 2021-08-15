---
description: Доступ к описанию вершины, переданному в D3DX10CreateMesh. Описание вершины описывает макет буферов вершин сетки.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'Метод ID3DX10Mesh:: Жетвертексдескриптион (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5857b5162cf351a235d9cbecd2e457030820485d37e9aa49062a63b196f95900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540230"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>Метод ID3DX10Mesh:: Жетвертексдескриптион

Доступ к описанию вершины, переданному в [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). Описание вершины описывает макет буферов вершин сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдеск* \[ заполняет\]
</dt> <dd>

Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Массив входных элементов, описывающих макет буферов вершин сетки. См [**. \_ элемент D3D10 input \_ element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*пдеклкаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Количество входных элементов в Ппдеск.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
