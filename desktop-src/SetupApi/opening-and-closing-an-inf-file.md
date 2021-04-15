---
description: Прежде чем функции настройки смогут получить доступ к информации в INF-файле, необходимо открыть ее с помощью вызова функции Сетупопенинффиле. Эта функция возвращает маркер в INF-файл.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Открытие и закрытие INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545791"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="557a8-104">Открытие и закрытие INF-файла</span><span class="sxs-lookup"><span data-stu-id="557a8-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="557a8-105">Прежде чем функции настройки смогут получить доступ к информации в INF-файле, необходимо открыть ее с помощью вызова функции [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) .</span><span class="sxs-lookup"><span data-stu-id="557a8-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="557a8-106">Эта функция возвращает маркер в INF-файл.</span><span class="sxs-lookup"><span data-stu-id="557a8-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="557a8-107">Если вы не знакомы с именем INF-файла, который необходимо открыть, можно использовать функцию [**сетупжетинффилелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) для получения списка файлов INF в каталоге.</span><span class="sxs-lookup"><span data-stu-id="557a8-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="557a8-108">После открытия INF-файла к открытому INF-файлу можно добавить дополнительные INF-файлы с помощью функции [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) .</span><span class="sxs-lookup"><span data-stu-id="557a8-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="557a8-109">Это функционально аналогично оператору include.</span><span class="sxs-lookup"><span data-stu-id="557a8-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="557a8-110">Если последующие функции установки ссылаются на открытый INF-файл, они также смогут получить доступ к любой информации, хранящейся в добавленных файлах.</span><span class="sxs-lookup"><span data-stu-id="557a8-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="557a8-111">Если не указать INF-файл во время вызова функции [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **сетупопенаппендинффиле** добавляет файлы, заданные ключом **лайаутфиле** в разделе **Version** файла Open INF.</span><span class="sxs-lookup"><span data-stu-id="557a8-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="557a8-112">Если сведения в INF-файле больше не нужны, вызовите функцию [**сетупклосеинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) , чтобы освободить ресурсы, выделенные во время вызова [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span><span class="sxs-lookup"><span data-stu-id="557a8-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



