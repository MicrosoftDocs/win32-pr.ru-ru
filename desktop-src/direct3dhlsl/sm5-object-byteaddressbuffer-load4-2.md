---
title: 'Функция Битеаддрессбуффер:: Load4 (uint, uint)'
description: Возвращает четыре значения и состояние операции.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Функция Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070028"
---
# <a name="load4uint-uint-function"></a>Load4 (uint, uint), функция

Возвращает четыре значения и состояние операции.

## <a name="syntax"></a>Синтаксис

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **uint**

Входной адрес в байтах, который должен быть кратным 4.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint4**

Четыре значения.

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[**битеаддрессбуффер**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 