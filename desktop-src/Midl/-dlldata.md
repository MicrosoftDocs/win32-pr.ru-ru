---
title: /dlldata, параметр
description: Параметр/dlldata используется для указания имени файла для созданного файла DLLDATA для прокси-библиотеки DLL. Если не указан параметр/dlldata, используется имя файла по умолчанию DLLDATA. c.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- MIDL/dlldata Switch
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105644"
---
# <a name="dlldata-switch"></a>/dlldata, параметр

Параметр **/dlldata** используется для указания имени файла для созданного файла DLLDATA для прокси-библиотеки DLL. Если не указан параметр **/dlldata** , используется имя файла по умолчанию DLLDATA. c.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*имя файла* 
</dt> <dd>

Имя исходного файла C, который будет создан компилятором MIDL для прокси-библиотеки DLL.

</dd> </dl>

## <a name="remarks"></a>Remarks

Файл, указанный параметром *File-Name* , должен быть связан с DLL-библиотекой прокси. Файл dlldata содержит точки входа и структуры данных, необходимые фабрике классов для прокси-библиотеки DLL. Эти структуры данных указывают интерфейсы объектов, содержащиеся в прокси-библиотеке DLL. Файл dlldata также указывает идентификатор класса фабрики класса для прокси-библиотеки DLL. Это всегда идентификатор UUID первого интерфейса первого прокси-файла (в алфавитном порядке).

Один и тот же файл dlldata должен быть указан при вызове MIDL для всех IDL-файлов, которые будут передаваться в конкретную библиотеку DLL. Файл dlldata создается или обновляется во время каждой компиляции MIDL, постепенно создавая список интерфейсов, которые попадают в библиотеку DLL прокси.

## <a name="examples"></a>Примеры

**MIDL/dlldata Data. c**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




