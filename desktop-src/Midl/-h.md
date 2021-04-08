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
# <a name="h-switch"></a><span data-ttu-id="12387-104">Параметр/h</span><span class="sxs-lookup"><span data-stu-id="12387-104">/h switch</span></span>

<span data-ttu-id="12387-105">Параметр **/h** функционально эквивалентен параметру [**/Header**](-header.md) .</span><span class="sxs-lookup"><span data-stu-id="12387-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="12387-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="12387-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="12387-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="12387-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="12387-108">Задает имя файла заголовка, переопределяющего имя файла заголовка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12387-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="12387-109">Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="12387-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12387-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12387-110">Remarks</span></span>

<span data-ttu-id="12387-111">Параметр **/h** указывает *filename* в качестве имени файла заголовка, содержащего все определения, содержащиеся в IDL-файле, без синтаксиса IDL.</span><span class="sxs-lookup"><span data-stu-id="12387-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="12387-112">Этот файл можно использовать в качестве заголовочного файла C или C++.</span><span class="sxs-lookup"><span data-stu-id="12387-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="12387-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="12387-113">Examples</span></span>

<span data-ttu-id="12387-114">**MIDL/h тлибхеад. h filename. idl**</span><span class="sxs-lookup"><span data-stu-id="12387-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="12387-115">**MIDL/h "MIDL. h" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="12387-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="12387-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12387-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12387-117">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="12387-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="12387-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="12387-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




