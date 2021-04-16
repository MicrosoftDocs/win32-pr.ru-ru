---
title: /Сал, параметр
description: Параметр/Сал направляет MIDL для создания аннотаций SAL в создаваемых файлах-заглушках.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL/Сал Switch
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650312"
---
# <a name="sal-switch"></a>/Сал, параметр

Параметр **/Сал** направляет MIDL для создания аннотаций SAL в создаваемых файлах-заглушках.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

MIDL помечает параметры указателя и массива с заметками, отражающими описание параметра в IDL-файле в соответствии с применением RPC и подсистемой маршалирования NDR. MIDL не создает аннотации для параметров в методах интерфейса, помеченных [**\[ локальным \]**](local.md)атрибутом, если в командной строке также отсутствует [**/Сал \_ Local**](-sal-local.md) . Чтобы переопределить созданную с помощью MIDL аннотацию, используйте атрибут [**\[ аннотации \]**](annotate.md) .

Созданные MIDL-заметки всегда имеют префикс \_ \_ RPC \_ и должны использовать заголовок **RPCSS. h** для преобразования аннотации в стандартные аннотации SAL.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Сал \_ локальный**](-sal-local.md)
</dt> <dt>

[**\[комментировани\]**](annotate.md)
</dt> </dl>

 

 




