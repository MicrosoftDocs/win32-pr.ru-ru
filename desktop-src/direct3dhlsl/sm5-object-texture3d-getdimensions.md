---
title: 'Функция Texture3D:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture3D:: Dimension'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 8a7dd6248b7b6effc08e510ea56da6426c41dc54418bf7ee5da8cdc3c9ad965a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985714"
---
# <a name="texture3dgetdimensions-function"></a>Функция Texture3D:: Dimension

Возвращает размеры ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Миплевел* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Необязательный элемент. Уровень mipmap (должен быть указан, если используется *нумберофлевелс* ).

</dd> <dt>

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

*Глубина* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Глубина ресурса в пикселей текстуры.

</dd> <dt>

*Нумберофлевелс* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число уровней mipmap (требуется также *миплевел* ).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Ничего

## <a name="remarks"></a>Remarks

Это список перегруженных версий этого метода.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
