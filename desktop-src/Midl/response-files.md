---
title: Файлы ответов
description: В качестве альтернативы размещению всех параметров в командной строке компилятор MIDL принимает файлы ответов, содержащие переключатели и аргументы.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL компилятора MIDL, файлы ответов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387075"
---
# <a name="response-files"></a><span data-ttu-id="e1f06-104">Файлы ответов</span><span class="sxs-lookup"><span data-stu-id="e1f06-104">Response Files</span></span>

<span data-ttu-id="e1f06-105">В качестве альтернативы размещению всех параметров в командной строке компилятор MIDL принимает файлы ответов, содержащие переключатели и аргументы.</span><span class="sxs-lookup"><span data-stu-id="e1f06-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="e1f06-106">Файл ответов — это текстовый файл, содержащий один или несколько параметров командной строки компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="e1f06-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="e1f06-107">В отличие от командной строки, файл ответов допускает несколько строк параметров и имен файлов.</span><span class="sxs-lookup"><span data-stu-id="e1f06-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="e1f06-108">Это может быть полезно из-за ограничений среды сборки или в качестве удобства для процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="e1f06-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="e1f06-109">Файл ответов MIDL можно указать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e1f06-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="e1f06-110"> **\@ имя файла** MIDL</span><span class="sxs-lookup"><span data-stu-id="e1f06-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="e1f06-111"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="e1f06-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="e1f06-112">Указывает имя файла ответов.</span><span class="sxs-lookup"><span data-stu-id="e1f06-112">Specifies the name of the response file.</span></span> <span data-ttu-id="e1f06-113">Имя файла ответа должно сразу следовать за символом @ без пробелов между символом @ и именем файла ответа.</span><span class="sxs-lookup"><span data-stu-id="e1f06-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="e1f06-114">Параметры в файле ответов обрабатываются так, как если бы они присутствовали в этом месте в командной строке MIDL.</span><span class="sxs-lookup"><span data-stu-id="e1f06-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="e1f06-115">Каждый аргумент в файле ответов должен начинаться и заканчиваться на одной строке.</span><span class="sxs-lookup"><span data-stu-id="e1f06-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="e1f06-116">Нельзя использовать символ обратной косой черты ( \\ ) для сцепления строк.</span><span class="sxs-lookup"><span data-stu-id="e1f06-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="e1f06-117">MIDL поддерживает аргументы командной строки, включающие один или несколько файлов ответов в сочетании с другими параметрами командной строки:</span><span class="sxs-lookup"><span data-stu-id="e1f06-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="e1f06-118">**MIDL-Оикф @midl1.rsp -envwin32 @midl2.rsp ИТФ. idl**</span><span class="sxs-lookup"><span data-stu-id="e1f06-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="e1f06-119">Компилятор MIDL не поддерживает вложенные файлы ответов.</span><span class="sxs-lookup"><span data-stu-id="e1f06-119">The MIDL compiler does not support nested response files.</span></span>

 

 




