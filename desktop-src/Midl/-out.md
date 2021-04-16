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
# <a name="out-switch"></a><span data-ttu-id="def75-104">/out - параметр</span><span class="sxs-lookup"><span data-stu-id="def75-104">/out switch</span></span>

<span data-ttu-id="def75-105">Параметр **/out** указывает каталог по умолчанию, в который компилятор MIDL записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="def75-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="def75-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="def75-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="def75-107">*Спецификация пути*</span><span class="sxs-lookup"><span data-stu-id="def75-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="def75-108">Указывает путь к каталогу, в котором создаются файлы-заглушки, заголовков и переключателей.</span><span class="sxs-lookup"><span data-stu-id="def75-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="def75-109">Можно указать спецификацию диска, абсолютный путь к каталогу или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="def75-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="def75-110">Пути можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="def75-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="def75-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="def75-111">Remarks</span></span>

<span data-ttu-id="def75-112">Выходной каталог можно указать с помощью буквы диска, имени абсолютного пути или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="def75-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="def75-113">Параметр **/out** можно использовать с любыми параметрами, включающими спецификацию отдельного выходного файла.</span><span class="sxs-lookup"><span data-stu-id="def75-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="def75-114">Если параметр **/out** не указан, файлы записываются в текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="def75-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="def75-115">Каталог по умолчанию, заданный параметром **/out** , может быть переопределен путем явного указания пути, указанного как часть параметра [**/cstub**](-cstub.md), [**/Header**](-header.md), [**/proxy**](-proxy.md)или [**/sstub**](-sstub.md) .</span><span class="sxs-lookup"><span data-stu-id="def75-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="def75-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="def75-116">Examples</span></span>

<span data-ttu-id="def75-117">**MIDL/out c: \\ MyDir \\ мисубдир \\ SubDir2 глубже filename. idl**</span><span class="sxs-lookup"><span data-stu-id="def75-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="def75-118">**MIDL/out c: filename. idl**</span><span class="sxs-lookup"><span data-stu-id="def75-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="def75-119">**MIDL/out \\ MyDir \\ мисубдир \\ другое filename. idl**</span><span class="sxs-lookup"><span data-stu-id="def75-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="def75-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="def75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def75-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="def75-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="def75-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="def75-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="def75-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="def75-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="def75-124">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="def75-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="def75-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="def75-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




