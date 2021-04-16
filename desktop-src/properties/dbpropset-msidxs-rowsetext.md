---
description: Расширяет свойства, определенные для интерфейсов API набора строк.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702791"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ мсидксс \_ ровсетекст

Расширяет свойства, определенные для интерфейсов API набора строк.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

\_ \_ Набор свойств DBPROPSET мсидксс ровсетекст содержит следующие константы свойств:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>МСИДКССПРОП \_ ровсеткуеристатус
</dt> <dd>

Идентификатор свойства 2. Состояние запроса для набора строк. \_ \* Константы stat указывают состояние выполнения и надежности.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_ \_ строка локали команды мсидксспроп \_
</dt> <dd>

Идентификатор свойства 3. Строка языкового стандарта, представляющая язык и региональные параметры, используемые для этого набора строк.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_Ограничение запроса \_ мсидксспроп
</dt> <dd>

Идентификатор свойства 4. Строка запроса, связанная с этим набором строк.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_дерево синтаксического анализа мсидксспроп \_
</dt> <dd>

Идентификатор свойства 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>МСИДКССПРОП \_ максимальный \_ ранг 
</dt> <dd>

Идентификатор свойства 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>\_найдены результаты \_ мсидксспроп
</dt> <dd>

Идентификатор свойства 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>МСИДКССПРОП \_ вхереид
</dt> <dd>

Идентификатор свойства 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_версия сервера \_ мсидксспроп 
</dt> <dd>

Новые для Windows 7. Идентификатор свойства 9. Версия сервера.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>МСИДКССПРОП \_ Server \_ WINVER \_ Major
</dt> <dd>

Идентификатор свойства 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>МСИДКССПРОП \_ Server \_ WINVER \_ минор
</dt> <dd>

Идентификатор свойства 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>МСИДКССПРОП \_ Server \_ нлсверсион
</dt> <dd>

Идентификатор свойства 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>МСИДКССПРОП \_ сервер \_ нлсвер \_ определен 
</dt> <dd>

Идентификатор свойства 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>МСИДКССПРОП \_ те \_ же \_ использованные сортировки 
</dt> <dd>

Идентификатор свойства 14.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы запросить \_ версию сервера мсидксспроп \_ , необходимо выдать фиктивный запрос к серверу, как показано в следующем примере.

`SELECT top 1 workid from servername.systemindex`

После возврата набора строк вызовите метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для возможностей набора строк, а затем вызовите метод [ировсетинфо::-Properties](/previous-versions/windows/desktop/ms719611(v=vs.85)) для нового свойства ( \_ версия сервера мсидксспроп \_ ). Свойство имеет тип **VT \_ I4** и может принимать одно из следующих значений:

\#определение CI \_ версии \_ WDS30 0x102//258

\#определение CI \_ версии \_ WDS40 0x109//265

\#определение CI \_ версии \_ WIN70 0X700//1792

После того как значение известно, клиент может сформировать запрос, который поддерживается сервером, и выдать реальный запрос.

DBPROPSET \_ мсидксс \_ ровсетекст объявляется в нткуери. h.

 

 
