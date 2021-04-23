---
title: /cstub, параметр
description: Параметр/cstub указывает имя файла заглушки клиента для интерфейса RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- MIDL/cstub Switch
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334571"
---
# <a name="cstub-switch"></a><span data-ttu-id="8886f-104">/cstub, параметр</span><span class="sxs-lookup"><span data-stu-id="8886f-104">/cstub switch</span></span>

<span data-ttu-id="8886f-105">Параметр **/cstub** указывает имя файла заглушки клиента для интерфейса RPC.</span><span class="sxs-lookup"><span data-stu-id="8886f-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="8886f-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="8886f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="8886f-107">*\_имя файла-заглушки \_*</span><span class="sxs-lookup"><span data-stu-id="8886f-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="8886f-108">Указывает имя файла, переопределяющего имя файла заглушки клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8886f-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="8886f-109">Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="8886f-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8886f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8886f-110">Remarks</span></span>

<span data-ttu-id="8886f-111">Указанное имя файла заменяет имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8886f-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="8886f-112">По умолчанию имя файла получается путем добавления расширения \_ c. c к имени IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="8886f-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="8886f-113">Этот параметр не влияет на интерфейсы OLE.</span><span class="sxs-lookup"><span data-stu-id="8886f-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="8886f-114">При импорте файлов указанное имя файла применяется только к одному файлу заглушки — файлу заглушки, соответствующему IDL-файлу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="8886f-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="8886f-115">Если *\_ \_ имя файла-заглушки* не включает в себя явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="8886f-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="8886f-116">Явный путь в *\_ \_ имени файла-заглушки* переопределяет спецификацию переключателя **/out** .</span><span class="sxs-lookup"><span data-stu-id="8886f-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="8886f-117">Параметр **/Client** None имеет приоритет над параметром **/cstub** .</span><span class="sxs-lookup"><span data-stu-id="8886f-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="8886f-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="8886f-118">Examples</span></span>

<span data-ttu-id="8886f-119">**MIDL/cstub My \_ кстуб. c имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="8886f-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="8886f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8886f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8886f-121">**/Header**</span><span class="sxs-lookup"><span data-stu-id="8886f-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="8886f-122">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="8886f-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8886f-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="8886f-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="8886f-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="8886f-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




