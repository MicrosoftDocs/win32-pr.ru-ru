---
description: Включает содержимое одного MOF-файла в другой MOF-файл.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693552"
---
# <a name="include"></a><span data-ttu-id="8f8ac-103">"#include"</span><span class="sxs-lookup"><span data-stu-id="8f8ac-103">'#include'</span></span>
<span data-ttu-id="8f8ac-104">/\* Заголовок: Мимоф. mof                           *//*   Title: MyMof2. mof \*/</span><span class="sxs-lookup"><span data-stu-id="8f8ac-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="8f8ac-105">\#Команда "включить препроцессор" включает содержимое одного MOF-файла в другой MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="8f8ac-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="8f8ac-106">В следующем примере кода описывается синтаксис \# команды include.</span><span class="sxs-lookup"><span data-stu-id="8f8ac-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="8f8ac-107">В предыдущем примере Моффиле. MOF — это имя MOF-файла, который необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="8f8ac-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="8f8ac-108">В следующем примере показаны два MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="8f8ac-108">The following example shows two MOF files.</span></span> <span data-ttu-id="8f8ac-109">При компиляции первого файла MOF компилятор автоматически компилирует второй MOF-файл (Mymof2. MOF) в месте, где размещена \# Инструкция include.</span><span class="sxs-lookup"><span data-stu-id="8f8ac-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="8f8ac-110">В предыдущий пример включен следующий MOF-файл:</span><span class="sxs-lookup"><span data-stu-id="8f8ac-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="8f8ac-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8f8ac-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f8ac-112">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="8f8ac-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



