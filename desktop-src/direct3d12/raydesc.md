---
description: Передается функции Трацерай для определения источника, направления и экстентов луча.
ms.assetid: ''
title: Структура Райдеск
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701248"
---
# <a name="raydesc-structure"></a>Структура Райдеск

Передается функции [**трацерай**](traceray-function.md) для определения источника, направления и экстентов луча.

## <a name="syntax"></a>Синтаксис


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Поля

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Лета**
</dt> <dd>

Источник луча.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**тмин**
</dt> <dd>

Минимальная область луча.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Двух**
</dt> <dd>

Направление луча.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**тмакс**
</dt> <dd>

Максимальная область луча.


</dd>

## <a name="requirements"></a>Требования



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




