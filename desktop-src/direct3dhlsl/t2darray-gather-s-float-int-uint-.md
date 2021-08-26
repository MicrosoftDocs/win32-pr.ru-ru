---
title: 'Функция Texture2DArray:: собрать (S, float, int, uint)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: собрать (S, float, int, uint)'
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
keywords:
- Собрать функцию HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2dcc5e9ec7acc6066ffb926fa9b757512e54dbad0e592a0e6bf8035620902f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023354"
---
# <a name="texture2darraygathersfloatintuint-function"></a>Функция Texture2DArray:: собрать (S, float, int, uint)

Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*S* \[ в\]
</dt> <dd>

Тип: **самплерстате**

Индекс выборки с отсчетом от нуля.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **float**

Образцы координат (u, v).

</dd> <dt>

*Смещение* \[ окне\]
</dt> <dd>

Тип: **int**

Смещение, применяемое к координатам текстуры перед выборкой.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **TemplateType**

Значение из четырех компонентов, тип которого совпадает с типом шаблона.

## <a name="remarks"></a>Remarks

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Собрать методы](texture2darray-gather.md)
</dt> </dl>

 

 
