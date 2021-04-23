---
description: Необходимо использовать функцию Сетупопенинффиле, чтобы открыть INF-файл, прежде чем можно будет получить из него сведения или добавить в него другие INF-файлы.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Открытие INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910336"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="13ce0-103">Открытие INF-файла</span><span class="sxs-lookup"><span data-stu-id="13ce0-103">Opening the INF File</span></span>

<span data-ttu-id="13ce0-104">Необходимо использовать функцию [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) , чтобы открыть INF-файл, прежде чем можно будет получить из него сведения или добавить в него другие INF-файлы.</span><span class="sxs-lookup"><span data-stu-id="13ce0-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="13ce0-105">Следующий командлет открывает INF-файл с помощью [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) и возвращает маркер минф в открытый файл INF.</span><span class="sxs-lookup"><span data-stu-id="13ce0-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="13ce0-106">Параметр *инфкласс* параметра **Сетупопенинффиле** указывается как **null** , чтобы указать, что класс INF-файла должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="13ce0-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="13ce0-107">После открытия файла INF можно вызвать функцию [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , чтобы добавить файл в открытый INF-файл.</span><span class="sxs-lookup"><span data-stu-id="13ce0-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="13ce0-108">Чтобы добавить несколько файлов, повторите эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="13ce0-108">To append several files, repeat this process.</span></span> <span data-ttu-id="13ce0-109">Если вызвать функцию **сетупопенаппендинффиле** и переданное в нее имя файла имеет **значение NULL**, функция выполнит поиск в разделе версии открытого INF-файла (и всех добавленных INF-файлов) для ключа лайаутфиле.</span><span class="sxs-lookup"><span data-stu-id="13ce0-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="13ce0-110">Если функция находит ключ, она добавляет файл, заданный этим ключом (обычно макет. INF).</span><span class="sxs-lookup"><span data-stu-id="13ce0-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="13ce0-111">Если несколько файлов INF объединены, **сетупопенаппендинффиле** начинает с последнего ДОБАВЛЕНного INF-файла при поиске раздела версии.</span><span class="sxs-lookup"><span data-stu-id="13ce0-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



