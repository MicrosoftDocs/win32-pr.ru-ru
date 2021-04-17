---
title: /Header, параметр
description: Параметр/header указывает имя файла заголовка.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- MIDL/Header Switch
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411898"
---
# <a name="header-switch"></a><span data-ttu-id="fc450-104">/Header, параметр</span><span class="sxs-lookup"><span data-stu-id="fc450-104">/header switch</span></span>

<span data-ttu-id="fc450-105">Параметр **/Header** указывает имя файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="fc450-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="fc450-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="fc450-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fc450-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="fc450-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="fc450-108">Задает имя файла заголовка, переопределяющего имя файла заголовка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc450-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="fc450-109">Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="fc450-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc450-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc450-110">Remarks</span></span>

<span data-ttu-id="fc450-111">Указанное имя файла заменяет имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc450-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="fc450-112">Имя файла по умолчанию получается путем замены расширения IDL (обычно IDL) именем файла Extension. h.</span><span class="sxs-lookup"><span data-stu-id="fc450-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="fc450-113">Для интерфейсов OLE параметр **/Header** переопределяет имя файла заголовка интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc450-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="fc450-114">При импорте файлов указанное имя файла применяется только к одному файлу заголовка — файлу заголовка, соответствующему IDL-файлу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="fc450-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="fc450-115">Если *имя_файла* не включает явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="fc450-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="fc450-116">Явный путь в *filename* переопределяет спецификацию переключателя **/out** .</span><span class="sxs-lookup"><span data-stu-id="fc450-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="fc450-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="fc450-117">Examples</span></span>

<span data-ttu-id="fc450-118">**MIDL/Header "Bar. h" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="fc450-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fc450-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc450-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc450-120">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="fc450-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc450-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="fc450-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="fc450-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="fc450-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="fc450-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="fc450-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="fc450-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="fc450-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="fc450-125">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="fc450-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




