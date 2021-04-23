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
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784227"
---
# <a name="dlldata-switch"></a><span data-ttu-id="710a8-105">/dlldata, параметр</span><span class="sxs-lookup"><span data-stu-id="710a8-105">/dlldata switch</span></span>

<span data-ttu-id="710a8-106">Параметр **/dlldata** используется для указания имени файла для созданного файла DLLDATA для прокси-библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="710a8-107">Если не указан параметр **/dlldata** , используется имя файла по умолчанию DLLDATA. c.</span><span class="sxs-lookup"><span data-stu-id="710a8-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="710a8-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="710a8-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="710a8-109">*имя файла*</span><span class="sxs-lookup"><span data-stu-id="710a8-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="710a8-110">Имя исходного файла C, который будет создан компилятором MIDL для прокси-библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="710a8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="710a8-111">Remarks</span></span>

<span data-ttu-id="710a8-112">Файл, указанный параметром *File-Name* , должен быть связан с DLL-библиотекой прокси.</span><span class="sxs-lookup"><span data-stu-id="710a8-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="710a8-113">Файл dlldata содержит точки входа и структуры данных, необходимые фабрике классов для прокси-библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="710a8-114">Эти структуры данных указывают интерфейсы объектов, содержащиеся в прокси-библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="710a8-115">Файл dlldata также указывает идентификатор класса фабрики класса для прокси-библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="710a8-116">Это всегда идентификатор UUID первого интерфейса первого прокси-файла (в алфавитном порядке).</span><span class="sxs-lookup"><span data-stu-id="710a8-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="710a8-117">Один и тот же файл dlldata должен быть указан при вызове MIDL для всех IDL-файлов, которые будут передаваться в конкретную библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="710a8-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="710a8-118">Файл dlldata создается или обновляется во время каждой компиляции MIDL, постепенно создавая список интерфейсов, которые попадают в библиотеку DLL прокси.</span><span class="sxs-lookup"><span data-stu-id="710a8-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="710a8-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="710a8-119">Examples</span></span>

<span data-ttu-id="710a8-120">**MIDL/dlldata Data. c**</span><span class="sxs-lookup"><span data-stu-id="710a8-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="710a8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="710a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710a8-122">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="710a8-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




