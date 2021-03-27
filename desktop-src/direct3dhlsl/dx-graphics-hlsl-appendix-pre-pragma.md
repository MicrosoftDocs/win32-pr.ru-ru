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
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068998"
---
# <a name="pragma-directive"></a>\#Директива pragma

Директива препроцессора, которая предоставляет зависящие от компьютера или операционные системы функции, сохраняя общую совместимость с языками C и C++.



| \#*строка маркера* pragma |
|-------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                    | Описание                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*<br/> | Последовательность символов, которая предоставляет определенную инструкцию и аргументы компилятора. Этот параметр подлежит раскрытию макросов. <br/> |



 

## <a name="remarks"></a>Примечания

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

 

 





