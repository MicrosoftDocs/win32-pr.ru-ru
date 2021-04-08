---
title: /рпксс, параметр
description: Если указан параметр/рпксс, он действует так, как если бы \_ для всех операций интерфейса был указан атрибут включения выделения. Использование этого атрибута не рекомендуется.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL/рпксс Switch
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068850"
---
# <a name="rpcss-switch"></a>/рпксс, параметр

Если указан параметр **/рпксс** , он действует так, как если бы для всех операций интерфейса был указан атрибут [**включения \_ выделения**](enable-allocate.md) . Использование этого атрибута не рекомендуется.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

В режиме по умолчанию пакет RPCSS включается только в том случае, если для процедуры или интерфейса установлен атрибут [**Enable \_ allocate**](enable-allocate.md) или параметр **/рпксс** указан в командной строке. В режиме **/ОСФ** заглушка на стороне сервера включает пакет выделения RPCSS.

## <a name="examples"></a>Примеры

**MIDL/рпксс filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**включить \_ выделение**](enable-allocate.md)
</dt> <dt>

[**/осф**](-osf.md)
</dt> </dl>

 

 




