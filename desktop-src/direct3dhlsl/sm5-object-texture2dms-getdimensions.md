---
title: 'Функция Texture2DMS:: Dimension'
description: 'Возвращает размеры ресурса. | Функция Texture2DMS:: Dimension'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: dbe034b6484b80efb58712196c4bd4d0aa67800c51f659c97b0d400e934eeecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985834"
---
# <a name="texture2dmsgetdimensions-function"></a>Функция Texture2DMS:: Dimension

Возвращает размеры ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
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

*Нумберофсамплес* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число расположений выборки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Это список перегруженных версий этого метода.


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
