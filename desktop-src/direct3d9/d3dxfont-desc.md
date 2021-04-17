---
description: Определяет атрибуты шрифта.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Структура D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720891"
---
# <a name="d3dxfont_desc-structure"></a>\_Структура D3DXFONT DESC

Определяет атрибуты шрифта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Height**
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота в логических единицах символьной ячейки или символа шрифта.

</dd> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина (в логических единицах) символов в шрифте.

</dd> <dt>

**Weight**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Вес шрифта в диапазоне от 0 до 1000.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число запрошенных уровней MIP. Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap. Если значение равно 1, пространство текстуры сопоставляется с пространством экрана одинаково.

</dd> <dt>

**Наклонный**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Задайте значение **true** для курсивного шрифта.

</dd> <dt>

**CharSet**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Кодировка.

</dd> <dt>

**аутпутпреЦисион**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Точность вывода. Точность вывода определяет, насколько близко выходные данные должны соответствовать запрошенной высоте, ширине, ориентации символов, Escape, тону и типу шрифта.

</dd> <dt>

**Качество**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Качество вывода.

</dd> <dt>

**питчандфамили**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота и семейство шрифта.

</dd> <dt>

**Преимущственно**
</dt> <dd>

Тип: **TCHAR**

</dd> <dd>

Строка или символы, заканчивающиеся нулем и указывающие гарнитуру шрифта. Длина строки не должна превышать 32 символов, включая завершающий символ null. Если преимущственно является пустой строкой, будет использоваться первый шрифт, соответствующий другим указанным атрибутам. Если для параметров компилятора требуется Юникод, то тип данных TCHAR разрешается в WCHAR; в противном случае тип данных разрешается в CHAR. См. заметки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет тип структуры. Если определен Юникод, \_ тип структуры D3DXFONT DESC разрешается в D3DXFONT \_ дескв; в противном случае тип структуры разрешается в D3DXFONT \_ DESC.

Возможные значения приведенных выше элементов приведены в структуре GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
