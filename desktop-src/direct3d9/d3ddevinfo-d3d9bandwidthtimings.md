---
description: Метрики пропускной способности для получения помощи в понимании производительности приложения.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Структура D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273737"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>\_Структура D3D9BANDWIDTHTIMINGS D3DDEVINFO

Метрики пропускной способности для получения помощи в понимании производительности приложения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**максбандвидсутилизед**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Пропускная способность или максимальная скорость передачи данных с центрального процессора узла на GPU. Обычно это полоса пропускания шины PCI или AGP, соединяющая ЦП и GPU.

</dd> <dt>

**фронтендуплоадмеморютилизедперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент использования памяти при передаче данных с центрального процессора на графический процессор.

</dd> <dt>

**вертексратеутилизедперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент пропускной способности вершин. Это количество обработанных вершин по сравнению с теоретической максимальной скоростью обработки вершин.

</dd> <dt>

**трианглесетупратеутилизедперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Установка треугольника — процент пропускной способности. Число треугольников, настроенных для растрирования по сравнению с теоретической максимальной скоростью настройки треугольника.

</dd> <dt>

**филлратеутилизедперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент пропускной способности заполнения пикселей. Число пикселей, которые заполняются по сравнению с теоретической заливкой пикселей.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
