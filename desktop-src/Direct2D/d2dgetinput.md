---
title: Функция D2DGetInput (D2d1effecthelpers. h)
description: Возвращает цвет входных данных N во входной координате. Доступно только для простых входных данных.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Функция D2DGetInput Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657826"
---
# <a name="d2dgetinput-function"></a>Функция D2DGetInput

Возвращает цвет входных данных N во входной координате. Доступно только для простых входных данных.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*N* \[ в\]
</dt> <dd>

Входной номер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **float4**, СОДЕРЖАЩУЮ цвет RGBA в формате инпутн.

## <a name="remarks"></a>Комментарии

В следующем примере показана функция, используемая как часть арифметического составного действия.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Другой пример использования этой функции см. в разделе Примечания для [ \_ \_ записи D2D PS](d2d-ps-entry.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Связывание шейдеров эффектов](effect-shader-linking.md)
</dt> <dt>

[Вспомогательные методы HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





