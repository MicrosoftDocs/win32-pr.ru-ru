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
ms.openlocfilehash: fce4b8f2fec887397794914604a0755049615699af77c5572536b5758bda2d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986364"
---
# <a name="message-pragma-directive"></a>Директива pragma сообщения

Директива pragma, которая создает сообщения времени компиляции.



| \#сообщение pragma ("*лексема-строка*") |
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

 

 





