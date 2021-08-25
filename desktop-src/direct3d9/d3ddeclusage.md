---
description: Определяет предполагаемое использование данных вершин.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Перечисление D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857514"
---
# <a name="d3ddeclusage-enumeration"></a>Перечисление D3DDECLUSAGE

Определяет предполагаемое использование данных вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGEное \_ расположение**
</dt> <dd>

Размещение данных в диапазоне от (-1,-1) до (1, 1). Используйте D3DDECLUSAGE \_ позиции с индексом использования 0, чтобы указать непреобразованную точку для обработки вершины фиксированной функции и тесселяцию n-patch. Используйте D3DDECLUSAGE \_ позиции с индексом использования, равным 1, чтобы указать непреобразованное расположение в шейдере вершинной функции для анимации вершин.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ блендвеигхт**
</dt> <dd>

Данные веса смешения. Используйте D3DDECLUSAGE \_ блендвеигхт с индексом использования 0, чтобы указать весовые коэффициенты смешения, используемые в индексированном и неиндексированном смешении вершин.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ блендиндицес**
</dt> <dd>

Смешивание данных индексов. Используйте D3DDECLUSAGE \_ блендиндицес с индексом использования 0, чтобы указать индексы матрицы для выборки с индексированными палитрами.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE, \_ Обычная**
</dt> <dd>

Нормальные данные вершин. Используйте D3DDECLUSAGE \_ нормаль с индексом использования, равным 0, чтобы указать нормали вершин для обработки фиксированной вершины функции и тесселяцию n-patch. Используйте D3DDECLUSAGE \_ нормаль с индексом использования, равным 1, чтобы указать нормали вершин для обработки фиксированной вершины функции для анимации вершин.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ псизе**
</dt> <dd>

Размер точки данных. Используйте D3DDECLUSAGE \_ псизе с индексом использования, равным 0, чтобы указать атрибут размера точки, используемый ядром программы установки средства настройки компонента, чтобы расширить точку до четырех элементов для функции "звезда".

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ текскурд**
</dt> <dd>

Данные координат текстуры. Используйте D3DDECLUSAGE \_ текскурд, n для указания координат текстуры в процессе обработки вершин фиксированной функции и в шейдерах пикселей до PS \_ 3 \_ 0. Их можно использовать для передачи определяемых пользователем данных.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ тангенс**
</dt> <dd>

Данные касательной вершины.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ бинормал**
</dt> <dd>

Данные бинормал вершин.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ тессфактор**
</dt> <dd>

Одиночное положительное значение с плавающей точкой. Используйте D3DDECLUSAGE \_ тессфактор с индексом использования 0, чтобы указать коэффициент тесселяции, используемый в единице тесселяции для управления частотой тесселяции. Дополнительные сведения о типе данных см. в разделе D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ позиций**
</dt> <dd>

Данные вершин содержат преобразованные данные о положении в диапазоне от (0, 0) до (ширина окна просмотра, высота окна просмотра). Используйте D3DDECLUSAGE \_ позиции с индексом использования, равным 0, чтобы указать преобразованное расположение. Если задано объявление, содержащее это значение, конвейер не выполняет обработку вершин.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Цвет D3DDECLUSAGE**
</dt> <dd>

Данные вершин содержат рассеянный или отраженный цвет. Используйте D3DDECLUSAGE \_ Color с индексом использования, равным 0, чтобы указать рассеянный цвет в предваряющих текстурах в функции и шейдеры пикселей до PS \_ 3 \_ 0. Используйте D3DDECLUSAGE \_ Color с индексом использования, равным 1, чтобы указать отражающий цвет в предваряющих текстурах и в шейдерах пикселей перед PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ туман**
</dt> <dd>

Данные вершин содержат данные тумана. Используйте D3DDECLUSAGE \_ туман с индексом использования, равным 0, чтобы указать значение смешения тумана, используемое после завершения заливки пикселей. Это относится к шейдерам пикселей до версии PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**\_Глубина D3DDECLUSAGE**
</dt> <dd>

Данные вершин содержат данные глубины.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Пример D3DDECLUSAGE**
</dt> <dd>

Данные вершин содержат данные выборки. Используйте \_ Пример D3DDECLUSAGE с индексом использования, равным 0, чтобы указать значение смещения для поиска. Его можно использовать только с D3DDECLUSAGE \_ лукуппресамплед или D3DDECLUSAGE \_ Lookup.

</dd> </dl>

## <a name="remarks"></a>Remarks

Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Каждый элемент массива содержит тип использования.

Дополнительные сведения об объявлениях вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Объявление вершины (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




