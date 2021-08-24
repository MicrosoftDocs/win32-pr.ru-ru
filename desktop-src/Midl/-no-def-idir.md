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
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811304"
---
# <a name="no_def_idir-switch"></a>\_ \_ коммутатор идир/но DEF

При указании каталогов с параметром [**/i**](-i.md) параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только каталоги, указанные с помощью параметра **/i** , игнорируя текущий каталог, а также каталоги, заданные переменной среды include.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

Если с параметром [**/i**](-i.md) не указаны каталоги, параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только текущий каталог.

## <a name="examples"></a>Примеры

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/акф**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




