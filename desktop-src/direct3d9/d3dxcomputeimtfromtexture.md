---
description: Вычисляет ИМТ для каждого треугольника из текстуры, сопоставленной с сеткой, которая может использоваться в качестве входных данных для функций Уватлас D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Функция D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081914"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>Функция D3DXComputeIMTFromTexture

Вычисляет ИМТ для каждого треугольника из текстуры, сопоставленной с сеткой, которая может использоваться в качестве входных данных для [функций УВАТЛАС](dx9-graphics-reference-d3dx-functions-uvatlas.md)D3DX.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.

</dd> <dt>

*птекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на текстуру (см. [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)), сопоставленный с сеткой.

</dd> <dt>

*двтекстуреиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.

</dd> <dt>

*двоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры переноса текстур. Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*пстатускаллбакк* 
</dt> <dd>

Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.

</dd> <dt>

*пусерконтекст* 
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния. Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.

</dd> <dt>

*ппимтдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ. Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Учитывая текстуру, которая сопоставляется с поверхностью сетки, алгоритм рассчитывает ИМТ для каждой грани. Это приведет к тому, что треугольники, содержащие данные сигнала с более низкой частотой, будут занимать меньше пространства в окончательной текстуре Atlas при параметризации с помощью функций Уватлас. Предполагается, что текстура будет интерполяция через сетку билинеарли.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Использование Уватлас (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
