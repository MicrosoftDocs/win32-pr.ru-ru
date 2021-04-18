---
title: Поиск файлов
description: По умолчанию версия-кандидат выполняет поиск файлов заголовков и файлов ресурсов (таких как файлы значков и курсоров) в текущем каталоге, а затем в каталогах, заданных переменной среды INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700643"
---
# <a name="searching-for-files"></a><span data-ttu-id="c18d5-103">Поиск файлов</span><span class="sxs-lookup"><span data-stu-id="c18d5-103">Searching for Files</span></span>

<span data-ttu-id="c18d5-104">По умолчанию версия-кандидат выполняет поиск файлов заголовков и файлов ресурсов (таких как файлы значков и курсоров) в текущем каталоге, а затем в каталогах, заданных переменной среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="c18d5-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="c18d5-105">(Переменная среды PATH не влияет на каталоги, поиск которых выполняется в RC.)</span><span class="sxs-lookup"><span data-stu-id="c18d5-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="c18d5-106">Добавление каталога для поиска</span><span class="sxs-lookup"><span data-stu-id="c18d5-106">Adding a Directory to Search</span></span>

<span data-ttu-id="c18d5-107">С помощью параметра **/i** можно добавить каталог в список каталогов поиска RC.</span><span class="sxs-lookup"><span data-stu-id="c18d5-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="c18d5-108">Затем компилятор выполняет поиск в каталогах в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="c18d5-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="c18d5-109">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c18d5-109">The current directory</span></span>
2.  <span data-ttu-id="c18d5-110">Каталог или каталоги, указанные с помощью параметра **/i** , в том порядке, в котором они отображаются в командной строке RC.</span><span class="sxs-lookup"><span data-stu-id="c18d5-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="c18d5-111">Список каталогов, заданных переменной среды INCLUDE, в порядке их перечисления в переменной, если не указан параметр **/x**</span><span class="sxs-lookup"><span data-stu-id="c18d5-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="c18d5-112">В следующем примере компилируется файл определения ресурса MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="c18d5-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="c18d5-113">**RC/i c: \\ Источник: \\ /i d: \\ Resources MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="c18d5-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="c18d5-114">При компиляции скрипта MyApp. RC версия-кандидат ищет файлы заголовков и файлы ресурсов в текущем каталоге, затем в C: \\ Источник \\ и D: \\ Resources, а затем в каталогах, заданных переменной среды include.</span><span class="sxs-lookup"><span data-stu-id="c18d5-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="c18d5-115">Пропуск переменной среды INCLUDE</span><span class="sxs-lookup"><span data-stu-id="c18d5-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="c18d5-116">При определении каталогов для поиска в версии-КАНДИДАТе можно запретить использовать переменную среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="c18d5-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="c18d5-117">Для этого используйте параметр **/x** .</span><span class="sxs-lookup"><span data-stu-id="c18d5-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="c18d5-118">Затем компилятор ищет файлы только в текущем каталоге и в любых каталогах, указанных с помощью параметра **/i** .</span><span class="sxs-lookup"><span data-stu-id="c18d5-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="c18d5-119">Следующая команда компилирует файл скрипта MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="c18d5-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="c18d5-120">**RC/x/i c: \\ Источник \\ материалов MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="c18d5-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="c18d5-121">При компиляции скрипта MyApp. RC версия-кандидат сначала ищет файлы заголовков и файлы ресурсов в текущем каталоге, а затем в C: \\ Источник \\ .</span><span class="sxs-lookup"><span data-stu-id="c18d5-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="c18d5-122">Он не выполняет поиск в каталогах, заданных переменной среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="c18d5-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




