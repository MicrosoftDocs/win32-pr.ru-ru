---
title: /sstub, параметр
description: Параметр/sstub указывает имя файла заглушки сервера для интерфейса RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- MIDL/sstub Switch
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672220"
---
# <a name="sstub-switch"></a><span data-ttu-id="511fc-104">/sstub, параметр</span><span class="sxs-lookup"><span data-stu-id="511fc-104">/sstub switch</span></span>

<span data-ttu-id="511fc-105">Параметр **/sstub** указывает имя файла заглушки сервера для интерфейса RPC.</span><span class="sxs-lookup"><span data-stu-id="511fc-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="511fc-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="511fc-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="511fc-107">*\_имя файла-заглушки \_*</span><span class="sxs-lookup"><span data-stu-id="511fc-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="511fc-108">Указывает имя файла, переопределяющего имя файла заглушки сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="511fc-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="511fc-109">Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="511fc-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="511fc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="511fc-110">Remarks</span></span>

<span data-ttu-id="511fc-111">Указанное имя файла заменяет имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="511fc-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="511fc-112">По умолчанию имя файла получается путем добавления \_ S. C к имени IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="511fc-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="511fc-113">Этот параметр не влияет на интерфейсы OLE.</span><span class="sxs-lookup"><span data-stu-id="511fc-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="511fc-114">При импорте файлов указанное имя файла применяется только к одному файлу заглушки — файлу заглушки, соответствующему IDL-файлу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="511fc-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="511fc-115">Если *\_ \_ имя файла-заглушки* не включает в себя явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="511fc-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="511fc-116">Явный путь в *\_ \_ имени файла-заглушки* переопределяет спецификацию переключателя **/out** .</span><span class="sxs-lookup"><span data-stu-id="511fc-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="511fc-117">Параметр **/Server** None имеет приоритет над параметром **/sstub** .</span><span class="sxs-lookup"><span data-stu-id="511fc-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="511fc-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="511fc-118">Examples</span></span>

<span data-ttu-id="511fc-119">**MIDL/sstub My \_ сстуб. c имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="511fc-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="511fc-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="511fc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511fc-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="511fc-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="511fc-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="511fc-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="511fc-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="511fc-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="511fc-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="511fc-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




