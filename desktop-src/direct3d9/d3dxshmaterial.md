---
description: В сферах с сферическими гармониями (SH) предварительно вычисленные радианце передаваемые материалы (PRT).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Структура D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713645"
---
# <a name="d3dxshmaterial-structure"></a>Структура D3DXSHMATERIAL

В сферах с сферическими гармониями (SH) предварительно вычисленные радианце передаваемые материалы (PRT).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Члены

<dl> <dt>

**Диффузное**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Рассеянный албедо поверхности. Это значение игнорируется, если объект является зеркалом.

</dd> <dt>

**бмиррор**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Необходимо задать значение **false**.

</dd> <dt>

**бсубсурф**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Задайте значение **true** , чтобы включить рассеивание подповерхности; любой объект, не являющийся разбросам подповерхности, не может быть зеркалом.

</dd> <dt>

**релативеиндексофрефрактион**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Относительный индекс refraction является соотношением между двумя абсолютными индексами refraction. Индекс refraction — это отношение синуса угла объекта к синусу угла дробной части.

</dd> <dt>

**абсорптион**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Коэффициент абсорптион — это параметр уравнения для подготовки к просмотру тома, который используется для моделирования облегчения распространения на принимающем носителе.

</dd> <dt>

**редуцедскаттеринг**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Уменьшение коэффициента распределения — это параметр уравнения для подготовки к просмотру тома, который используется для моделирования облегчения распространения на принимающем носителе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Спектрал сцены используют красный канал из материалов вместо значения светимости.

Дополнительные сведения о PRT см. в следующих статьях:

-   Йенсен, Хенрик ванн, et al. Сигграф материалы: практическая модель для транспорта тонкой поверхности, 2001.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
