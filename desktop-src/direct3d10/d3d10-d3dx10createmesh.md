---
description: Создает объект сетки с помощью декларатора.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Функция D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685009"
---
# <a name="d3dx10createmesh-function"></a>Функция D3DX10CreateMesh

Создает объект сетки с помощью декларатора.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), объект устройства, связываемый с сеткой.

</dd> <dt>

*пдекларатион* \[ окне\]
</dt> <dd>

Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Массив элементов [**D3D10 \_ \_ элемента ввода \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , описывающих формат вершины для возвращенной сетки. Этот параметр должен быть напрямую сопоставлен с гибким форматом вершин (ФВФ).

</dd> <dt>

*Деклкаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число элементов в Пдекларатион.

</dd> <dt>

*ппоситионсемантик* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Семантика, определяющая, какая часть объявления вершины содержит сведения о положении.

</dd> <dt>

*Вертекскаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин для сетки. Этот параметр должен быть больше 0.

</dd> <dt>

*Фацекаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число граней для сетки. Допустимый диапазон для этого числа больше 0 и один меньше максимального значения DWORD (обычно 65534), так как последний индекс зарезервирован.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из [**\_ сетки D3DX10**](d3dx10-mesh.md), указывая параметры сетки.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Адрес указателя на [**интерфейс ID3DX10Mesh**](id3dx10mesh.md), представляющий созданный объект сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Функции D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
