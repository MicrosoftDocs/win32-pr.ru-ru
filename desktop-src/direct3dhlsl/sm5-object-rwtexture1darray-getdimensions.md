---
title: 'Функция RWTexture1DArray:: Dimension'
description: 'Возвращает размеры ресурса. | Функция RWTexture1DArray:: Dimension'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273538"
---
# <a name="rwtexture1darraygetdimensions-function"></a>Функция RWTexture1DArray:: Dimension

Возвращает размеры ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Ширина* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ширина ресурса в пикселей текстуры.

</dd> <dt>

*Элементы* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Количество элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

Это список перегруженных версий этого метода.


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
