---
description: Определяет макет данных вершин. Каждая вершина может содержать один или несколько типов данных, и каждый тип данных описывается элементом вершины.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Структура D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664983"
---
# <a name="d3dvertexelement9-structure"></a>Структура D3DVERTEXELEMENT9

Определяет макет данных вершин. Каждая вершина может содержать один или несколько типов данных, и каждый тип данных описывается элементом вершины.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Члены

<dl> <dt>

**Stream**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Номер потока.

</dd> <dt>

**Offset**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала данных вершины до данных, связанных с определенным типом данных.

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Тип данных, указанный как [**D3DDECLTYPE**](./d3ddecltype.md). Один из нескольких предопределенных типов, определяющих размер данных. Некоторые методы имеют неявный тип.

</dd> <dt>

**Метод**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Метод задает обработку тесселяции, которая определяет способ интерпретации (или обработки) данных вершин. Дополнительные сведения см. в разделе [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Определяет, для каких данных будут использоваться данные; то есть взаимодействие между макетами данных вершин и шейдерами вершин. Каждое использование служит для привязки объявления вершины к шейдеру вершин. В некоторых случаях они имеют специальную интерпретацию. Например, элемент, указывающий D3DDECLUSAGE \_ нормаль или D3DDECLUSAGE, \_ используется тесселяцией N-patch для настройки тесселяции. Список доступных семантик см. в разделе [**D3DDECLUSAGE**](./d3ddeclusage.md) . D3DDECLUSAGE \_ текскурд можно использовать для определяемых пользователем полей (для которых не определено использование).

</dd> <dt>

**усажеиндекс**
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Изменяет данные об использовании, чтобы разрешить пользователю указывать несколько типов использования.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Данные вершин определяются с помощью массива структур **D3DVERTEXELEMENT9** . Используйте [**D3DDECL \_ End**](d3ddecl-end.md) , чтобы объявить последний элемент в объявлении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Объявление вершины (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
