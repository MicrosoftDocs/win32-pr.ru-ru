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
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="3242f-103">DBPROPSET \_ мсидксс \_ ровсетекст</span><span class="sxs-lookup"><span data-stu-id="3242f-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="3242f-104">Расширяет свойства, определенные для интерфейсов API набора строк.</span><span class="sxs-lookup"><span data-stu-id="3242f-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="3242f-105">\_ \_ Набор свойств DBPROPSET мсидксс ровсетекст содержит следующие константы свойств:</span><span class="sxs-lookup"><span data-stu-id="3242f-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="3242f-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>МСИДКССПРОП \_ ровсеткуеристатус</span><span class="sxs-lookup"><span data-stu-id="3242f-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="3242f-107">Идентификатор свойства 2.</span><span class="sxs-lookup"><span data-stu-id="3242f-107">Property ID 2.</span></span> <span data-ttu-id="3242f-108">Состояние запроса для набора строк.</span><span class="sxs-lookup"><span data-stu-id="3242f-108">Query status for the rowset.</span></span> <span data-ttu-id="3242f-109">\_ \* Константы stat указывают состояние выполнения и надежности.</span><span class="sxs-lookup"><span data-stu-id="3242f-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_ \_ строка локали команды мсидксспроп \_</span><span class="sxs-lookup"><span data-stu-id="3242f-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="3242f-111">Идентификатор свойства 3.</span><span class="sxs-lookup"><span data-stu-id="3242f-111">Property ID 3.</span></span> <span data-ttu-id="3242f-112">Строка языкового стандарта, представляющая язык и региональные параметры, используемые для этого набора строк.</span><span class="sxs-lookup"><span data-stu-id="3242f-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_Ограничение запроса \_ мсидксспроп</span><span class="sxs-lookup"><span data-stu-id="3242f-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="3242f-114">Идентификатор свойства 4.</span><span class="sxs-lookup"><span data-stu-id="3242f-114">Property ID 4.</span></span> <span data-ttu-id="3242f-115">Строка запроса, связанная с этим набором строк.</span><span class="sxs-lookup"><span data-stu-id="3242f-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_дерево синтаксического анализа мсидксспроп \_</span><span class="sxs-lookup"><span data-stu-id="3242f-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="3242f-117">Идентификатор свойства 5.</span><span class="sxs-lookup"><span data-stu-id="3242f-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>МСИДКССПРОП \_ максимальный \_ ранг</span><span class="sxs-lookup"><span data-stu-id="3242f-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="3242f-119">Идентификатор свойства 6.</span><span class="sxs-lookup"><span data-stu-id="3242f-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>\_найдены результаты \_ мсидксспроп</span><span class="sxs-lookup"><span data-stu-id="3242f-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="3242f-121">Идентификатор свойства 7.</span><span class="sxs-lookup"><span data-stu-id="3242f-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>МСИДКССПРОП \_ вхереид</span><span class="sxs-lookup"><span data-stu-id="3242f-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="3242f-123">Идентификатор свойства 8.</span><span class="sxs-lookup"><span data-stu-id="3242f-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_версия сервера \_ мсидксспроп</span><span class="sxs-lookup"><span data-stu-id="3242f-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="3242f-125">Новые для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3242f-125">New for Windows 7.</span></span> <span data-ttu-id="3242f-126">Идентификатор свойства 9.</span><span class="sxs-lookup"><span data-stu-id="3242f-126">Property ID 9.</span></span> <span data-ttu-id="3242f-127">Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="3242f-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>МСИДКССПРОП \_ Server \_ WINVER \_ Major</span><span class="sxs-lookup"><span data-stu-id="3242f-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="3242f-129">Идентификатор свойства 10.</span><span class="sxs-lookup"><span data-stu-id="3242f-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>МСИДКССПРОП \_ Server \_ WINVER \_ минор</span><span class="sxs-lookup"><span data-stu-id="3242f-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="3242f-131">Идентификатор свойства 11.</span><span class="sxs-lookup"><span data-stu-id="3242f-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>МСИДКССПРОП \_ Server \_ нлсверсион</span><span class="sxs-lookup"><span data-stu-id="3242f-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="3242f-133">Идентификатор свойства 12.</span><span class="sxs-lookup"><span data-stu-id="3242f-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>МСИДКССПРОП \_ сервер \_ нлсвер \_ определен</span><span class="sxs-lookup"><span data-stu-id="3242f-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="3242f-135">Идентификатор свойства 13.</span><span class="sxs-lookup"><span data-stu-id="3242f-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="3242f-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>МСИДКССПРОП \_ те \_ же \_ использованные сортировки</span><span class="sxs-lookup"><span data-stu-id="3242f-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="3242f-137">Идентификатор свойства 14.</span><span class="sxs-lookup"><span data-stu-id="3242f-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3242f-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3242f-138">Remarks</span></span>

<span data-ttu-id="3242f-139">Чтобы запросить \_ версию сервера мсидксспроп \_ , необходимо выдать фиктивный запрос к серверу, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3242f-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="3242f-140">После возврата набора строк вызовите метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для возможностей набора строк, а затем вызовите метод [ировсетинфо::-Properties](/previous-versions/windows/desktop/ms719611(v=vs.85)) для нового свойства ( \_ версия сервера мсидксспроп \_ ).</span><span class="sxs-lookup"><span data-stu-id="3242f-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="3242f-141">Свойство имеет тип **VT \_ I4** и может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3242f-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="3242f-142">\#определение CI \_ версии \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="3242f-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="3242f-143">\#определение CI \_ версии \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="3242f-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="3242f-144">\#определение CI \_ версии \_ WIN70 0X700//1792</span><span class="sxs-lookup"><span data-stu-id="3242f-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="3242f-145">После того как значение известно, клиент может сформировать запрос, который поддерживается сервером, и выдать реальный запрос.</span><span class="sxs-lookup"><span data-stu-id="3242f-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="3242f-146">DBPROPSET \_ мсидксс \_ ровсетекст объявляется в нткуери. h.</span><span class="sxs-lookup"><span data-stu-id="3242f-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
