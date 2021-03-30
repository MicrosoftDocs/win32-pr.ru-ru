---
title: Сведения о файлах ресурсов
description: Описывает, как включить ресурсы в приложение Windows с помощью версии-КАНДИДАТа.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067979"
---
# <a name="about-resource-files"></a><span data-ttu-id="2c15e-103">Сведения о файлах ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c15e-103">About Resource Files</span></span>

<span data-ttu-id="2c15e-104">Чтобы включить ресурсы в приложение Windows с помощью версии-КАНДИДАТа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2c15e-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="2c15e-105">Создание отдельных файлов для курсоров, значков, растровых изображений, диалоговых окон и шрифтов.</span><span class="sxs-lookup"><span data-stu-id="2c15e-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="2c15e-106">Создайте скрипт определения ресурса (RC-файл), описывающий ресурсы, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="2c15e-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="2c15e-107">Скомпилируйте скрипт с RC.</span><span class="sxs-lookup"><span data-stu-id="2c15e-107">Compile the script with RC.</span></span> <span data-ttu-id="2c15e-108">Дополнительные сведения см. [в разделе Использование версии-кандидата (Командная строка RC)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="2c15e-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="2c15e-109">Свяжите файл скомпилированного ресурса (RES) с исполняемым файлом приложения с вашим компоновщиком.</span><span class="sxs-lookup"><span data-stu-id="2c15e-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="2c15e-110">Файл ресурсов — это текстовый файл с расширением RC.</span><span class="sxs-lookup"><span data-stu-id="2c15e-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="2c15e-111">Файл может использовать однобайтовые, двухбайтовые или символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="2c15e-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="2c15e-112">Синтаксис и семантика предварительной версии RC аналогичны компиляторам Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="2c15e-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="2c15e-113">Однако версия-кандидат поддерживает подмножество директив препроцессора, определяет и директивы pragma в скрипте.</span><span class="sxs-lookup"><span data-stu-id="2c15e-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="2c15e-114">В файле скрипта определяются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2c15e-114">The script file defines resources.</span></span> <span data-ttu-id="2c15e-115">Для ресурса, который существует в отдельном файле, таком как значок или курсор, сценарий указывает ресурс и файл, который его содержит.</span><span class="sxs-lookup"><span data-stu-id="2c15e-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="2c15e-116">Для некоторых ресурсов, таких как меню, в сценарии существует полное определение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c15e-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="2c15e-117">В следующих разделах описываются сведения, которые может содержать файл скрипта:</span><span class="sxs-lookup"><span data-stu-id="2c15e-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="2c15e-118">[Комментарии](comments.md), которые должны игнорироваться версией-кандидатом.</span><span class="sxs-lookup"><span data-stu-id="2c15e-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="2c15e-119">[Предопределенные макросы](predefined-macros.md), которые не принимают аргументы и не могут быть переопределены.</span><span class="sxs-lookup"><span data-stu-id="2c15e-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="2c15e-120">[Директивы препроцессора](preprocessor-directives.md), которые указывают RC на выполнение действий над сценарием перед его компиляцией.</span><span class="sxs-lookup"><span data-stu-id="2c15e-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="2c15e-121">[Операторы препроцессора](preprocessor-operators.md), которые используются с директивой **\# define** .</span><span class="sxs-lookup"><span data-stu-id="2c15e-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="2c15e-122">Директивы Pragma</span><span class="sxs-lookup"><span data-stu-id="2c15e-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="2c15e-123">[Операторы определения ресурсов](resource-definition-statements.md), которые содержат имена и описания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c15e-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




