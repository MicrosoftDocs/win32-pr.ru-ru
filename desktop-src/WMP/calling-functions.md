---
title: Вызов функций
description: Вызов функций
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Обложки проигрывателя Windows Media, вызов функций в JScript
- обложки, вызов функций в JScript
- вызов функций в JScript
- Файлы JScript для обложек, вызов функций
- Обложки проигрывателя Windows Media, атрибут scriptFile в JScript
- обложки, атрибут scriptFile в JScript
- атрибуты, scriptFile в JScript
- атрибут scriptFile в JScript
- Файлы JScript для обложек, атрибут scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532462"
---
# <a name="calling-functions"></a><span data-ttu-id="8196a-112">Вызов функций</span><span class="sxs-lookup"><span data-stu-id="8196a-112">Calling Functions</span></span>

<span data-ttu-id="8196a-113">Если необходимо вызвать более нескольких строк кода, можно загрузить файл скрипта с помощью атрибута **scriptFile** элемента **View** и вызвать функции в скрипте.</span><span class="sxs-lookup"><span data-stu-id="8196a-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="8196a-114">В одном представлении можно загрузить несколько файлов:</span><span class="sxs-lookup"><span data-stu-id="8196a-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="8196a-115">После загрузки файлов скриптов можно вызывать в них функции из раздела представления.</span><span class="sxs-lookup"><span data-stu-id="8196a-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="8196a-116">Например, чтобы вызвать функцию с именем *MyFunction* при нажатии на нечто, введите следующее:</span><span class="sxs-lookup"><span data-stu-id="8196a-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="8196a-117">Если имеется более одного представления, то для кода XML и JScript, выполняемого с текущим представлением, доступны только функции из файлов, загруженных в текущее представление.</span><span class="sxs-lookup"><span data-stu-id="8196a-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="8196a-118">Файлы, загруженные в другие представления, не находятся в области действия с текущим представлением.</span><span class="sxs-lookup"><span data-stu-id="8196a-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8196a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8196a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8196a-120">**Использование JScript**</span><span class="sxs-lookup"><span data-stu-id="8196a-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




