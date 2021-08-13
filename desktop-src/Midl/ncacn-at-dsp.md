---
title: атрибут ncacn_at_dsp
description: '\_ \_ Ключевое слово нкакн at DSP определяет AppleTalk DSP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb021f9212f1034f0b3c235ad77d9ad270325af914887252494316f9ae1c41b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642775"
---
# <a name="ncacn_at_dsp-attribute"></a>\_атрибут нкакн в \_ DSP

Ключевое слово **нкакн \_ at \_ DSP** определяет AppleTalk DSP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя порта* 
</dt> <dd>

Задает символьную строку длиной до 22 байт.

</dd> </dl>

## <a name="remarks"></a>Remarks

Синтаксис строки порта AppleTalk DSP, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL. Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**конечной**](endpoint.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Строковая привязка**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 