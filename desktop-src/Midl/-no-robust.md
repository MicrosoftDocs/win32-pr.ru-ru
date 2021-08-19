---
title: no_robust Switch
description: /Но \_ надежный коммутатор направляет КОМПИЛЯТОР MIDL явным образом отключить функцию командной строки/robust. Параметр командной строки/robust и связанные с ним компоненты являются параметрами компилятора по умолчанию для MIDL версии 6.0.359 и более поздних.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust параметр MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808859"
---
# <a name="no_robust-switch"></a>/но \_ надежный коммутатор

**/Но \_ надежный** коммутатор направляет компилятор MIDL явным образом отключить функцию командной строки [**/robust**](-robust.md) . Параметр командной строки **/robust** и связанные с ним компоненты являются параметрами компилятора по умолчанию для MIDL версии 6.0.359 и более поздних.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

В MIDL версии 6.0.359 и более поздних компилятор MIDL устанавливает [**/robust**](-robust.md) по умолчанию. **/Но \_ надежный** параметр командной строки должен использоваться для отключения функции **/robust** , если созданные заглушки должны выполняться в Microsoft Windows NT, Windows 95/98 или Windows.

## <a name="examples"></a>Примеры

**MIDL/но \_ надежность filename. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




