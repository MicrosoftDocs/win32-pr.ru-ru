---
description: После открытия файла INF можно собирать сведения из него для создания пользовательского интерфейса или для направления процесса установки. Функции установки предоставляют несколько уровней функциональности для сбора информации из INF-файла.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Извлечение сведений о файлах из INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897766"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="53b88-104">Извлечение сведений о файлах из INF-файла</span><span class="sxs-lookup"><span data-stu-id="53b88-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="53b88-105">После открытия файла INF можно собирать сведения из него для создания пользовательского интерфейса или для направления процесса установки.</span><span class="sxs-lookup"><span data-stu-id="53b88-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="53b88-106">Функции установки предоставляют несколько уровней функциональности для сбора информации из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="53b88-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="53b88-107">Для сбора информации...</span><span class="sxs-lookup"><span data-stu-id="53b88-107">To gather information…</span></span>                | <span data-ttu-id="53b88-108">Использовать эти функции...</span><span class="sxs-lookup"><span data-stu-id="53b88-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="53b88-109">Сведения о INF-файле</span><span class="sxs-lookup"><span data-stu-id="53b88-109">About the INF file</span></span>                    | [<span data-ttu-id="53b88-110">**сетупжетинфинформатион**</span><span class="sxs-lookup"><span data-stu-id="53b88-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="53b88-111">**сетупкуеринффилеинформатион**</span><span class="sxs-lookup"><span data-stu-id="53b88-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="53b88-112">[**Сетупкуеринфверсионинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="53b88-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="53b88-113">Сведения об исходном и целевом файлах</span><span class="sxs-lookup"><span data-stu-id="53b88-113">About source and target files</span></span>         | [<span data-ttu-id="53b88-114">**сетупжетсаурцефилелокатион**</span><span class="sxs-lookup"><span data-stu-id="53b88-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="53b88-115">**сетупжетсаурцефилесизе**</span><span class="sxs-lookup"><span data-stu-id="53b88-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="53b88-116">**сетупжеттаржетпас**</span><span class="sxs-lookup"><span data-stu-id="53b88-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="53b88-117">**сетупжетсаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="53b88-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="53b88-118">Из строки INF-файла</span><span class="sxs-lookup"><span data-stu-id="53b88-118">From a line of an INF file</span></span>            | [<span data-ttu-id="53b88-119">**сетупжетлинетекст**</span><span class="sxs-lookup"><span data-stu-id="53b88-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="53b88-120">**сетупфинднекстлине**</span><span class="sxs-lookup"><span data-stu-id="53b88-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="53b88-121">**сетупфинднекстматчлине**</span><span class="sxs-lookup"><span data-stu-id="53b88-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="53b88-122">**сетупжетлинебиндекс**</span><span class="sxs-lookup"><span data-stu-id="53b88-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="53b88-123">**сетупфиндфирстлине**</span><span class="sxs-lookup"><span data-stu-id="53b88-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="53b88-124">Из поля строки в INF-файле</span><span class="sxs-lookup"><span data-stu-id="53b88-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="53b88-125">**сетупжетстрингфиелд**</span><span class="sxs-lookup"><span data-stu-id="53b88-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="53b88-126">**сетупжетинтфиелд**</span><span class="sxs-lookup"><span data-stu-id="53b88-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="53b88-127">**сетупжетбинарифиелд**</span><span class="sxs-lookup"><span data-stu-id="53b88-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="53b88-128">**сетупжетмултисзфиелд**</span><span class="sxs-lookup"><span data-stu-id="53b88-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="53b88-129">В следующем примере функция [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) используется для получения понятного пользователю описания исходного носителя из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="53b88-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="53b88-130">В этом примере Минф — это маркер открытого INF-файла.</span><span class="sxs-lookup"><span data-stu-id="53b88-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="53b88-131">SourceId — это идентификатор указанного исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="53b88-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="53b88-132">Описание value СРЦИНФО \_ указывает, что функция [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) должна извлекать описание исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="53b88-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="53b88-133">Буфер указывает на строку, которая получит описание, Максбуфсизе указывает ресурсы, выделенные буферу, а Буфсизе — ресурсы, необходимые для хранения буфера.</span><span class="sxs-lookup"><span data-stu-id="53b88-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="53b88-134">Если Буфсизе больше Максбуфсизе, функция возвратит **значение false**, а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет ошибку \_ недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="53b88-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
