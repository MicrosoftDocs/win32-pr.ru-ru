---
description: Определяет атрибуты шрифта.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Структура D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647835"
---
# <a name="d3dx10_font_desc-structure"></a>D3DX10 \_ \_ структура шрифта

Определяет атрибуты шрифта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

Число запрошенных уровней mipmap. Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap. Если значение равно 1, пространство текстуры сопоставляется с пространством экрана одинаково.

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

**Преимущственно \[ LF \_ фацесизе\]**
</dt> <dd>

Тип: **TCHAR**

</dd> <dd>

Строка, завершающаяся нулем, которая указывает имя гарнитуры шрифта. Длина строки не должна превышать 32 символов, включая завершающий символ **null** . Если преимущственно является пустой строкой, будет использоваться первый шрифт, соответствующий другим указанным атрибутам. Если для параметров компилятора требуется Юникод, то тип данных TCHAR разрешается в WCHAR; в противном случае тип данных разрешается в CHAR. См. заметки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет тип структуры. Если задано значение Unicode, \_ \_ тип структуры D3DX10 Font DESC разрешается в D3DX10 \_ шрифт \_ дескв; в противном случае тип структуры разрешается в D3DX10 \_ Font \_ DESC.

Возможные значения приведенных выше элементов приведены в структуре GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
