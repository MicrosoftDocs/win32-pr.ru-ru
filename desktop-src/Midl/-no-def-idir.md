---
title: no_def_idir Switch
description: При указании каталогов с параметром/I \_ параметр идир/но DEF \_ предписывает компилятору MIDL искать только каталоги, указанные с помощью параметра/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir параметр MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889820"
---
# <a name="no_def_idir-switch"></a>\_ \_ коммутатор идир/но DEF

При указании каталогов с параметром [**/i**](-i.md) параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только каталоги, указанные с помощью параметра **/i** , игнорируя текущий каталог, а также каталоги, заданные переменной среды include.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

Если с параметром [**/i**](-i.md) не указаны каталоги, параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только текущий каталог.

## <a name="examples"></a>Примеры

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/акф**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




