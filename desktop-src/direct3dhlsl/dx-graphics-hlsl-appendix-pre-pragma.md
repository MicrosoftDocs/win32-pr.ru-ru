---
title: " Директива pragma"
description: Директива препроцессора, которая предоставляет зависящие от компьютера или операционные системы функции, сохраняя общую совместимость с языками C и C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Директива pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024614"
---
# <a name="pragma-directive"></a>\#Директива pragma

Директива препроцессора, которая предоставляет зависящие от компьютера или операционные системы функции, сохраняя общую совместимость с языками C и C++.



| \#*строка маркера* pragma |
|-------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                    | Описание                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*<br/> | Последовательность символов, которая предоставляет определенную инструкцию и аргументы компилятора. Этот параметр подлежит раскрытию макросов. <br/> |



 

## <a name="remarks"></a>Remarks

Если компилятор обнаруживает прагма-директиву, которая не распознается, она выдает предупреждение, но компиляция будет продолжена.

Компилятор HLSL распознает следующие директивы pragma:

-   [DEF](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [\_Матрица Pack](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>См. также

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





