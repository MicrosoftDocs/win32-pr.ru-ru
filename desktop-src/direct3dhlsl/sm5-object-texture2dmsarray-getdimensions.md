---
title: 'Функция Texture2DMSArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2DMSArray:: Dimension'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
keywords:
- Функция Dimension HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353722"
---
# <a name="texture2dmsarraygetdimensions-function"></a>Функция Texture2DMSArray:: Dimension

Возвращает размеры ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Ширина* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ширина ресурса в пикселей текстуры.

</dd> <dt>

*Высота* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Высота ресурса в пикселей текстуры.

</dd> <dt>

*Элементы* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество элементов в массиве.

</dd> <dt>

*Нумберофсамплес* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число расположений выборки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Nothing

## <a name="remarks"></a>Примечания

Это список перегруженных версий этого метода.


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
