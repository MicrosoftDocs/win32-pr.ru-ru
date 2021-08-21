---
title: 'Функция Рвструктуредбуффер:: Load (int, uint)'
description: 'Считывает данные буфера и возвращает сведения о состоянии операции. | Функция Рвструктуредбуффер:: Load (int, uint)'
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24aee1d7abfcec66fe9e005fdc65010be52b89fdb820374276f12091ddfe2903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986254"
---
# <a name="rwstructuredbufferloadintuint-function"></a>Функция Рвструктуредбуффер:: Load (int, uint)

Считывает данные буфера и возвращает сведения о состоянии операции.

## <a name="syntax"></a>Синтаксис


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **int**

Расположение буфера.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип:

Возвращаемый тип соответствует типу в объявлении для объекта [**рвструктуредбуффер**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
