---
title: 'Функция Texture2DArray:: Гасералфа (S, float, int, uint)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасералфа (S, float, int, uint)'
ms.assetid: B04F29A7-0EC9-49F0-9662-00F1DD0F3E5B
keywords:
- Функция Гасералфа HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6efa67eb0f2e3eed33f18788443723fadce825a381511019dcc24d941656865c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788294"
---
# <a name="texture2darraygatheralphasfloatintuint-function"></a>Функция Texture2DArray:: Гасералфа (S, float, int, uint)

Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherAlpha(
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

[Методы Гасералфа](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
