---
title: Команда файла ответа
description: Файл ответов — это текстовый файл, содержащий один или несколько параметров командной строки компилятора MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Справочник по командной строке MIDL, команда файла ответа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986724"
---
# <a name="the-response-file-command"></a><span data-ttu-id="941bc-104">Команда файла ответа</span><span class="sxs-lookup"><span data-stu-id="941bc-104">The Response File Command</span></span>

<span data-ttu-id="941bc-105">Файл ответов — это текстовый файл, содержащий один или несколько параметров командной строки компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="941bc-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="941bc-106">В отличие от командной строки, файл ответов допускает несколько строк параметров и имен файлов.</span><span class="sxs-lookup"><span data-stu-id="941bc-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="941bc-107">Это может быть полезно из-за ограничений среды сборки или в качестве удобства для процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="941bc-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="941bc-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="941bc-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="941bc-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*\_файл ответов*</span><span class="sxs-lookup"><span data-stu-id="941bc-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="941bc-110">Указывает имя файла ответов.</span><span class="sxs-lookup"><span data-stu-id="941bc-110">Specifies the name of a response file.</span></span> <span data-ttu-id="941bc-111">Имя файла ответа должно следовать сразу за символом @.</span><span class="sxs-lookup"><span data-stu-id="941bc-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="941bc-112">Между символом @ и именем файла ответа пробелы не допускаются.</span><span class="sxs-lookup"><span data-stu-id="941bc-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="941bc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="941bc-113">Remarks</span></span>

<span data-ttu-id="941bc-114">В качестве альтернативы размещению всех параметров, связанных с параметром в командной строке, компилятор MIDL принимает файлы ответов, содержащие переключатели и аргументы.</span><span class="sxs-lookup"><span data-stu-id="941bc-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="941bc-115">Параметры в файле ответов обрабатываются так, как если бы они присутствовали в этом расположении в командной строке MIDL.</span><span class="sxs-lookup"><span data-stu-id="941bc-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="941bc-116">Каждый аргумент в файле ответов должен начинаться и заканчиваться на одной строке.</span><span class="sxs-lookup"><span data-stu-id="941bc-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="941bc-117">Символ обратной косой черты ( \) не может использоваться для сцепления линий.</span><span class="sxs-lookup"><span data-stu-id="941bc-117">The backslash character (\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="941bc-118">Если строка является частью заключенной в кавычки строки в файле ответов, то символ обратной косой черты можно использовать только перед другой обратной косой чертой или перед символом двойной кавычки (").</span><span class="sxs-lookup"><span data-stu-id="941bc-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="941bc-119">Если строка не является частью заключенной в кавычки строки, то символ обратной косой черты можно использовать только до символа двойной кавычки.</span><span class="sxs-lookup"><span data-stu-id="941bc-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="941bc-120">MIDL поддерживает аргументы командной строки, включающие один или несколько файлов ответов в сочетании с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="941bc-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="941bc-121">Компилятор MIDL не поддерживает вложенные файлы ответов.</span><span class="sxs-lookup"><span data-stu-id="941bc-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="941bc-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="941bc-122">Examples</span></span>

<span data-ttu-id="941bc-123">**MIDL @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="941bc-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="941bc-124">**MIDL-Оикф @midl1.rsp -env Win32 @midl2.rsp ИТФ. idl**</span><span class="sxs-lookup"><span data-stu-id="941bc-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="941bc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="941bc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="941bc-126">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="941bc-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




