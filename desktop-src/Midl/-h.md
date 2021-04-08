---
title: Параметр/h
description: Параметр/h функционально эквивалентен параметру/Header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h Switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069097"
---
# <a name="h-switch"></a>Параметр/h

Параметр **/h** функционально эквивалентен параметру [**/Header**](-header.md) .

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*filename* 
</dt> <dd>

Задает имя файла заголовка, переопределяющего имя файла заголовка по умолчанию. Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр **/h** указывает *filename* в качестве имени файла заголовка, содержащего все определения, содержащиеся в IDL-файле, без синтаксиса IDL. Этот файл можно использовать в качестве заголовочного файла C или C++.

## <a name="examples"></a>Примеры

**MIDL/h тлибхеад. h filename. idl**

**MIDL/h "MIDL. h" имя_файла. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> </dl>

 

 




