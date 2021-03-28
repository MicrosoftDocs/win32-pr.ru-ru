---
title: Директива pragma сообщения
description: Директива pragma, которая создает сообщения времени компиляции.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Директива pragma Message HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784461"
---
# <a name="message-pragma-directive"></a>Директива pragma сообщения

Директива pragma, которая создает сообщения времени компиляции.



| \#pragma Message "*токен-String*" |
|-----------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                    | Описание                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*<br/> | Сообщение компилятора.<br/> |



 

## <a name="examples"></a>Примеры

В следующем примере демонстрируется обработка сообщений во время предварительной обработки.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Директива pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





