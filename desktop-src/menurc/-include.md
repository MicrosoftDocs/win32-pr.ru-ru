---
title: " include"
description: Директива \ include заставляет компилятор ресурсов обработать файл, указанный в параметре filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414641"
---
# <a name="-include"></a><span data-ttu-id="58abc-103">относится</span><span class="sxs-lookup"><span data-stu-id="58abc-103">' include'</span></span>

<span data-ttu-id="58abc-104">Директива **\# include** заставляет компилятор ресурсов обработать файл, указанный в параметре *filename* .</span><span class="sxs-lookup"><span data-stu-id="58abc-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="58abc-105">Этот файл должен быть файлом заголовка, который определяет константы, используемые в файле определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="58abc-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="58abc-106">Файл может использовать однобайтовые, двухбайтовые или символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="58abc-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="58abc-107"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="58abc-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="58abc-108">Имя включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="58abc-108">Name of the file to be included.</span></span> <span data-ttu-id="58abc-109">Если файл находится в текущем каталоге, строка должна быть заключена в двойные кавычки. Если файл находится в каталоге, указанном переменной среды INCLUDE, строка должна быть заключена в символы «меньше» и «больше» (<>).</span><span class="sxs-lookup"><span data-stu-id="58abc-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="58abc-110">Необходимо указать полный путь, заключенный в двойные кавычки ("), если файл не находится в текущем каталоге или в каталоге, указанном переменной среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="58abc-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58abc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58abc-111">Remarks</span></span>

<span data-ttu-id="58abc-112">Используйте следующую инструкцию в файле заголовка, чтобы окружить инструкции, которые могут быть скомпилированы компилятором C, но не версией-КАНДИДАТом:</span><span class="sxs-lookup"><span data-stu-id="58abc-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="58abc-113">Таким образом можно использовать те же включаемые файлы в файлах c и RC.</span><span class="sxs-lookup"><span data-stu-id="58abc-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="58abc-114">Пример</span><span class="sxs-lookup"><span data-stu-id="58abc-114">Example</span></span>

<span data-ttu-id="58abc-115">В этом примере производится обработка файлов заголовков Windows. h и Мидефс. h при компиляции файла определения ресурса:</span><span class="sxs-lookup"><span data-stu-id="58abc-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="58abc-116">См. также</span><span class="sxs-lookup"><span data-stu-id="58abc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58abc-117">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="58abc-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




