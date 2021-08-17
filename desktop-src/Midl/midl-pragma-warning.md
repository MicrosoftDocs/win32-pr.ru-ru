---
title: midl_pragma атрибут предупреждения
description: Используйте параметр компилятора MIDL \_ pragma warning, чтобы временно переопределить поведение сообщения о предупреждении MIDL во время компиляции.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma атрибута предупреждения MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae8e902d1e58ff216f36ae8003dc8f3f553a32005136ef2a86201bd17279107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067094"
---
# <a name="midl_pragma-warning-attribute"></a>MIDL \_ pragma, атрибут Warning

Используйте параметр **компилятора MIDL \_ pragma warning** , чтобы временно переопределить поведение сообщения о предупреждении MIDL во время компиляции.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*\_параметр предупреждения* 
</dt> <dd>

Параметр warning может принимать одно из следующих значений: Disable, Enable, Default.

</dd> <dt>

*\_список сообщений* 
</dt> <dd>

Список номеров сообщений, разделенных пробелами.

</dd> </dl>

## <a name="remarks"></a>Remarks

Директиву pragma можно использовать как директиву pragma C-Compiler. То есть он отключает, включает или возвращает поведение по умолчанию для данного предупреждения MIDL.

## <a name="examples"></a>Примеры

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




