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
ms.openlocfilehash: 6dc3483706369837d96d14cf30b2f0c6ee307e376f8c422e11d56e06451a22e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811214"
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

## <a name="remarks"></a>Remarks

Указанное имя файла заменяет имя файла по умолчанию, полученное путем добавления \_ P. C к имени IDL-файла. Параметр/ [**proxy**](proxy.md) не влияет на интерфейсы RPC.

Если *\_ \_ имя файла прокси-сервера* не включает явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) . Явный путь в *\_ \_ имени файла прокси* переопределяет спецификацию переключателя **/out** .

Более подробное описание файла прокси интерфейса и других файлов, создаваемых компилятором MIDL, см. в разделе [Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md).

## <a name="examples"></a>Примеры

**MIDL/proxy My \_ proxy. c имя_файла. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




