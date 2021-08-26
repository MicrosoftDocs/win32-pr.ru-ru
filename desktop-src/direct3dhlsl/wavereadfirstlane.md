---
title: Функция Вавереадланефирст
description: Возвращает значение выражения для активной полосы текущего волна с наименьшим индексом.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- Функция Вавереадланефирст HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b7b8e22cb17db4bdb2d692dc003baf63a6c6836c7d1a05a67444d254940e342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948914"
---
# <a name="wavereadlanefirst-function"></a>Функция Вавереадланефирст

Возвращает значение выражения для активной полосы текущего волна с наименьшим индексом.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Выражение для вычисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Полученное значение равномерно распределяется по волнам.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 




