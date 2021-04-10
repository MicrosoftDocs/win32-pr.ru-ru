---
title: /Proxy, параметр
description: Параметр/proxy указывает имя прокси-файла интерфейса для COM-интерфейса.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- MIDL/proxy Switch
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889824"
---
# <a name="proxy-switch"></a>/Proxy, параметр

Параметр **/proxy** указывает имя прокси-файла интерфейса для COM-интерфейса.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*\_имя файла прокси-сервера \_* 
</dt> <dd>

Указывает имя файла, переопределяющего имя файла прокси-сервера интерфейса по умолчанию. Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Указанное имя файла заменяет имя файла по умолчанию, полученное путем добавления \_ P. C к имени IDL-файла. Параметр/ [**proxy**](proxy.md) не влияет на интерфейсы RPC.

Если *\_ \_ имя файла прокси-сервера* не включает явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) . Явный путь в *\_ \_ имени файла прокси* переопределяет спецификацию переключателя **/out** .

Более подробное описание файла прокси интерфейса и других файлов, создаваемых компилятором MIDL, см. в разделе [Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md).

## <a name="examples"></a>Примеры

**MIDL/proxy My \_ proxy. c имя_файла. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




