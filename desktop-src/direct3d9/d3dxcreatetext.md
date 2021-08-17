---
description: Создает сетку, содержащую указанный текст, используя шрифт, связанный с контекстом устройства.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Функция D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9db7cc6fa89f8f102cabccdebd14852a50f60576b6135ae52e4cc9fada494812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732298"
---
# <a name="d3dxcreatetext-function"></a>Функция D3DXCreateText

Создает сетку, содержащую указанный текст, используя шрифт, связанный с контекстом устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство, создавшее сетку.

</dd> <dt>

*HDC* \[ окне\]
</dt> <dd>

Тип: **HDC**

Контекст устройства, содержащий шрифт для выходных данных. Шрифт, выбранный в контексте устройства, должен быть шрифтом TrueType.

</dd> <dt>

*птекст* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую создаваемый текст. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*Отклонение* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное отклонение в соответствии с контурами шрифтов TrueType.

</dd> <dt>

 Объем \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Величина вытягивания текста в отрицательном z-направлении.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Указатель на возвращенную сетку.

</dd> <dt>

*ппаджаценци* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на буфер, содержащий сведения о смежности. Может иметь **значение NULL**.

</dd> <dt>

*пглифметрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпглифметриксфлоат**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Указатель на массив структур [**глифметриксфлоат**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) , содержащих данные метрики глифа. Каждый элемент содержит сведения о положении и ориентации соответствующего глифа в строке. Число элементов в массиве должно быть равно числу символов в строке. Обратите внимание, что источник в каждой структуре не является относительным относительно всей строки, а задается относительно этой символьной ячейки. Чтобы вычислить весь ограничивающий прямоугольник, добавьте шаг приращения для каждого глифа во время прохода по строке. Если вы не беспокоитесь о размере глифов, присвойте этому параметру **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateTextW. В противном случае вызов функции разрешается в D3DXCreateTextA, так как используются строки ANSI.

Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции рисования фигур](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
