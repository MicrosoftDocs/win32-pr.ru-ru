---
title: /out - параметр
description: Параметр/out указывает каталог по умолчанию, в который компилятор MIDL записывает выходные файлы.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- параметр/out MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672223"
---
# <a name="out-switch"></a>/out - параметр

Параметр **/out** указывает каталог по умолчанию, в который компилятор MIDL записывает выходные файлы.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*Спецификация пути* 
</dt> <dd>

Указывает путь к каталогу, в котором создаются файлы-заглушки, заголовков и переключателей. Можно указать спецификацию диска, абсолютный путь к каталогу или и то, и другое. Пути можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Выходной каталог можно указать с помощью буквы диска, имени абсолютного пути или и того и другого. Параметр **/out** можно использовать с любыми параметрами, включающими спецификацию отдельного выходного файла.

Если параметр **/out** не указан, файлы записываются в текущий каталог.

Каталог по умолчанию, заданный параметром **/out** , может быть переопределен путем явного указания пути, указанного как часть параметра [**/cstub**](-cstub.md), [**/Header**](-header.md), [**/proxy**](-proxy.md)или [**/sstub**](-sstub.md) .

## <a name="examples"></a>Примеры

**MIDL/out c: \\ MyDir \\ мисубдир \\ SubDir2 глубже filename. idl**

**MIDL/out c: filename. idl**

**MIDL/out \\ MyDir \\ мисубдир \\ другое filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/Proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




