---
title: /IID, параметр
description: Параметр/IID указывает имя файла идентификатора интерфейса для COM-интерфейса, переопределяя имя по умолчанию, полученное путем добавления \_ i. c к имени IDL-файла.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL/IID Switch
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411896"
---
# <a name="iid-switch"></a>/IID, параметр

Параметр **/IID** указывает имя файла идентификатора интерфейса для COM-интерфейса, переопределяя имя по умолчанию, полученное путем добавления \_ i. c к имени IDL-файла.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*filename* 
</dt> <dd>

Указывает имя файла идентификатора интерфейса, переопределяющего имя файла идентификатора интерфейса по умолчанию для COM-интерфейса. Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр **/IID** не влияет на интерфейсы RPC.

Если *имя_файла* не включает явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) . Явный путь в *filename* переопределяет спецификацию переключателя **/out** .

## <a name="examples"></a>Примеры

**MIDL/IID "My \_ IID. c" имя_файла. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/Proxy**](-proxy.md)
</dt> </dl>

 

 




