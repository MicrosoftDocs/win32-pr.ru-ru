---
title: Директива pragma DEF
description: Директива pragma, которая вручную выделяет регистр шейдера с плавающей запятой.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Директива pragma DEF HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6961f5fd8c05f291af3634c07de6befada0efa54586796ca881bffe893bf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726444"
---
# <a name="def-pragma-directive"></a>Директива pragma DEF

Директива pragma, которая вручную выделяет регистр шейдера с плавающей запятой.



| \#pragma DEF ( *Целевая*, *Регистрация*, *val1*, *val2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                        | Описание                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*мишень*<br/>       | Целевой объект, содержащий регистр для выделения. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*зарегистрировать*<br/> | Регистр шейдера с плавающей точкой для выделения. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Первый байт значения, которое необходимо выделить указанному регистру. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Второй байт значения, которое необходимо выделить указанному регистру. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Третий байт значения, которое необходимо выделить указанному регистру. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Четвертый байт значения, которое необходимо выделить указанному регистру. <br/> |



 

## <a name="remarks"></a>Remarks

Директива pragma DEF позволяет разработчику предварительно заполнить регистр шейдера с плавающей точкой с указанным значением. Эта директива pragma используется редко.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Директива pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





