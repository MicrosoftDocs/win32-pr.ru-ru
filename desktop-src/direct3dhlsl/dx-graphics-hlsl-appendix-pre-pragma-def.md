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
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996823"
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



 

## <a name="remarks"></a>Примечания

Директива pragma DEF позволяет разработчику предварительно заполнить регистр шейдера с плавающей точкой с указанным значением. Эта директива pragma используется редко.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Директива pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





