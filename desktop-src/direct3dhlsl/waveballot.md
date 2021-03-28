---
title: Функция Вавеактивебаллот
description: Возвращает uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущем волне.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Функция Вавеактивебаллот HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533596"
---
# <a name="waveactiveballot-function"></a>Функция Вавеактивебаллот

Возвращает uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущем волне. 

## <a name="syntax"></a>Синтаксис

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Логическое выражение для вычисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект uint4, содержащий битовую маску вычисления логического выражения для всех активных желобов в текущей волны. Наименьший значащий бит соответствует полосе с нулевым индексом. Биты, соответствующие неактивным дорожкам, будут равны нулю. Биты, которые больше или равны [**вавежетланекаунт**](wavegetlanecount.md) , будут равны нулю.

## <a name="remarks"></a>Примечания

Разные GPU имеют разную ширину процессоров SIMD (число полос). Большая часть этих функций **вавекскскс** может работать на уровне абстракции, где скрыта ширина виртуальной машины. Чтобы обеспечить максимальную переносимость кода на графических процессорах, используйте встроенные функции, не зависящие от ширины компьютера. Например, вы можете использовать следующие службы.

``` syntax
uint result = WaveActiveCountBits( bBit );
```

вместо следующего кода:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 




